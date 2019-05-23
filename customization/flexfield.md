# FlexField

### FlexField

Sometimes using existing fields is not enough and you need to create custom which can be a combination of multiple fields, use fields from related collections and be result of some calculation. In this case you can use **FlexField**.

You can defined your custom **JavaScript** function which can format fields data any way you want. With the help of model object you can access **Record** and also its related **Records** fields.

```javascript
  
function fieldValue(model) {
    return '[test] ' + model('unique_name')[0];
}

```

