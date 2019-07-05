# Any SQL – Deploy to Heroku

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

1. Follow this guide to create project: [https://app.jetadmin.io/projects/create](https://app.jetadmin.io/projects/create)
2. Create application on **Heroku** \(need to create account if you don't have\)

   [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/jet-admin/jet-bridge/tree/heroku)  
   You will be asked to specify application name and database settings  


   ![](../../.gitbook/assets/image%20%288%29.png)

3. You will see **Jet Admin** token in the console output which you should later enter on **Project Create** page. If you want to display **Jet Admin** token manually, use the following command: `jet_bridge token` 
4. Finish your project installation by opening in your browser: [**http://YOUR\_APP\_HOST/api/register/**](http://localhost:8888/api/register/) where **YOUR\_APP\_HOST** is your **Heroku Application** HOST.

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

