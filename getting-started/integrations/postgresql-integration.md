---
description: Connecting PostgresQL to Jet Admin
---

# Database Integration

### 1. Add PostgreSQL to Jet Admin

Create a new resource in **Jet Admin**, and select "PostgreSQL" as the _type_. Enter your database connection details.

We recommend setting up separate resources for read and write access to make it harder to accidentally cause unwanted changes to your database. When setting up a resource to write to your database, you can enable a simplified interface that can make standard SQL write queries to further reduce the chance of errors.

**Resources** &gt; **Add** &gt; **PostgreSQL**

![](../../.gitbook/assets/screen-shot-2020-03-04-at-5.20.57-pm.png)

### 2. Deployment Method



