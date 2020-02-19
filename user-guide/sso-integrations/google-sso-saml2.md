# Google SSO \(SAML2\)

Setting up **SSO** for your **Jet Admin** project requires your to set up **Custom Domain** for your project first.

### 1. Go to SSO Applications

![](../../.gitbook/assets/image%20%28177%29.png)

### 2. Create a new SSO application

![](../../.gitbook/assets/image%20%2843%29.png)

### 3. Open your G Suite SAML Apps and create a new one

![](../../.gitbook/assets/image%20%28283%29.png)

### 4. Select SETUP MY OWN CUSTOM APP

![](../../.gitbook/assets/image%20%2883%29.png)

### 5. Download IDP metadata .xml file

![](../../.gitbook/assets/image%20%28313%29.png)

### 6. Specify application basic information

![](../../.gitbook/assets/image%20%28309%29.png)

### 7. Set up Jet Admin SSO application and copy ACS URL

Specify **Entity ID** and upload saved **Metadata \(.xml\)** file from the previous step.  
**Entity ID** should be unique text identifier of your application

**ACS URL** displayed at the bottom of page will be needed on the next step.

![](../../.gitbook/assets/image%20%28100%29.png)

### 8. Set up G Suite SAML App

Specify **ACS URL** and **Entity ID** entered on the previous step

![](../../.gitbook/assets/image%20%2818%29.png)

### 9. Set attributes mapping

You should specify 3 attributes to map on Jet Admin user account:

* **Email** should map to **Basic Information - Primary Email**
* **FirstName** should map to **Basic Information - First Name**
* **LastName** should map to **Basic Information - Last Name**

![](../../.gitbook/assets/image%20%28120%29.png)

### 10. You are all set

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.

![](../../.gitbook/assets/image%20%28275%29.png)

![](../../.gitbook/assets/image%20%2886%29.png)

