---
description: >-
  Let's reach 100% of our Setup Guide to customize Jet Admin to fit all your
  operational requirements.
---

# Setup Guide

Welcome to your new Back Office 🎉

### Introducing the Layout Editor mode

**Layout Edit** mode allows you to customize the entire UI, and is not limited to the visibility of your collections. 

![](../.gitbook/assets/customize_interface.png)

After having clicked on the "Customize Interface" button, you can choose one of the Customization interface area.

* **Menu** - Customize menu items, ordering, create section for each menu items group.
* **Change page view \(go to page that you want to edit\):**
  * **Dashboard** - Track your KPI using charts. 
  * **Collections view** - Customize your collections view, column visibility.
  * **Detail view** -  Customize collection records: layouts, fields, actions, relationships and widgets in one view to see all our important data at a glance.
* **Collection settings panel** - Configure all the fields widget available from the selected collection.

![](../.gitbook/assets/edit_mode%20%281%29.png)

In order to edit _collections, dashboard or detail collection record_  go to the specific page.

### **Configuring the visibility of your collections and fields**

Go to 'Edit mode' and choose the menu area, we can find all our available collections and delete those we don't want to see.

![](../.gitbook/assets/edit_mode_menu1.png)

To get the collection back go to "Add Item" and choose a "Collection link" item.

![](../.gitbook/assets/edit_mode_add_item.png)

![](../.gitbook/assets/edit_mode_add_item_model_link.png)

Let's click on the collection _Dishes_ and __go to Edit Mode_._ Then, we can see all the dishes records listed on a table view. We can hide and reorders the table's columns to be more usable by our business team.

![](../.gitbook/assets/edit_mode_collection_view1%20%281%29.png)

### Configure fields format 

Choosing the right widgets is an important step to display your data in the most usable way. In this example, we are configuring the collection _News_ to display the fields _Photo_ and _Date_ with more suitable widgets.

From the collection settings panel, _we can configure all the fields available from the selected collection._

![](../.gitbook/assets/edit_mode_menu_settings_news.png)

![](../.gitbook/assets/edit_mode_menu_settings_created_date.png)

For the _Created Date Time_ field, we chose the widget _Date/Time Field_ and the widget _Image Field_ for the field _Photo._

![](../.gitbook/assets/created_date_time_field.png)

![](../.gitbook/assets/news_photo_field.png)

![](../.gitbook/assets/news_all.png)

### **Change icons and collections names**

By default, Jet Admin is able to automatically set a suitable icon on the most common collections \(e.g. users, companies, payments and more\).

But of course, it's totally customizable. We can find all the collections customization settings from the collection settings panel. To open it, just click on the right cog icon beside the collection name from the left navigation bar.

![](../.gitbook/assets/edit_mode_menu_settings.png)

![](../.gitbook/assets/edit_mode_delete.png)

![](../.gitbook/assets/icons.png)

### Add a new chart

It's now the perfect timing to further in the UI customization. After clicking on the _Start_ button on the "Add a new chart" step, we will be automatically redirected to the Dashboard with the Layout Editor enabled.

From there, we can click "Add a new chart" to create our first chart. Then, we can create many different charts \(Line chart, Bar chart, Counter, List etc.\) using a simple builder or SQL.

![](../.gitbook/assets/charts.png)

#### Using simple builder

For now, we will just create a very simple **Counter** chart "Number of orders".

![](../.gitbook/assets/simple.png)

#### Using **SQL**

For now, we will just create a very simple **Pie chart** chart "Orders distributed by status types".

![](../.gitbook/assets/sql_chart.png)

### **Build Detail View UI**

A **Detail view** allows us to drag'n'drop sections, layouts, fields, actions, relationships and widgets in one view to see all our important data at a glance.

![](../.gitbook/assets/edit_mode_detail_view.png)

### Create a segment

Jet Admin lets you filter and segment any group of records to organize your data. Generally, they corresponds to the different steps of an operational process.

For example, we're implementing here the order's status and creating 3 segments corresponding to the possible status: _Preorder, Takeaway and Booking_. 

**Simple.** Build a search request and press 'Plus' button on the right. 

![](../.gitbook/assets/segments.png)

**Collection panel.** Go to 'Edit mode' and choose a 'Collection Settings' area. On the **Segments** tab press 'Add segment' button.

![](../.gitbook/assets/segment_edit.png)

By default, you can access to the segments from the collection's header and directly in the navigation bar. 

![](../.gitbook/assets/segment_view1.png)

![](../.gitbook/assets/segment_view2.png)

### Invite your teammates

User roles determine the access level or permissions of your teammates.

* **Admin** - Has all the privileges from the Editor role + can access all the project settings \(manage teams, users, environments, billings, etc.\).
* **Editor** - Has all the User privileges and can access to the UI customization through the **Layout Editor** mode.
* **User** - Can use all the features of the back office as an end user without accessing any customization options.

![](../.gitbook/assets/users%20%281%29.png)

![](../.gitbook/assets/jet_invite%20%281%29.png)

![](../.gitbook/assets/customer_support_invite.png)

![](../.gitbook/assets/sup.png)

### Create your new team and manage permissions

With the Jet's user management system, we can organize our interface per units \(e.g. support, tech, sales, etc.\) and keep control over who has access to which content in our company.

In this case, we have to upgrade to the Pro plan to benefits from this feature. The reason is because you first need to give a production \(or a remote environment\) access to multiple users before configuring their team-based permissions.

Once upgraded, we'll be able to create a new team. Below, we created a _Customer Support_ team and we chose to copy the layout from the _Operations_ team. 

![](../.gitbook/assets/customer_support.png)

We should manage permissions **All, Read, Write, Delete** for each collections.

### Create multiple projects

![](../.gitbook/assets/pr1.png)

![](../.gitbook/assets/mg1.png)

![](../.gitbook/assets/pr2.png)

