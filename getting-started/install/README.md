---
description: >-
  The following instructions will guide you through the installation process of
  Jet Admin
---

# Create a project

1. Start by creating a new account at [https://app.jetadmin.io/register](https://app.jetadmin.io/register) or sign up with Google/Facebook.

![](../../.gitbook/assets/snimok-ekrana-2019-07-23-v-12.00.06.png)

2. Once you've signed up, you'll be able to add a new project to Jet Admin and start the installation process. 

![](../../.gitbook/assets/snimok-ekrana-2019-07-23-v-12.25.17.png)

3. Specify the name of your project and choose how you would like to install Jet Admin. 

![](../../.gitbook/assets/snimok-ekrana-2019-07-23-v-12.03.19.png)



{% page-ref page="../adding-a-data-source.md" %}

**Databases**

In order to integrate **Jet Admin** with your project using **SQL** database you need to install **Jet Bridge**. It will connect to your database and link **Jet Admin** with your project.   
It will work even with your local application on **localhost**.

{% hint style="warning" %}
**Jet Admin** is a small web server using **Tornado** web framework that connects to your database and generates API interface through which **Jet Admin** can operate with your data.
{% endhint %}

**Jet Bridge** is open**-**source plugin are available on **Github:**  
[https://github.com/jet-admin/jet-bridge](https://github.com/jet-admin/jet-bridge)

### Method 1. Deploy to Heroku

The simplest way to install **Jet Admin** is to deploy it to the **Heroku** cloud platform. It will require you to allow external access to your database.

{% page-ref page="any-sql-deploy-to-heroku.md" %}

### Method 2. Using only Jet Bridge

Install **Jet Bridge** without additional software or web services on any server or localhost. You will need to install **Python** dependencies and run the application manually.

{% page-ref page="any-sql-jet-bridge-app.md" %}

### Method 3. Using Jet Bridge inside Docker

Install **Jet Bridge** without need to install any dependencies except **Docker** application. May require additional network configuration for your OS.

{% page-ref page="any-sql-jet-bridge-docker.md" %}

### For Django framework

To integrate **Jet Admin** with your **Django** project you need to install the **Jet Bridge** package. It will work even with your local application on **localhost**.

**Jet Bridge** **for Django** sources are available on **Github:**  
[https://github.com/jet-admin/jet-django](https://github.com/jet-admin/jet-django)

This is the quickest way to install **Jet Admin** for Django based projects. Installed in the same way as most **Django** packages.

{% page-ref page="django-framework-package.md" %}



###   3. **Enter a token.** 

Choose this option if you have already integrated Jet Bridge and received a token for your project. You'll be asked to enter your Jet Bridge API URL and Token to finish the installation. 

![](../../.gitbook/assets/snimok-ekrana-2019-07-23-v-12.29.18.png)

## Common problems

Please see our guide to fixing some of the most common installation issues.

{% page-ref page="common-problems.md" %}

