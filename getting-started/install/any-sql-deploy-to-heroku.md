# Any SQL – Deploy to Heroku

In order to install **Jet Admin** on your project please follow this guide:  
[https://app.jetadmin.io/projects/create](https://app.jetadmin.io/projects/create)

This documentation contains only **Jet Bridge** step detailed description.

The most simple way to try **Jet Admin** and deploy it to free **Heroku** cloud platform with a few clicks. It will require you to allow access to your database from external network.

#### Requirements

* Any of the following **SQL Databases**:
  * PostgreSQL 
  * MySQL 
  * SQLite 
  * Oracle 
  * Microsoft SQL Server 
  * Firebird 
  * Sybase
* SQL database installed on host with **external IP** and opened **port**

#### Installation

1. Create application on **Heroku** \(need to create account if you don't have\)

   [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/jet-admin/jet-bridge/tree/heroku)  
   You will be asked to specify application name and database settings  


   ![](../../.gitbook/assets/image%20%288%29.png)

2. You will see **Jet Admin** token in the console output which you should enter on **Project Create** page. If you want to display **Jet Admin** token manually, use the following command:

   ```text
   jet_bridge token
   ```

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

