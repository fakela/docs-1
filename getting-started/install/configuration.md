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

{% tabs %}
{% tab title="jet.ini" %}
```text
[JET]
DATABASE_ENGINE=postgresql
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=mydb
DATABASE_USER=user
DATABASE_PASSWORD=password
```
{% endtab %}
{% endtabs %}

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
| **DATABASE\_HOST** | Database host |
| **DATABASE\_PORT** | Database port |
| **DATABASE\_USER** | Database user |
| **DATABASE\_PASSWORD** | Database password |
| **DATABASE\_NAME** | Database name or path \(SQLite\) |

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

