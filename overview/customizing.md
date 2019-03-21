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

![](../.gitbook/assets/image%20%2823%29.png)

![](../.gitbook/assets/image%20%2852%29.png)

### Saving changes when in Customize Mode

Once you have finished with customization don't forget to save changes with **Save button** at the bottom center of the screen.

![](../.gitbook/assets/image%20%287%29.png)

### **Flex Features**

While we are trying to include most of important features out of the box sometimes its not enough. For any specific cases we offer **Flex** features to implement functionality not available with standard features. You can read more about them below.

### FlexView

For very specific pages you can create your own custom **FlexView** based on **React,** **Angular** or any other framework and integrate it in **Jet Admin** interface. Writing your own custom **JS/CSS/HTML** has no limits in implementing any page you need.

To integrate your custom **FlexView** with **Jet Admin** data you can use **Jet Admin SDK** library.

Examples of using **FlexView** can be found on our GitHub:

* React – [https://github.com/jet-admin/jet-flex-view-react-example](https://github.com/jet-admin/jet-flex-view-react-example)
* Angular – [https://github.com/jet-admin/jet-flex-view-angular-example](https://github.com/jet-admin/jet-flex-view-angular-example)

Detailed tutorial how to create your own **FlexView** can be found here:

{% page-ref page="../customization/flexview.md" %}

### FlexAction

If need to run some operations on records or any other business logic inside your **Backend** you can create **FlexActions** and run them directly from **Jet Admin** interface. Passing some additional parameters to your **Backend** is supported.

Detailed tutorial how to create **FlexAction** can be found here:

{% page-ref page="../customization/flexaction.md" %}

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



