# Custom Authorization

We provide different options for custom authorization flows based on your architecture and requirements. They all based on the fact that users and tokens are stored on Jet Admin side, but they can be duplicated and synchronized from your custom provider.

### 1. OAuth2/SAML provider \(Social Networks or Custom on your side\)

* You can connect your **SSO providers** to use for users **Sign In** and **Sign Up**.  [Learn more about SSO integrations](../user-guide/sso-integrations/)
* **User permissions** are stored on **Jet Admin** side, but you can ignore it if you are using **Additional tokens**. 
* You can use **Additional tokens** from your **SSO provider** for authenticating **HTTP** requests.

### 2. User synchronization \(by your backend\)

* You can implement **User synchronization** on your backend. [Learn more about managing Jet Admin users with our API](jet-admin-api/)
* It's possible to set up **Webhook** when user is added to the project
* You can save any **Additional tokens** from your backend to **User properties** and use them for authenticating **HTTP** requests.
* You can allow users to **Sign Up** by themselves [Learn more about Self Sign On](self-sign-up.md)

