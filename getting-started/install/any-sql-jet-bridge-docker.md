# Any SQL – Jet Bridge Docker

Install **Jet Bridge** without installing any dependencies except the **Docker** application. May require additional network configuration for your OS.

**Jet Bridge** has a **Docker** image available on [Docker Hub](https://cloud.docker.com/u/jetadmin/repository/docker/jetadmin/jetbridge).  
In order start it inside **Docker** for your configuration run the following command.

You can read more about all possible settings on the [Configuration]() page.

#### Requirements

* **Docker** installed
* **localhost** or **web server** with external IP

#### Installation

1. Install **Docker** if you haven't yet and make sure it's running. [https://docs.docker.com/install/](https://docs.docker.com/install/)
2. Follow this guide to create a project: [https://app.jetadmin.io/projects/create](https://app.jetadmin.io/projects/create)
3. In the menu, choose 'SQL database' as your technological stack and select 'Install with Docker".                                                                                                                                                         

![](../../.gitbook/assets/image%20%28176%29.png)

4. Install Jet Bridge container by running:

```text
sh <(curl -s https://raw.githubusercontent.com/jet-admin/jet-bridge/master/install_jet.sh) hi_16 20a05f49-52c9-4015-ab72-9332dc0c8732
```

5. Finish your project installation by opening in your browser: [**http://localhost:8888/api/register/**](http://localhost:8888/api/register/) where **localhost** is your **Jet Bridge** HOST and **8888** is its PORT. 

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

{% page-ref page="django-framework-package.md" %}

## Common problems

{% page-ref page="common-problems.md" %}

