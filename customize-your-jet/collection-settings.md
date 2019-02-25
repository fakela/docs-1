---
description: >-
  The Edit mode allows you to personalize all of your UI options, and is not
  limited to the reordering or hiding of collections or fields.
---

# Collection settings

### Accessing collection settings

To customize your fields widgets clicking on the 'Collection' tab in 'Settings'.

![](../.gitbook/assets/snimok-ekrana-2019-01-15-v-1.21.04.png)

### Configure the settings and accessibility of your collection

A lot of options are easily accessible and most of them are straightforward. However, you should know how some of them work.

### **Settings**

You are able to change the name, sorting field and order of all the records in a collection.

![](../.gitbook/assets/snimok-ekrana-2019-01-15-v-1.15.25.png)

### Configuring the settings and accessibility of your fields

Each field of a collection is also customizable. This is very useful in some use cases where you want to do a bit more than display the default name which is inherited from your database setup. For each field, depending on its type \(date, number, words…\) you can change the following :

* **Display name**: even if in your database the field has a specific name, you can choose a different Display name, usually a simpler one to boost the efficiency of your operations.
* **Description**: this description is useful when you create a new record in a collection. Below the field name you will then see what it refers to, or details about what should be indicated in the field.
* **Read only**: if you click on this option, nobody will be able to edit or change what is in the selected field.
* **Filtering enables**: in some situations, you do not want to allow the filters to be used on a field, this is the option you need to act on if this is the case.
* **Widget**: this very powerful feature allows you to display data in a more appropriate way than a text or a number. The list varies depending on your field type \(date, text, etc.\).

![](../.gitbook/assets/snimok-ekrana-2019-01-15-v-1.18.43.png)

#### Select Field

To specify all available options for **Select Field** fill in **params** field the following way**:**

```javascript
{"options":[
    {"value":"0","name":"PREORDER","color":"yellow"},
    {"value":"1","name":"TAKEAWAY","color":"blue"},
    {"value":"2","name":"BOOKING","color":"green"}
]}
```

* **value** - field value in your database
* **name** - text which will be used for displaying
* **color** can be one of: yellow, blue, green, red

![](../.gitbook/assets/image%20%2852%29.png)









