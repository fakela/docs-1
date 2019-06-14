# How it works

**Jet Admin** is a SaaS frontend application hosted on **Jet Admin** side that works in your browser. It connects to your project SQL database through open source **Jet Bridge** backend application which you install on your side. So Integrating **Jet Admin** with your project requires installing only one component - **Jet Bridge**. Here how it should look like after installation:

![Jet Admin architecture](../.gitbook/assets/artboard-2.png)

**Your App**

Any of your applications which works with your **Database**. **Jet Admin** does not interact with it directly.

**Database**

Your database **Jet Admin** has no direct access to.

**Jet Bridge**

An open source application installed on your server's side and connected to your database. It automatically generates REST API based on your database structure. **Jet Interface** works with **Database** through **Jet Bridge**.

**Jet Interface**

Web application accessible from any browser. Maintaining and updating of this web application is on **Jet Admin** team side. Your application data is transmitted directly from **Jet Bridge** to **Jet Interface** in your browser and remain invisible for the **Jet Admin** service.

### 

### Data Privacy

The main advantage of Jet Admin’s architecture is that absolutely no data transits or crosses our servers. The user accesses application data directly from the client and Jet Admin is just deployed as a service to display and interact with the data. 

With Jet Admin, your data are transferred directly from your application to your browser while remaining invisible to our servers.

### Security

We use a two-step authentication to connect you to both Jet Admin’s server and your Admin API.

The first step is to retrieve your UI configuration. When logging into your account, your credentials are sent to the Jet Admin’s server which returns the UI token to authenticate your session.

The second step is to authenticate to your Jet Bridge – generated admin backend or to your app \(to get access to your data\). Your password is sent to your Admin API which returns the Data token signed by the JET\_ADMIN\_AUTH\_SECRET you chose. Each of your requests to your Admin API are authenticated with the Data Token.

In a nutshell, your admin uses the UI token to make request about the UI configuration. Then the Data Token is used to make queries on your Admin API to manage your data. All our tokens are generated using the JWT standard.







