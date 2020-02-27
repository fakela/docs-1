---
description: Connect Jet Admin to any REST API.
---

# Rest API

You can make requests to any HTTP API with Jet Admin. Many developers get data from their own internal APIs, render them in `Table`s, then `post` data \(like resetting passwords\) back again to their own API. But you can also connect Jet Admin to APIs like Stripe, Salesforce, Slack, etc.

You query REST resources in an interface where you can set URL params, headers and cookies:

![](../../.gitbook/assets/rest-api.png)



## API Authentication

### OAuth 2.0

![](../../.gitbook/assets/screen-shot-2020-02-27-at-10.41.47-am.png)



![](../../.gitbook/assets/screen-shot-2020-02-27-at-10.42.54-am.png)

### Authorization bearer token

Adding an API that uses a bearer token authentication scheme is easy in Jet Admin. Just add it as a header in the Query.



## Define collections and query for your Rest API

![](../../.gitbook/assets/screen-shot-2020-02-27-at-10.53.18-am.png)



