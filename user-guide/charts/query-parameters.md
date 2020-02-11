# Query Parameters

## What are query parameters?

Sometimes you would need to switch between several time periods or user groups in one chart. For instance, if you want to measure progress in revenue over time, you would most likely want to compare it month-by-month and have the same chart for _January_, _February_, _etc_. To avoid creating multiple charts for each month, you can use **query parameters** instead. 

Query parameters will let you segment and switch between different data groups in the same chart, whether it is a **simple** or **SQL chart**.

## Add a simple chart parameter 

To add a parameter, open the chart builder by creating a new chart or clicking the cog icon next to the existing one and click +Add filter. In a new window, select a **field** that your parameter will be based on \(e.g. _Date_ for periods of time, _Payment Type_ for payment types, _etc._\) and specify the **filter type** \(e.g. _more than_, _equals to_, _etc._\).

For example, if you want to switch between different payment types on your chart, you would put _Payment Type_ as your field and _Equals_ as your filter type. 

Then, scroll down the last dropdown menu and click +Add Parameter.

![](../../.gitbook/assets/image%20%2816%29.png)

From there, you can specify the keyword and title of a new parameter as well as select its type \(e.g. text, number, dropdown list, etc.\)

![](../../.gitbook/assets/image%20%2842%29.png)

A new parameter will appear under your chart in the chart builder. 

![](../../.gitbook/assets/image%20%28115%29.png)

To edit a parameter, click on the cog icon to the right of the parameter's name. 

![](../../.gitbook/assets/image%20%28246%29.png)

## Add a SQL chart parameter

To add a new parameter to a SQL chart, click the Parameter button in the Live Query builder. 

![](../../.gitbook/assets/image%20%28267%29.png)

From there, specify the keyword and title of a new parameter as well as select its type \(e.g. text, number, dropdown list, etc.\)

![](../../.gitbook/assets/image%20%28199%29.png)

A new parameter will appear under your chart in the chart builder and in your query between double curly braces. To edit a parameter, click on the cog icon to the right of the parameter's name.

![](../../.gitbook/assets/image%20%28268%29.png)

