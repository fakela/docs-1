---
description: >-
  How to integrate Jet Admin with your project with standalone Jet Bridge or
  using Docker containers
---

# Installation

## For any SQL database

### Method 1. Using standalone Jet Bridge

In order to integrate **Jet Admin** with your project using **SQL** database you need to install **Jet Bridge**. It will connect to your database and link **Jet Admin** with your project.   
It will work even with your local application on **localhost**.

{% hint style="info" %}
**Jet Admin** is small web server using **Tornado** we framework that connects to your database and generates API interface through which **Jet Admin** can operate with your data.
{% endhint %}

#### Requirements

* **Python** 2.7 or 3.4+
* Any of the following **SQL Databases**:
  * PostgreSQL 
  * MySQL 
  * SQLite 
  * Oracle 
  * Microsoft SQL Server 
  * Firebird 
  * Sybase

#### Installation

1. Install **jet\_bridge** package using pip or update if you did it before

```bash
pip install jet_bridge -U
```

2. Install appropriate database adapter

```bash
# for PostgreSQL
pip install psycopg2
# for MySQL
pip install mysqlclient
```

3. Run **Jet Bridge** for your configuration.   
You can read about all possible settings at [Configuration](configuration.md) page.

```bash
DATABASE_ENGINE=postgresql \
    DATABASE_HOST=host.docker.internal \
    DATABASE_PORT=5432 \
    DATABASE_NAME=database \
    DATABASE_USER=postgres \
    DATABASE_PASSWORD=password \
    jet_bridge 
```

![Result of running Jet Bridge](../.gitbook/assets/image%20%2828%29.png)

4. Register your project by opening in your browser:   
**http://localhost:8888/** where **localhost** is your **Jet Bridge** HOST and **8888** is its PORT.  
If you want to run Jet Bridge on different host/port you can configure it \(read more at [Configuration](configuration.md) page\).

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

After registering your project you will be redirected to your project and can start working with **Jet**

### Method 2. Using Jet Bridge inside Docker

**Jet Bridge** has **Docker** image available on [Docker Hub](https://cloud.docker.com/u/jetadmin/repository/docker/jetadmin/jetbridge).  
In order start it inside **Docker** for your configuration run the following command.  
You can read about all possible settings at [Configuration](configuration.md) page.

1. Install **Docker** if you don't have it [https://docs.docker.com/install/](https://docs.docker.com/install/)
2. Make sure **Docker** is running
3. Update **Jet Bridge** image if downloaded it before

```text
docker pull jetadmin/jetbridge
```

4. Run **Docker** container. This will run Jet Bridge on **http://localhost:8888/.** 

{% hint style="info" %}
If you want to run on different port change it here:  
****`... -p 9000:8888 ...` – this will run on **9000**
{% endhint %}

```bash
docker run -p 8888:8888 \
    -e DATABASE_ENGINE=postgresql \
    -e DATABASE_HOST=host.docker.internal \
    -e DATABASE_PORT=5432 \
    -e DATABASE_NAME=database \
    -e DATABASE_USER=postgres \
    -e DATABASE_PASSWORD=password \
    jetadmin/jetbridge
```

{% hint style="warning" %}
If you are using **Docker before 18.03** you can't use `host.docker.internal` for DATABASE\_HOST  
**Docker 17.12 – 18.02** use `docker.for.mac.host.internal`  
**Docker 17.06 – 17.11** use `docker.for.mac.localhost`  
**Docker 17.05 and below** your `local host IP address` \(can be found using `ifconfig` command\)
{% endhint %}

5. Register your project by opening in your browser:   
**http://localhost:8888/** where **localhost** is your **Jet Bridge** HOST and **8888** is its PORT.  
If you want to run Jet Bridge on different host/port you can configure it by changing **Docker** container port in this command. 

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

## For Django framework

In order to integrate **Jet Admin** with your project using **SQL** database you need to install **Jet Bridge**. It will connect to your database and link **Jet Admin** with your project.   
It will work even with your local application on **localhost**.

#### Requirements

* **Python** 3.4+
* **Django** 1.11+

#### Installation

1. Download and install latest version of **Jet Bridge** for **Django**:

```text
pip install jet-django
```

2. Add `jet_django` application to the `INSTALLED_APPS` setting inside **settings.py** file:

```text
INSTALLED_APPS = (
  ...
  'jet_django',
  ...
)
```

3. Add URL-pattern to the **urls.py** file:

```text
from jet_django.urls import jet_urls

urlpatterns = [
  ...
  url(r'^jet_api/', include(jet_urls)),
  ...
]
```

4. Apply migrations:

```text
python manage.py migrate jet_django
```

5. Restart your project

6. Open **YOUR\_PROJECT\_URL/jet\_api/register/** in browser to create a project. Normally it should open automatically on start up.

## Common problems

### CORS issue

If you deploying **Jet Bridge** behind proxy or some web server you can start receiving the following errors in your browser console:

> Access to XMLHttpRequest at '...' from origin 'https://app.jetad.io.io' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource.

Normally you shouldn't have this issue as **Jet Bridge** automatically adds the appropriate **CORS** headers to all responses.

#### Behind Nginx

To fix **CORS** issue for **Nginx** add the following to your server config:

{% code-tabs %}
{% code-tabs-item title="my-website.conf" %}
```text
server {
    listen 80;
    ...

    location / {
      ###################################
      # START
      # Add this block to your location
      ###################################
      
      proxy_hide_header 'Access-Control-Allow-Origin';
      proxy_hide_header 'Access-Control-Allow-Methods';
      proxy_hide_header 'Access-Control-Allow-Headers';
      proxy_hide_header 'Access-Control-Expose-Headers';

      if ($request_method = 'OPTIONS') {
        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, PATCH, DELETE, OPTIONS';
        add_header 'Access-Control-Allow-Headers' 'Authorization,DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range';
        add_header 'Access-Control-Max-Age' 1728000;
        add_header 'Content-Type' 'text/plain; charset=utf-8';
        add_header 'Content-Length' 0;
        return 204;
      }

      add_header 'Access-Control-Allow-Origin' '*' always;
      add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, PATCH, DELETE, OPTIONS';
      add_header 'Access-Control-Allow-Headers' 'Authorization,DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range';
      add_header 'Access-Control-Expose-Headers' 'Content-Length,Content-Range';
      
      ###################################
      # END
      ###################################
      
      ...
      proxy_pass http://webserver;
      ...
    }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

