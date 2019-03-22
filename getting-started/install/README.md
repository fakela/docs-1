---
description: >-
  How to integrate Jet Admin with your project with standalone Jet Bridge or
  using Docker containers
---

# Installation

## For any SQL database

In order to integrate **Jet Admin** with your project using **SQL** database you need to install **Jet Bridge**. It will connect to your database and link **Jet Admin** with your project.   
It will work even with your local application on **localhost**.

{% hint style="info" %}
**Jet Admin** is small web server using **Tornado** we framework that connects to your database and generates API interface through which **Jet Admin** can operate with your data.
{% endhint %}

**Jet Bridge** sources are available on **Github:**  
[https://github.com/jet-admin/jet-bridge](https://github.com/jet-admin/jet-bridge)

### Method 1. Deploy to Heroku

{% page-ref page="any-sql-deploy-to-heroku.md" %}

### Method 2. Using standalone Jet Bridge

{% page-ref page="any-sql-jet-bridge-app.md" %}

### Method 3. Using Jet Bridge inside Docker

{% page-ref page="any-sql-jet-bridge-docker.md" %}

## For Django framework

In order to integrate **Jet Admin** with your **Django** project using you need to install **Jet Bridge** package. It will connect your Django project to **Jet Admin**.   
It will work even with your local application on **localhost**.

**Jet Bridge** sources are available on **Github:**  
[https://github.com/jet-admin/jet-django](https://github.com/jet-admin/jet-django)

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

