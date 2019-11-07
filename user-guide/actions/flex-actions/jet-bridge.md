# Jet Bridge

**Jet** uses its own universal messaging protocol via **REST API** to run actions on your **Backend**. So it will first ask your **Backend** for a list of available actions and then will execute them when you need to. Actions which are connected to some **Collection** will automatically appear in **Jet Admin** interface. To define your **FlexAction** you will need to implement single REST API method on your side to process 2 types of messages:

1. List of available actions and their parameters
2. Execution of particular action
3. Get field options

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
[    {        // each action shoud defined unique name        "name": "mail_users",        "model_action": {  // this is action which will be applied to selected users (for_instance==True flag)            "model": "users",  // this should be collection name            "for_instance": true,             "bulk": true // this allows to execute single action query with ids separated with comma instead of one query per row        }    },    {        "name": "refresh_users_status",        "model_action": { // this is action which will be applied to all users (no for_instance==True flag)            "model": "users"        }    },    {        "name": "refresh_users_status",        "common_action": { } // this is a common action which is not connected to any collections    }]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Example of **execute\_action** message response
{% endapi-method-response-example-description %}

```javascript
{    "result": true}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=202 %}
{% api-method-response-example-description %}
Example of **get\_field\_options** message response
{% endapi-method-response-example-description %}

```javascript
[    {        'value': 'london',        'name': 'London',        'color': 'blue'    },    {        'value': 'new_york',        'name': 'New York',        'color': 'green'    }]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### 

