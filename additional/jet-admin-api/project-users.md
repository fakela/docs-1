# Project Users

{% api-method method="get" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/users/" %}
{% api-method-summary %}
Get list of all project users
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="PROJECT\_NAME" type="string" required=true %}
Unique project name \(can be taken from Jet Admin project URL\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token authentication, example:   
`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    id: 1504,
    user: {
        username: "a.svetlov@geex-arts.com"
        first_name: "Anton"
        last_name: "Svetlov"
        email: "a.svetlov@geex-arts.com"
        photo: "https://api.jetadmin.io/media/user/photo/2018/10/09/18402150_1144874585658871_7416256167591393723_o.jpg"
        uid: "28c9bc6d-1f80-4898-93d3-154fa66b22ac"
    },
    user_email: null
    group: {
        id: 1491
        name: "Administrators"
        description: ""
        super_group: true
        project_permissions: []
        properties: {}
    },
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/users/" %}
{% api-method-summary %}
Invite new project user and send invite
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="PROJECT\_NAME" type="string" required=true %}
Unique project name \(can be taken from Jet Admin project URL\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token authentication, example:   
`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="user\_email" type="string" required=true %}
User email, example: a.svetlov@geex-arts.com
{% endapi-method-parameter %}

{% api-method-parameter name="group" type="number" required=true %}
Group ID, example: 1491
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="object" required=false %}
JSON Object, example: {office: "New York"}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    id: 1504,
    user_email: null
    group: 1491,
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/users/:USER\_ID/" %}
{% api-method-summary %}
Update existing project user
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="PROJECT\_NAME" type="string" required=true %}
Unique project name \(can be taken from Jet Admin project URL\)
{% endapi-method-parameter %}

{% api-method-parameter name="USER\_ID" type="number" required=true %}
Project user ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token authentication, example:   
`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="user\_email" type="string" required=false %}
User email, example: a.svetlov@geex-arts.com
{% endapi-method-parameter %}

{% api-method-parameter name="group" type="number" required=false %}
Group ID, example: 1491
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="object" required=false %}
JSON Object, example: {office: "New York"}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    id: 1504,
    user_email: null
    group: 1491,
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/users/:USER\_ID/" %}
{% api-method-summary %}
Delete existing project user
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="PROJECT\_NAME" type="string" required=true %}
Unique project name \(can be taken from Jet Admin project URL\)
{% endapi-method-parameter %}

{% api-method-parameter name="USER\_ID" type="number" required=true %}
Project user ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token authentication, example:   
`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

