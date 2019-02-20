# Customizing

Most of **Jet Admin** interface customization is available directly in your browser without need of developers work so that any person can customize it. To achieve it we implemented **Customize Mode**.

{% hint style="info" %}
For more advanced customization you can use [Flex Features](customizing.md#flex-features)
{% endhint %}

### Enable Customize Mode

To start customizing interface directly from your browser:

1. Click **Customize Interface** button.
2. Choose which section you want to customize **\(1\)**, **\(2\)** or **\(3\).** Depending on which page you are on sections **\(2\)** and **\(3\)** can change.

{% hint style="success" %}
You can begin customization. You can find more about possible customization in next sections of this page.
{% endhint %}

![](../.gitbook/assets/image%20%2817%29.png)

![](../.gitbook/assets/image%20%2844%29.png)

### Saving changes when in Customize Mode

Once you have finished with customization don't forget to save changes with **Save button** at the bottom center of the screen.

![](../.gitbook/assets/image%20%285%29.png)

### **Flex Features**

While we are trying to include most of important features out of the box sometimes its not enough. For any specific cases we offer **Flex** features to implement functionality not available with standard features. You can read more about them below.

### FlexView

For very specific pages you can create your own custom **FlexView** based on **React,** **Angular** or any other framework and integrate it in **Jet Admin** interface. Writing your own custom **JS/CSS/HTML** has no limits in implementing any page you need.

To integrate your custom **FlexView** with **Jet Admin** data you can use **Jet Admin SDK** library.

Examples of using **FlexView** can be found on our GitHub:

* React – [https://github.com/jet-admin/jet-flex-view-react-example](https://github.com/jet-admin/jet-flex-view-react-example)
* Angular – [https://github.com/jet-admin/jet-flex-view-angular-example](https://github.com/jet-admin/jet-flex-view-angular-example)

Detailed tutorial how to create your own FlexView can be found here:

{% page-ref page="../customization/flexview.md" %}

### FlexAction

If need to run some operations on records or any other business logic inside your **Backend** you can create **FlexActions** and run them directly from **Jet Admin** interface. Passing some additional parameters to your **Backend** is supported.

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

### FlexField

Sometimes using existing fields is not enough and you need to create custom which can be a combination of multiple fields, use fields from related collections and be result of some calculation. In this case you can use **FlexField**.

You can defined your custom **JavaScript** function which can format fields data any way you want. With the help of model object you can access **Record** and also its related **Records** fields.

```javascript
  
function fieldValue(model) {
    return '[test] ' + model('unique_name')[0];
}

```

### FlexCollection

Not always data you want to view in admin interface is stored in a single table. For such cases **FlexCollection** can be created that can represent a combination of data from different data sources and/or result of some calculations.



