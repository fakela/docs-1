# Create a chart

### 1. Add a Chart Widget

To create a new chart, enter the Visual Builder mode from a dashboard to which you would like to add the chart. Then, choose an appropriate chart widget from the menu on the right. 

You can learn more about all chart types and their functions here:

{% page-ref page="chart-widgets.md" %}

![](../../.gitbook/assets/image%20%28151%29.png)

### 2. Build a Query

Once you drag and dropped a chart on your dashboard, you would have to build a query to specify this chart's parameters. There are two types of queries in Jet:

1. Simple 
2. SQL

![](../../.gitbook/assets/image%20%2831%29.png)

### 2.1 Creating a simple chart

1. Type in the name of a chart 
2. Select a widget \(in case you'd like to change it\)
3. Select a collection that will be a data source
4. Apply filters to disctinct the needed data
5. Choose aggregation function: 

* Count
* Sum
* Min
* Max
* Avg

If you would like to add several charts, press '+ Add more':

![](../../.gitbook/assets/image%20%2853%29.png)

For each chart you can set legend and color:

![](../../.gitbook/assets/image%20%28179%29.png)

Select fields using 'Group by' 

```sql
SELECT 
    (
        CASE issues_status_id 
        WHEN 1 THEN 'Return' 
        WHEN 2 THEN 'Refund' 
        WHEN 3 THEN 'Out of stock'
        END
    ) AS gr, 
    COUNT(*) 
FROM
    issues
GROUP BY gr
ORDER BY gr;

```

### Doughnut chart

Here's an example of creating a doughnut chart:

![](../../.gitbook/assets/image%20%28247%29.png)

Display:

![](../../.gitbook/assets/image%20%28210%29.png)

![](../../.gitbook/assets/image%20%2826%29.png)



### 2.2 Creating a Chart with SQL

To create a complex chart with SQL, switch to the SQL tab in the editing chart window. Next do the following:

1. Specify the name of a new chart
2. Select a chart widget \(in case you'd like to change it\)
3. Run a SQL query 
4. Choose columns for display
5. Specify the "group by" and "display" parameters

![](../../.gitbook/assets/image%20%28293%29.png)

### Line chart

You must returned two or more \(for a few charts\) columns. In the following example, we simply count the number of `ride` per month.

```sql
SELECT
    DATE_TRUNC('month', start) AS gr,
    count(*)
FROM 
    ride
GROUP BY gr
ORDER BY gr;
```

![](../../.gitbook/assets/image%20%28200%29.png)



### Bar chart

```sql
SELECT
    (
        CASE onboarding_status 
        WHEN 1 THEN 'New' 
        WHEN 2 THEN 'Review' 
        WHEN 3 THEN 'Activated' 
        WHEN 4 THEN 'Rejected' 
        END
    ) AS gr,
    COUNT(id)
FROM
    driver_onboarding
GROUP BY gr
ORDER BY gr DESC;
```

![](../../.gitbook/assets/image%20%28167%29.png)

### Pie / Doughnut chart

```sql
SELECT
    (
        CASE order_status_id 
        WHEN 1 THEN 'New order' 
        WHEN 2 THEN 'In Progress' 
        WHEN 3 THEN 'Delivired'
        END
    ) AS gr, 
    COUNT(id) 
FROM
    order_history
GROUP BY gr
ORDER BY gr;
```

![](../../.gitbook/assets/image%20%2882%29.png)

### Counter

```sql
SELECT 
    SUM(total_amount) * SUM(currency)
FROM
    transaction
```

![](../../.gitbook/assets/image%20%2881%29.png)

### List

```sql
SELECT 
    name
FROM 
    customer
ORDER BY rating;
```

![](../../.gitbook/assets/image%20%28176%29.png)

## Parameters

Learn more about query parameters here:

{% page-ref page="query-parameters.md" %}

