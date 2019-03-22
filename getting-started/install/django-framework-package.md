# Django framework – Package

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

6. Open **YOUR\_PROJECT\_URL/jet\_api/register/** in browser to create a project. 

