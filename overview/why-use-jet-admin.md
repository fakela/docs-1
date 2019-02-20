# How it works

This page describes how **Jet Admin** operates and integrates with your project. Integrating **Jet Admin** with your project requires installing only one component - **Jet Bridge.**

### **A**rchitecture

![Jet Admin architecture](../.gitbook/assets/image%20%2812%29.png)

**Your app**  
Any of your applications which works with database. Jet Admin does not interact with it.

**Database**  
Your database Jet has no access to.

**Jet Bridge**  
An open source application installed on your server's side and connected to your database. Used for automatically API generation based on your data structure. It is needed for Jet Admin to operate with your data. 

**Jet Interface**  
Web application accessible from any browser. Maintaining and updating this web application is on **Jet Admin** team side. Your data is transmitted directly from Jet Bridge to Jet Interface which works in your browser and remain invisible for the Jet service.



