# FlexAction

If need to run some operations on records or any other business logic inside your **Backend** you can create **FlexActions** and run them directly from **Jet Admin** interface. Passing some additional parameters to your **Backend** is supported.

### Method 1 – Jet Bridge

**Jet** uses its own universal messaging protocol via **REST API** to run actions on your **Backend**. So it will first ask your **Backend** for a list of available actions and then will execute them when you need to. Actions which are connected to some **Collection** will automatically appear in **Jet Admin** interface. To define your **FlexAction** you will need to implement single REST API method on your side to process 2 types of messages:

1. List of available actions and their parameters
2. Execution of particular action

After you have implemented this **API method** you should specify **Messages URL** field in your Jet Admin **Project Settings**  to finish integration.

{% api-method method="post" host="http://YOURBACKEND" path="/api/messages/" %}
{% api-method-summary %}
Jet Admin messages REST API endpoint
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="object" required=false %}
Authorization Token which you should check
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="params" type="object" required=false %}
Optional action parameters
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Unique messages name, may be one of:  
**get\_action\_list**, **execute\_action**
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Example of **get\_action\_list** message response
{% endapi-method-response-example-description %}

```javascript
[
    {
        // each action shoud defined unique name
        "name": "mail_users",
        "model_action": {  // this is action which will be applied to selected users (for_instance==True flag)
            "model": "users",  // this should be collection name
            "for_instance": true, 
            "bulk": true // this allows to execute single action query with ids separated with comma instead of one query per row
        }
    },
    {
        "name": "refresh_users_status",
        "model_action": { // this is action which will be applied to all users (no for_instance==True flag)
            "model": "users"
        }
    },
    {
        "name": "refresh_users_status",
        "common_action": { } // this is a common action which is not connected to any collections
    }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Example of **execute\_action** message response
{% endapi-method-response-example-description %}

```javascript
{
    "result": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Method 2 – Jet Django

To implement integration you should have installed **Jet** for your **Backend** environment. This will allow you to write actions processing on your favourite language and environment. **Jet** uses its own universal messaging protocol to run actions on your **Backend**. So it will first ask your **Backend** for a list of available actions and then will execute them when you need to. Actions which are connected to some **Collection** will automatically appear in **Jet Admin** interface. To define your **FlexAction** first **create \(1\)** and then **import \(2\)** message handlers the following way:

{% code-tabs %}
{% code-tabs-item title="jet\_messages.py" %}
```python
from jet_django.admin.jet import jet
from jet_django.messages import GET_ACTION_LIST, EXECUTE_ACTION

# define handler which will return all possible actions
def get_action_list(params):
    return [
        {
            # each action shoud defined unique name
            'name': 'mail_users',
            'model_action': {  # this is action which will be applied to selected users (for_instance==True flag)
                'model': 'users;user',  # this should be collection name
                'for_instance': True, 
                'bulk': True # this allows to execute single action query with ids separated with comma instead of one query per row
            }
        },
        {
            'name': 'refresh_users_status',
            'model_action': { # this is action which will be applied to all users (no for_instance==True flag)
                'model': 'users;user'
            }
        },
        {
            'name': 'refresh_users_status',
            'common_action': { } # this is a common action which is not connected to any collections
        }
    ]

# define handler which will process all possible actions
def execute_action(params):
    if params['name'] == 'mail_users':
        # Your custom action processing here
        ids = params.get('params', {}).get('ids')
        return {
            'result': True
        }

# add defined handlers
jet.add_message_handler(GET_ACTION_LIST, get_action_list)
jet.add_message_handler(EXECUTE_ACTION, execute_action)

```
{% endcode-tabs-item %}

{% code-tabs-item title="apps.py" %}
```python
from django.apps import AppConfig

class CoreConfig(AppConfig):
    name = 'core'

    def ready(self):
        # import your handlers
        from . import jet_messages
```
{% endcode-tabs-item %}
{% endcode-tabs %}

![Collection FlexAction example](../.gitbook/assets/image%20%2810%29.png)

![Record FlexAction example](../.gitbook/assets/image%20%2814%29.png)

You can also ask users for some parameters for your action if you need. In order to achieve it you should define their description in **params** key. After that parameters form will appear in **Jet Admin** interface automatically.

**params** field is an array of possible parameters in the following format:

* **name** – unique name of action
* **field** – type of parameter, should be one of the following:
  * BooleanField 
  * TranslatableField 
  * SelectField 
  * ForeignKey 
  * DateTimeField 
  * TimestampField 
  * DateField 
  * TimeField 
  * JSONField 
  * SqlField 
  * CodeField 
  * CharField 
  * TextField 
  * IntegerField 
  * FloatField 
  * DecimalField
* **params** – additional parameters for fields, for example **ForeignKey** requires you to specify **related\_model** option

{% code-tabs %}
{% code-tabs-item title="flex\_action\_params\_example.py" %}
```python
# Example for requesting paramters from user for action
def get_action_list(params):
    return [
        {
            'name': 'account_transfer',
            'model_action': {
                'model': ['projects;income', 'projects;outcome'],
                'for_instance': False
            },
            'params': [
                {
                    'name': 'account_from',
                    'field': 'ForeignKey',
                    'params': {'related_model': {'model': 'projects;account'}}
                },
                {
                    'name': 'amount_from',
                    'field': 'DecimalField'
                },
                {
                    'name': 'account_to',
                    'field': 'ForeignKey',
                    'params': {'related_model': {'model': 'projects;account'}}
                },
                {
                    'name': 'amount_to',
                    'field': 'DecimalField'
                },
                {
                    'name': 'description',
                    'field': 'TextField',
                    'required': False
                },
                {
                    'name': 'date',
                    'field': 'DateTimeField',
                    'required': False
                }
            ]
        }
    ]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

![](../.gitbook/assets/image%20%2825%29.png)

### 

