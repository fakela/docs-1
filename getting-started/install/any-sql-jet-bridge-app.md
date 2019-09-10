# Any SQL – Jet Bridge App

Install **Jet Bridge** without any additional software or web services on any server or localhost. You will need to install **Python** dependencies and run the application manually.

{% embed url="https://youtu.be/rELzK1DS084" %}



#### Requirements

* **Python** 2.7 or 3.4+
* **pip -** package manager for Python
* Any of the following **SQL Databases**:
  * PostgreSQL 
  * MySQL 
  * SQLite 
  * Oracle 
  * Microsoft SQL Server 
* **localhost** or **web server** with external IP

#### Installation

1. Follow this guide to create a project: [https://app.jetadmin.io/projects/create](https://app.jetadmin.io/projects/create)
2. Install **Python** 2.7 or 3.4+ \(comes with **pip\)** [https://www.python.org/downloads/](https://www.python.org/downloads/)
3. Install **jet\_bridge** package using pip or update if you did it before using command line

```bash
pip install jet_bridge -U
# or for Python 3
pip3 install jet_bridge -U
```

{% hint style="info" %}
For **Windows** you need to specify **pip** full path and run command this way \(**pip** is stored in **Scripts** folder inside **Python**, path may be different in your case\):  
_C:\Users\User\AppData\Local\Programs\Python\Python37-32\Scripts\pip.exe install jet\_bridge -U_
{% endhint %}

4. Install the appropriate database adapter and libraries

```bash
# for PostgreSQL
pip install psycopg2
# for PostgreSQL + PosGIS
pip install GeoAlchemy2==0.6.2
pip install Shapely==1.6.4

# for MySQL
pip install mysqlclient

# for MSSQL
pip install pyodbc
```

{% hint style="info" %}
For **Windows** and **MySQL** you may also need to install **Microsoft Visual C++ Redistributable for Visual Studio 2017:**  
[https://support.microsoft.com/ru-ru/help/2977003/the-latest-supported-visual-c-downloads](https://support.microsoft.com/ru-ru/help/2977003/the-latest-supported-visual-c-downloads)
{% endhint %}

5. Run **Jet Bridge** with the command line shown below:

```bash
jet_bridge 
```

If you run this command for the first time, you will be asked to enter the settings \(database host, port, etc.\) based on which a config file will be automatically generated. You can edit this config file later.

![](../../.gitbook/assets/image%20%2813%29.png)

After filling all required options, a config file will be generated and now you can run Jet Bridge by executing this command once again:

```bash
jet_bridge 
```

![Result of running Jet Bridge](../../.gitbook/assets/image%20%28115%29.png)

{% hint style="info" %}
You can read about all possible settings on the [Configuration]() page.
{% endhint %}

6. You will see the **Jet Admin** token in the console output which you should later enter on the **Project Create page**. If you want to display the **Jet Admin** token manually, use the following command:

```text
jet_bridge token
```

7. Finish your project installation by opening in your browser \(normally it should open automatically\): [**http://localhost:8888/api/register/**](http://localhost:8888/api/register/) where **localhost** is your **Jet Bridge** HOST and **8888** is its PORT. If you want to run Jet Bridge on different host/port you can configure it \(read more at [Configuration](https://docs.jetadmin.io/getting-started/configuration) page\).

{% hint style="info" %}
If you don't have **Jet** account yet, you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project, you will be redirected to your project and can start working with **Jet Admin.**
{% endhint %}

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

