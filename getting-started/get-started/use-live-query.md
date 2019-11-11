# Use Live Query

When you need to implement your own custom logic into a chart, you can create a SQL chart with the Live Query.

Let's create a line chart to show the progress in the number of rides each month. To create a complex chart with SQL, switch to the SQL tab in the editing chart window. Next do the following:

1. Specify the name of a new chart
2. Select a chart widget \(in case you'd like to change it\)
3. Run a SQL query 
4. Choose columns for display
5. Specify the "group by" and "display" parameters

![](../../.gitbook/assets/image%20%28275%29.png)

In the following example, we simply counted the number of `ride`s per month.

```sql
SELECT
    DATE_TRUNC('month', start) AS gr,
    count(*)
FROM 
    ride
GROUP BY gr
ORDER BY gr;
```

![](../../.gitbook/assets/image%20%28187%29.png)



