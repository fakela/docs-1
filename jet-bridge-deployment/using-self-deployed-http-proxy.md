# Using self-deployed HTTP proxy

By default all queries for **HTTP based resources** \(**Custom Rest API, 3rd party integrations**\) are sent by **Jet Admin** through our **Jet Bridge** proxy endpoint at [https://api.jetadmin.io/api/proxy\_request/](https://api.jetadmin.io/api/proxy_request/) for convenience. Requests data going through our servers are never being recorded, but if you don't want data to go through **Jet Admin** servers you can use self hosted **HTTP Proxy** on your side as part of open source **Jet Bridge** application.

## Using self-deployed HTTP proxy

Follow instructions after you have created **Jet Admin** **Rest API** resource:

#### 1. Install Jet Bridge

Use the following guides to install **Jet Bridge** application as standalone **Python application** or **Docker container**:

{% page-ref page="install/any-sql-jet-bridge-docker.md" %}

{% page-ref page="install/any-sql-jet-bridge-app.md" %}

{% hint style="info" %}
You can skip database configuration part and use **Jet Bridge** just for proxying **HTTP requests**.
{% endhint %}

#### 2. Set up Jet Bridge

Go to **Project Settings -&gt; Resources -&gt; Choose Rest API resource** and copy **Jet Bridge Token**:

![](../.gitbook/assets/image%20%28340%29.png)

Specify the following **Jet Bridge** configuration:

**DATABASE\_ENGINE** = none  
**TOKEN** = &lt;token from project settings&gt;

Check the link below to learn how to specify **Jet Bridge** configuration:

{% page-ref page="install/configuration.md" %}

#### 3. Run Jet Bridge with the updated configuration

**4. Update resource to use custom HTTP proxy**

In resource settings click **Edit Settings** button and set **Custom HTTP proxy** to your **Jet Bridge** proxy request URL:  
&lt;**JET\_BRIDGE\_HOST&gt;/api/proxy\_request/**

For example for Jet Bridge running on localhost and port 8888 this will be:   
[http://localhost:8888/api/proxy\_request/](http://localhost:8888/api/proxy_request/)

![](../.gitbook/assets/image%20%28341%29.png)

#### 5. You are done!

Now all HTTP queries for this resource will be sent through your server.

