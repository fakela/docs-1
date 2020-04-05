---
description: Connecting Firebase to Jet Admin
---

# Firebase / Firestore

Jet Admin supports Firebase's Admin API and allows you to create your custom internal tools to manage your Firebase application.

Jet Admin supports managing users, querying and updating from Firebase Real-time Databases, and querying from Firestore.

### 1. Get Firebase Key

In the resources selector view - choose "Firebase." You will be prompted to provide a Service Account Key as well as a Database URL. The Service Account key is a JSON blob that you can create from your Firebase console, and the Database URL is how you can inform which database Jet Admin should use. For more information on how you can obtain these fields see Firebase's documentation [https://firebase.google.com/docs/admin/setup](https://firebase.google.com/docs/admin/setup)

**Firebase &gt; Project Settings &gt; Service accounts &gt; Generate a new private key**

![](../../.gitbook/assets/screen-shot-2020-02-14-at-6.21.29-pm.png)

After providing the Service Account Key and the Database URL, hit "Save." Jet Admin will validate that it is able to connect to your Firebase database and then save. If instead you are looking to integrate Jet Admin with Firestore, you need only fill in the _Project Id_ section on this form.

### 2. Add to Jet Admin

![](../../.gitbook/assets/group%20%283%29.png)



### 3. Customize interface for your use cases

{% page-ref page="../../user-guide/visual-builder.md" %}



