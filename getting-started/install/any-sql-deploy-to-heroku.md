# Any SQL – Deploy to Heroku

The simplest way to install **Jet Admin** is to deploy it to the **Heroku** cloud platform. It will require you to allow external access to your database.

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

1. Follow this guide to create a project: [https://app.jetadmin.io/projects/create](https://app.jetadmin.io/projects/create)
2. In the menu, choose '**SQL database**' as your technology stack and then select '**Deploy to Heroku**' as your installation method.

3. Press the appeared 'Deploy to Heroku' button. 

                                 [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/jet-admin/jet-bridge/tree/heroku)

4. Afterwards, you will be asked to specify the application name and database settings. Note: the **Project Name** and **Token** fields will be filled in automatically.   


   ![](../../.gitbook/assets/image%20%2835%29.png)



5. Finish your project installation by opening this link in your browser: [**http://YOUR\_APP\_HOST/api/register/**](http://localhost:8888/api/register/) where **YOUR\_APP\_HOST** is your **Heroku Application** HOST.

{% hint style="info" %}
If you don't have a **Jet** account yet, you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project, you will be redirected to your project and can start working with **Jet Admin**
{% endhint %}

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

