# Django framework – Package

In order to install **Jet Admin** on your project please follow this guide:  
[https://app.jetadmin.io/projects/create](https://app.jetadmin.io/projects/create)

This documentation contains only **Jet Bridge** step detailed description.

Its the most simple way to try and use **Jet Admin** for Django based projects. Installed the same way as most **Django** packages.

In order to integrate **Jet Admin** with your project using **SQL** database you need to install **Jet Bridge**. It will connect to your database and link **Jet Admin** with your project.   
It will work even with your local application on **localhost**.

{% hint style="info" %}
**Jet Admin** for **Django** is a Python package installed with **pip** that integrates with your **models** and generates **API** interface through which **Jet Admin** can operate with your data. Though using this package is supported we recommend to use [standalone Jet Bridge](./#method-1-using-standalone-jet-bridge) as described before if possible.
{% endhint %}

**Jet Bridge** for **Django** sources are available on **Github:**  
[https://github.com/jet-admin/jet-django](https://github.com/jet-admin/jet-django)

#### Requirements

* **Python** 3.4+
* **Django** 1.11+
* **localhost** or **web server** with external IP

#### Installation

1. Download and install latest version of **Jet Bridge** for **Django**:

```bash
pip install jet-django
```

2. Add `jet_django` application to the `INSTALLED_APPS` setting inside **settings.py** file:

```python
INSTALLED_APPS = (
  ...
  'jet_django',
  ...
)
```

3. Add URL-pattern to the **urls.py** file:

```python
from jet_django.urls import jet_urls

urlpatterns = [
  ...
  url(r'^jet_api/', include(jet_urls)),
  ...
]
```

4. Apply migrations:

```bash
python manage.py migrate jet_django
```

5. Restart your project

6. You will see **Jet Admin** token in the console output which you should later enter on **Project Create** page. If you want to display **Jet Admin** token manually, use the following management command:

```bash
python manage.py jet_token
```

7. Finish your project installation by opening in your browser: [**http://localhost:8000/jet\_api/register/**](http://localhost:8000/jet_api/register/) where **localhost** is your **Django** HOST and **8000** is its PORT.   
**Please note!** **Jet Django** package sets **CORS** headers for **/jet\_api/** endpoints. If it conflicts with your **CORS** headers and you want to deal with it yourself, add the following in **settings.py**:

```python
JET_CORS_HEADERS = False
```

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

