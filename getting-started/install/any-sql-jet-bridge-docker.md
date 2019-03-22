# Any SQL – Jet Bridge Docker

Install **Jet Bridge** without need to install any dependencies except **Docker** application. May require additional network configuration for your OS.

**Jet Bridge** has **Docker** image available on [Docker Hub](https://cloud.docker.com/u/jetadmin/repository/docker/jetadmin/jetbridge).  
In order start it inside **Docker** for your configuration run the following command.  
You can read about all possible settings at [Configuration](../configuration.md) page.

#### Requirements

* **Docker** installed
* **localhost** or **web server** with external IP

#### Installation

1. Install **Docker** if you don't have it [https://docs.docker.com/install/](https://docs.docker.com/install/)
2. Make sure **Docker** is running
3. Update **Jet Bridge** image if downloaded it before

```text
docker pull jetadmin/jetbridge
```

4. Run **Docker** container. This will run Jet Bridge on **http://localhost:8888/.** 

{% hint style="info" %}
If you want to run on different port change it here:  
****`... -p 9000:8888 ...` – this will run on **9000**
{% endhint %}

```bash
docker run -p 8888:8888 \
    -e DATABASE_ENGINE=postgresql \
    -e DATABASE_HOST=host.docker.internal \
    -e DATABASE_PORT=5432 \
    -e DATABASE_NAME=database \
    -e DATABASE_USER=postgres \
    -e DATABASE_PASSWORD=password \
    jetadmin/jetbridge
```

{% hint style="warning" %}
If you are using **Docker before 18.03** you can't use `host.docker.internal` for DATABASE\_HOST  
**Docker 17.12 – 18.02** use `docker.for.mac.host.internal`  
**Docker 17.06 – 17.11** use `docker.for.mac.localhost`  
**Docker 17.05 and below** your `local host IP address` \(can be found using `ifconfig` command\)
{% endhint %}

5. Register your project by opening in your browser:   
**http://localhost:8888/** where **localhost** is your **Jet Bridge** HOST and **8888** is its PORT.  
If you want to run Jet Bridge on different host/port you can configure it by changing **Docker** container port in this command. 

{% hint style="info" %}
If you don't have **Jet** account yet you will be asked to create one and sign in with the existing account.
{% endhint %}

{% hint style="success" %}
After registering your project you will be redirected to your project and can start working with **Jet**
{% endhint %}

