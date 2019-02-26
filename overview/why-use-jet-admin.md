# How it works

**Jet Admin** is a SaaS frontend application hosted on **Jet Admin** side that works in your browser. It connects to your project SQL database through open source **Jet Bridge** backend application which you install on your side. So Integrating **Jet Admin**with your project requires installing only one component - **Jet Bridge**. Here how it should look like after installation:

![Jet Admin architecture](../.gitbook/assets/artboard-2.png)

**Your App**

Any of your applications which works with your **Database**. **Jet Admin** does not interact with it directly.

**Database**

Your database **Jet Admin** has no direct access to.

**Jet Bridge**

An open source application installed on your server's side and connected to your database. It automatically generates REST API based on your database structure. **Jet Interface** works with **Database** through **Jet Bridge**.

**Jet Interface**

Web application accessible from any browser. Maintaining and updating of this web application is on **Jet Admin** team side. Your application data is transmitted directly from **Jet Bridge** to **Jet Interface** in your browser and remain invisible for the **Jet Admin** service.



