# Project Teams

{% api-method method="get" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/groups/" %}
{% api-method-summary %}
Get list of all project teams
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
[
    {
        id: 35091
        name: "Sales"
        description: ""
        super_group: false
        project_permissions: [
            {
                id: 525
                permission_type: "model"
                permission_object: "jet_bridge.users_user"
                permission_actions: "r"
                date_add: "2019-03-22T19:03:02.425689+03:00"
            }
        ],
        properties: {
            industry: "EdTech"
        }
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/groups/" %}
{% api-method-summary %}
Create new project team
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
{% api-method-parameter name="name" type="string" required=false %}
Group name, example: "Sales"
{% endapi-method-parameter %}

{% api-method-parameter name="super\_group" type="boolean" required=true %}
If group will have all permissions
{% endapi-method-parameter %}

{% api-method-parameter name="project\_permissions" type="array" required=true %}
Array of permissions
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="object" required=false %}
JSON Object, example: {"industry": "New York"}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    id: 35091
    name: "Sales"
    description: ""
    super_group: false
    project_permissions: [
        {
            id: 525
            permission_type: "model"
            permission_object: "jet_bridge.users_user"
            permission_actions: "r"
            date_add: "2019-03-22T19:03:02.425689+03:00"
        }
    ],
    properties: {
        industry: "EdTech"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/groups/:GROUP\_ID/" %}
{% api-method-summary %}
Update existing project team
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="PROJECT\_NAME" type="string" required=true %}
Unique project name \(can be taken from Jet Admin project URL\)
{% endapi-method-parameter %}

{% api-method-parameter name="GROUP\_ID" type="number" required=true %}
Group ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token authentication, example:   
`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
Group name, example: "Sales"
{% endapi-method-parameter %}

{% api-method-parameter name="super\_group" type="boolean" required=false %}
If group will have all permissions
{% endapi-method-parameter %}

{% api-method-parameter name="project\_permissions" type="array" required=false %}
Array of permissions
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="object" required=false %}
JSON Object, example: {"industry": "New York"}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    id: 35091
    name: "Sales"
    description: ""
    super_group: false
    project_permissions: [
        {
            id: 525
            permission_type: "model"
            permission_object: "jet_bridge.users_user"
            permission_actions: "r"
            date_add: "2019-03-22T19:03:02.425689+03:00"
        }
    ],
    properties: {
        industry: "EdTech"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.jetadmin.io" path="/api/projects/:PROJECT\_NAME/groups/:GROUP\_ID/" %}
{% api-method-summary %}
Delete existing project team
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="PROJECT\_NAME" type="string" required=true %}
Unique project name \(can be taken from Jet Admin project URL\)
{% endapi-method-parameter %}

{% api-method-parameter name="GROUP\_ID" type="number" required=true %}
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
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

