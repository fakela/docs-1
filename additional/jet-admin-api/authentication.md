# Authentication

You should use your **Project Token** to authenticate all **Jet Admin API** requests \(can be taken from your **Jet Bridge** config or at the bottom **Project Settings** inside **Jet Admin**\).

{% api-method method="get" host="https://api.jetadmin.io" path="/api/....." %}
{% api-method-summary %}
For any Jet Admin API requests
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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

