# Customize List View

### Enable Customize Mode

To start customizing interface directly from your browser:

1. Click **Customize Interface** button
2. Choose which section you want to customize **\(1\)**, **\(2\)** or **\(3\).** Depending on which page you are on sections **\(2\)** and **\(3\)** can change

{% hint style="success" %}
You can begin customization. You can find more about possible customization in next sections of this page.
{% endhint %}

![](../.gitbook/assets/image%20%2822%29.png)

![](../.gitbook/assets/image%20%2851%29.png)

### Saving changes when in Customize Mode

Once you have finished with customization don't forget to save changes with **Save button** at the bottom center of the screen.

![](../.gitbook/assets/image%20%287%29.png)

### Changing Data layout

{% hint style="info" %}
To start enable Customization Mode first as described [here](layout-editor.md#enable-customize-mode).
{% endhint %}

By default all **collections** are displayed as tables. Some kind of **collections** are more appropriate to display with different layout. For example **Map** layout is more suitable for displaying restaurants than **Table** layout for some cases. Displaying Orders on **Kanban Board** gives you UI of a common **CRM** system.

To change **Data layout** turn on **Customize Interface** on **Collection List** page and select appropriate **Data layout** from the right menu.

All possible **Data layouts** in next sections.

{% hint style="success" %}
Once you have finished don't forget to save **Menu Customization** changes with **Save button** at the bottom center of the screen as described [here](layout-editor.md#saving-changes-of-customize-mode).
{% endhint %}

![](../.gitbook/assets/image%20%2835%29.png)

#### Data layout – Table

![](../.gitbook/assets/image%20%2846%29.png)

#### Data layout – Map

![](../.gitbook/assets/image%20%2860%29.png)

#### Data layout – Kanban Board

![](../.gitbook/assets/image%20%2836%29.png)

#### Data layout – Timetable

![](../.gitbook/assets/image%20%285%29.png)

#### Data layout – Sidelist

![](../.gitbook/assets/image%20%2831%29.png)

### Changing table columns

{% hint style="info" %}
To start enable Customization Mode first as described [here](layout-editor.md#enable-customize-mode).
{% endhint %}

To start changing columns of Table click **Edit Columns** button \(1\). Popup with Columns will appear.

![](../.gitbook/assets/image%20%2827%29.png)

#### Show/hide columns

You can turn on/off columns of table by clicking toggles next to each item **\(3\).** Table should instantly update.

#### Reorder columns

To reorder table columns just drag and drop them with a mouse to appropriate place.

### Add FlexField \(custom column\)

{% hint style="info" %}
To start enable Customization Mode first as described [here](layout-editor.md#enable-customize-mode).
{% endhint %}

Sometimes using existing columns is not enough and you need to create custom which can be a combination of multiple fields, use fields from related collections and be result of some calculation. In this case you can use **FlexField**.

To add **FlexField** click **Edit Columns** button \(1\). Popup with Columns will appear. Click **Add FlexField** button.

Then you need to specify fields:

* **Name** – unique name of field \(underscored\)
* **Verbose name** – name of field used for displaying
* **Field type** – type of data fields contains
* **Javascript Code** that perform field calculation. You can access current or related collection fields with `model` object.

Click **Create** button once you've finished.

{% hint style="success" %}
Once you have finished don't forget to save **Menu Customization** changes with **Save button** at the bottom center of the screen as described [here](layout-editor.md#saving-changes-of-customize-mode).
{% endhint %}

