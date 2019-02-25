# Browse

Every type of data \(_list of Restaurants, Orders, Users, etc._\) can be viewed in a table view. This screen allows you to find the appropriate record you are looking for and view/edit/delete or perform some operations on it.

![](../.gitbook/assets/image%20%2866%29.png)

### Navigating by page

Initially first records are displayed – in order to load more data you can just scroll the table and it will automatically load more data. Current position and number of pages are displayed under the table. If you want to navigate directly to exact page \(i.e. go to the last page\) you can just click the page you need.

![](../.gitbook/assets/image%20%2836%29.png)

### Number of records

You can find the number of records currently filtered \(or just number of all records if no filters have been applied\) at the bottom of the list. 

{% hint style="info" %}
In case of large number of records the approximate count is displayed in order to speed up loading. This optimization works only for **PostreSQL** and **MySQL** databases.
{% endhint %}

![](../.gitbook/assets/image%20%2814%29.png)

### Performing operations on selected records

You can select records by clicking on table rows or checkboxes in the left column. The popup menu with possible operations will show once you select at least once record. Clicking the right mouse button on the row selects only this row.

![](../.gitbook/assets/image%20%2822%29.png)

You can perform the following operations on selected records:

* Edit
* Duplicate \(only if 1 record selected\)
* Move
* Delete
* Your custom operations – [FlexActions]()

![](../.gitbook/assets/mass_operation%20%281%29.png)

{% hint style="info" %}
If you want to perform operation on all records you can put a tick at the top left of the list
{% endhint %}

### Select/deselect all records

If you want to perform operation on all records you can click on **Select All** link in the popup menu which appears once you start selecting records. And if you want to cancel selection you can click on **Deselect** link in the popup menu.

![](../.gitbook/assets/image%20%2857%29.png)

### Sorting records \(in database\)

If your collection can be sorted by some field in database \(i.e. Menu Items ordering\) you can get this functionality out of the box. You can move record by dragging row with a mouse.

![](../.gitbook/assets/image%20%2849%29.png)

Using sorting requires configuring **Ordering field** in collection's settings \(_Customize Interface → System settings_ from collection table view or from project [Collection List](../customize-your-jet/collection-settings.md)\). On **General** tab specify sorting field in **Ordering Field** \(this field should be able to store 0 and positive integers\) and save changes. After that you will be apply to reorder your collection's records by dragging table rows. ****

![](../.gitbook/assets/image%20%2838%29.png)

### Thumbnails for Image fields

**Jet Bridge** automatically generates thumbnails for fields containing images to decrease page loading speed and amount of data transferred. This may be especially noticeable for fields containing large images. Media directory will be used for caching generated thumbnails, maximum space that will be used is **50MB**. If cache space is exceeded older thumbnails will be replaced with new ones.

### Ordering of records \(in table\)

You can sort data in table by any column in **ascending** or **descending** order. To sort data by particular column in **ascending** order just click on column name. Click again to change order to **descending**. For example, in the if you do this on the ‘Created Date’ column which are dates, you will sort the data by order of creation, from the latest to the oldest or vice versa. If you do the same on the ‘Second Name’ column, it will reorder the data in alphabetical order. Current column used for ordering is marked with appropriate indicator.

![](../.gitbook/assets/image%20%2831%29.png)

### Customizing

Displaying columns, their ordering and other UI can be customized directly in **Jet Admin** interface.

[Read More](layout-editor.md) about table view customizing.

