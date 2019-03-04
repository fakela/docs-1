# Settings

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

{% code-tabs %}
{% code-tabs-item title="jet.ini" %}
```text
[JET]
DATABASE_ENGINE=postgresql
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=mydb
DATABASE_USER=user
DATABASE_PASSWORD=password
```
{% endcode-tabs-item %}
{% endcode-tabs %}

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

| **Name** | Description |
| :--- | :--- |
| **DATABASE\_ENGINE** | Database engine, one of: - postgresql - mysql - oracle - mssql - sqlite |
| **DATABASE\_HOST** | database\_host |
| **DATABASE\_PORT** | database\_port |
| **DATABASE\_USER** | database user |
| **DATABASE\_PASSWORD** | database password |
| **DATABASE\_NAME** | database name or path \(SQLite\) |

### Optional settings

| Name | Default | Description |
| :--- | :--- | :--- |
| **ADDRESS** \(optional\) | 0.0.0.0 | Server address |
| **PORT** \(optional\) | 8888 | port', default=8888, help='server port', type=int\)  |
| **CONFIG** \(optional\) | /etc/jet.conf | config', default=DEFAULT\_CONFIG\_PATH, help='config file path'\)  |
| **DEBUG** \(optional\) | false | debug mode |
| **READ\_ONLY** \(optional\) | false | read only |
| **WEB\_BASE\_URL** \(optional\) | [https://app.jetadmin.io](https://app.jetadmin.io) | Jet Admin frontend application base URL |
| **API\_BASE\_URL** \(optional\) | [https://api.jetadmin.io/api](https://api.jetadmin.io/api) | Jet Admin API base URL |
| **MEDIA\_STORAGE** \(optional\) | default | media storage type |
| **MEDIA\_ROOT** \(optional\) | media | media root |
| **MEDIA\_BASE\_URL** \(optional\) | -- none -- | media base URL |

