# FlexField

### FlexField

Sometimes using existing fields is not enough and you need to create custom which can be a combination of multiple fields, use fields from related collections and be result of some calculation. In this case you can use **FlexField**.

Go to **FlexField** create page as shown below   
\(Project Settings → Collections → Choose Collection → FlexField → Create\)

You can defined your custom **JavaScript** function which can format fields data any way you want. With the help of model object you can access **Record** and also its related **Records** fields.

Here are some basic example to get understanding:

#### Get Record field

```javascript
  
function fieldValue(model) {
    return model('unique_name');
}

```

#### Combine record fields

```javascript
  
function fieldValue(model) {
    return model('first_name') + ' ' + model('last_name');
}
```

#### Get number of related collection records

```javascript
  
function fieldValue(model) {
    return model('photos').length
}

```

#### Parse JSON field

```javascript

function formatDate(date) {
    return date.toLocaleString('en');
}
  
function fieldValue(model) {
    const data = model('json_field');

    if (!data['timestamp']) {
        return;
    }
        
    const date = new Date(data['timestamp'])
    const formated = formatDate(from);
    const parts = formated.split(', ');
    return parts[0] + ' ' + parts[1];
}

```

