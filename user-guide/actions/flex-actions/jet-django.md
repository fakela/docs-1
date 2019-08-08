# Jet Django



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
{% endcode-tabs %}

{% code-tabs %}
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

