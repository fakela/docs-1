---
description: Admin panel framework for your application
---

# Jet Admin User Guide

[![Preview](https://raw.githubusercontent.com/jet-admin/jet-bridge/master/static/overview.gif)](https://raw.githubusercontent.com/jet-admin/jet-bridge/master/static/overview.gif)

## Description

* About Jet Admin: [https://jetadmin.io](https://jetadmin.io/)
* **Live Demo**: [https://app.jetadmin.io/demo](https://app.jetadmin.io/demo)
* Documentation: [https://docs.jetadmin.io/](https://docs.jetadmin.io/)
* Support: [support@jetadmin.io](mailto:support@jetadmin.io)

**Jet Admin** is a SaaS service that automatically generates extendable back office for your application.   
**Jet Bridge** is a standalone app which generates REST API thought which your SQL database is connected to **Jet Admin**.   
This project has been designed to fit requirements of small startups and mature companies.

* **Data Privacy**. Jet does not access your data: its transferred directly from browser to your application.
* **Customizable Interface**. With WYSIWYG interface customization your can change almost every part of interface.
* **Extendable**. Flex Features allows you to create your custom Actions, Views, Fields and other.
* **Works with any technology**. The interface is generated automatically based on an analysis of the data and data structure of your database.
* **Quick installation**. All you need is to install Jet Bridge and connect it to your database.

This is a complete remake of our popular [Django Jet](https://github.com/geex-arts/django-jet) admin interface.

## Features

* **CRUD \(create, read, update, delete\)**

  All common operations to view, create, update or delete data.  
  [![CRUD \(create, read, update, delete\)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/list.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/list.jpeg)

* **Search and Filter**

  Filter data easily by any field with most common lookups and search them by text occurrence. For some specific cases you can create SQL Segment to filter with.  
  [![Search and Filter](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/filters.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/filters.jpeg)

* **Segments**

  Segments allow you to save applied set of filters as a Segment or create it from SQL query for quick use in future.  
  [![Segments](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/segment.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/segment.jpeg)

* **WYSIWYG Interface Customization**

  You can customize almost every part of interface visually – navigation menu, collection list views, record create/update forms.  
  [![WYSIWYG Interface Customization](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/customize.jpg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/customize.jpg)

* **List View layout**

  A number of out-of-the-box list layouts except default Table View like Kanban Board and Map with markers.  
  [![List View layout](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/kanban.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/kanban.jpeg)

* **Dashboards**

  Create different types of charts, tables and other widgets to visualize your KPIs or monitor data without programming – inside your visual interface. Complex data queries can be created with SQL.  
  [![Dashboards](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/dashboard.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/dashboard.jpeg)

* **Teams and Permissions**

  Invite users to collaborate on a project and assign access rights based on their team.  
  [![Teams and Permissions](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/users.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/users.jpeg)

* **Export**

  You can export all collection data or part of it into the most common formats like CSV or Excel.  
  [![Export](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/export.jpeg)](https://raw.githubusercontent.com/jet-admin/jet-bridge/dev/static/export.jpeg)

* **Responsive Layout**

  The interface is optimized for any device from phones to tablets to desktops.

## Extendability

While we are trying to include most of important features out of the box sometimes its not enough. For any specific cases we offer Flex features to implement functionality not available with standard features:

* **Custom Views**

  For very specific pages you can create your own custom FlexView based on React, Angular or any other framework and integrate it in Jet Admin interface. Writing your own custom JS/CSS/HTML has no limits in implementing any page you need.

* **Custom Actions**

  If need to run some operations on records or any other business logic inside your Backend you can create FlexActions and run them directly from Jet Admin interface. Passing some additional parameters to your Backend is supported.

* **Custom Fields**

  Sometimes using existing fields is not enough and you need to create custom which can be a combination of multiple fields, use fields from related collections and be result of some calculation. In this case you can use FlexField and write your custom JavaScript function which can format fields data any way you want.

## Support

Feel free to Email us – [support@jetadmin.io](mailto:support@jetadmin.io)

