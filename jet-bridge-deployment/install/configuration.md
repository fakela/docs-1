# Configuration

## Setting up your configuration

You can specify **Jet Bridge** configuration through one of the following methods:  
command line arguments, config file or environment variables. Here are examples:

### Method 1. Command line arguments

{% hint style="info" %}
Warning: arguments name should be lowercase. Other methods are case insensitive
{% endhint %}

```bash
jet_bridge --database_engine=postgresql \
    --database_host=localhost \
    --database_port=5432 \
    --database_user=user \
    --database_password=password \
    --database_name=mydb
```

### Method 2. Config file

{% code title="jet.ini" %}
```text
[JET]
DATABASE_ENGINE=postgresql
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=mydb
DATABASE_USER=user
DATABASE_PASSWORD=password
```
{% endcode %}

### Method 3. Environment variables

```bash
DATABASE_ENGINE=postgresql \
    DATABASE_HOST=localhost \
    DATABASE_PORT=5432 \
    DATABASE_NAME=mydb \
    DATABASE_USER=user \
    DATABASE_PASSWORD=password \
    jet_bridge
```

## All available settings

### Required settings

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Name</b>
      </th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>DATABASE_ENGINE</b>
      </td>
      <td style="text-align:left">
        <p>Database engine, one of:
          <br />postgresql
          <br />mysql
          <br />oracle
          <br />mssql
          <br />sqlite</p>
        <p>none</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>DATABASE_HOST</b>
      </td>
      <td style="text-align:left">Database host</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>DATABASE_PORT</b>
      </td>
      <td style="text-align:left">Database port</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>DATABASE_USER</b>
      </td>
      <td style="text-align:left">Database user</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>DATABASE_PASSWORD</b>
      </td>
      <td style="text-align:left">Database password</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>DATABASE_NAME</b>
      </td>
      <td style="text-align:left">Database name or path (SQLite)</td>
    </tr>
  </tbody>
</table>

### Optional settings

| Name | Default | Description |
| :--- | :--- | :--- |
| **ADDRESS** \(optional\) | 0.0.0.0 | Jet Bridge address |
| **PORT** \(optional\) | 8888 | Jet Bridge port |
| **CONFIG** \(optional\) | /etc/jet.conf | Path to config file |
| **DEBUG** \(optional\) | false | Run in debug mode |
| **READ\_ONLY** \(optional\) | false | Data read only |
| **WEB\_BASE\_URL** \(optional\) | [https://app.jetadmin.io](https://app.jetadmin.io) | Jet Admin frontend application base URL |
| **API\_BASE\_URL** \(optional\) | [https://api.jetadmin.io/api](https://api.jetadmin.io/api) | Jet Admin API base URL |
| **MEDIA\_STORAGE** \(optional\) | default | Media storage type |
| **MEDIA\_ROOT** \(optional\) | media | Media root |
| **MEDIA\_BASE\_URL** \(optional\) | -- none -- | Media base URL |

