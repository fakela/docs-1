# Segments

**Segments** allow you to use applied set of filters in future or create a sub-collection from it. The only information needs to create a **segment** for collection is a name and filters.

There are two ways to create Segment – on **Collection List** or **Collection Settings** page.

### Create Segment on Collection List Page

To create a new **Segment:**

1. Add filters on Collection List page \(as described on [Filtering](filter.md)\)
2. Click on **plus** button next to the filters list \(_New segment from filters_ tip will appear\) as on screenshot below. 
3. **Add Segment** popup will appear. Enter **Segment Name** and click **Add Segment** button.

{% hint style="success" %}
Your filters will be replaced with new **Segment** and a new **Segment** will appear in menu section of currently selected collection.
{% endhint %}

![](../.gitbook/assets/image%20%2863%29.png)

### Create Segment on Collection Settings Page

1. Open **Collection Settings** page one of the following ways:
   * Collection List/Edit page → Customize Interface → System Settings
   * Project Settings → Collections → Choose Collection
2. Go to **Segments** tab **\(1\)**
3. Click **Add Segment** button **\(2\)**
4. Fill segment information:
   1. **Segment Name \(3\)**
   2. **Segment Filters \(4\)** - adding filters is just the same as on **Collection List** [page](filter.md#adding-filters). Click **Add** button, choose parameters in appeared popup: **Filtering Field**, **Type of Filter** and **Filter Value.**
5. Click **Create** button

{% hint style="success" %}
New **Segment** will appear in menu section of currently selected collection and **Segments List**.
{% endhint %}

![](../.gitbook/assets/image%20%284%29.png)

### Create SQL Query Segments

For some complicated cases when general filtering is not enough you can create **Segment** from **SQL** **query**. Create segment just like in case of [Create Segment on Collection Settings Page](segments-1.md#create-segment-on-collection-settings-page), but instead of adding filters choose **SQL** type for segment and enter **SQL query** that will return records **ID** in the first column of query result.

