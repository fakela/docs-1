# Any SQL – Jet Bridge App

Install **Jet Bridge** without additional software or services on any server or localhost. It will require you to install **Python** dependencies and run the application yourself.

#### Requirements

* **Python** 2.7 or 3.4+
* **pip -** package manager for Python
* Any of the following **SQL Databases**:
  * PostgreSQL 
  * MySQL 
  * SQLite 
  * Oracle 
  * Microsoft SQL Server 
  * Firebird 
  * Sybase
* **localhost** or **web server** with external IP

#### Installation

1. Install **Python** 2.7 or 3.4+ \(comes with **pip\)** [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Install **jet\_bridge** package using pip or update if you did it before using command line

```bash
pip install jet_bridge -U
# or for Python 3
pip3 install jet_bridge -U
```

{% hint style="info" %}
For **Windows** platform you need to specify **pip** full path and run command this way \(**pip** is stored in **Scripts** folder inside **Python**, path may be different in your case\):  
_C:\Users\User\AppData\Local\Programs\Python\Python37-32\Scripts\pip.exe install jet\_bridge -U_
{% endhint %}

3. Install appropriate database adapter

```bash
# for PostgreSQL
pip install psycopg2
# for MySQL
pip install mysqlclient
```

{% hint style="info" %}
For **Windows** and **MySQL** you may also need to install **Microsoft Visual C++ Redistributable for Visual Studio 2017:**  
[https://support.microsoft.com/ru-ru/help/2977003/the-latest-supported-visual-c-downloads](https://support.microsoft.com/ru-ru/help/2977003/the-latest-supported-visual-c-downloads)
{% endhint %}

4. Run **Jet Bridge** with the command line as shown below:

```bash
jet_bridge 
```

If you run this command for the first time you will be asked to enter settings \(database host, port, etc.\) based on which a config file will be automatically generated. You can  edit this config file later.

![](../../.gitbook/assets/image%20%283%29.png)

After filling all required options config file will be generated and now you can run Jet Bridge by executing command once again:

```bash
jet_bridge 
```

![Result of running Jet Bridge](../../.gitbook/assets/image%20%2830%29.png)

{% hint style="info" %}
You can read about all possible settings at [Configuration](../configuration.md) page.
{% endhint %}

5. Register your project by opening in your browser:   
**http://localhost:8888/api/register/** where **localhost** is your **Jet Bridge** HOST and **8888** is its PORT. Normally it should open automatically on start up.

If you want to run Jet Bridge on different host/port you can configure it, read more about it on [Settings](../configuration.md) page.

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

After registering your project you will be redirected to your project and can start working with **Jet**

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

