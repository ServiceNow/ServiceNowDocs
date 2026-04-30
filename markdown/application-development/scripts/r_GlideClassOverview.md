---
title: Glide class overview
description: The ServiceNow Glide classes expose JavaScript APIs that enable you to conveniently work with tables using scripts.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Glide class overview

The ServiceNow Glide classes expose JavaScript APIs that enable you to conveniently work with tables using scripts.

Using the Glide APIs, you can perform database operations without writing SQL queries, display UI pages, and define UI actions. The following tables provide brief descriptions of the Glide classes and links to detailed information.

|Class|Description|
|-----|-----------|
|GlideRecord|Use this class for database operations instead of writing SQL queries. GlideRecord is a special Java class that can be used in JavaScript exactly as if it were a native JavaScript class. A GlideRecord is an object that contains records from a single table. See [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideElement|Use this class to operate on the fields of the current GlideRecord. See [GlideElement](https://www.servicenow.com/docs/access?context=c_GlideElementScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideSystem|Use this class to get information about the system. See [GlideSystem](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideAggregate|Use this class to perform database aggregation queries, such COUNT, SUM, MIN, MAX, and AVG, for creating customized reports or calculations in calculated fields. See [GlideAggregate](https://www.servicenow.com/docs/access?context=c_GlideAggregateScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideDateTime|Use this class to perform date-time operations, such as date-time calculations, formatting a date-time, or converting between date-time formats. See [GlideDateTime](https://www.servicenow.com/docs/access?context=c_GlideDateTimeScoped&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|

|Class|Description|
|-----|-----------|
|GlideAjax|Use this class to execute server-side code from the client. See [GlideAjax](https://www.servicenow.com/docs/access?context=c_GlideAjaxAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideDialogWindow|Use this class to display a dialog window. See [GlideDialogWindow](https://www.servicenow.com/docs/access?context=c_GlideDialogWindowAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideForm|Use this class to customize forms. See [GlideForm](https://www.servicenow.com/docs/access?context=c_GlideFormAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideList2|Use this class to customize \(v2\) lists, including normal lists and related lists. See [GlideList2](https://www.servicenow.com/docs/access?context=c_GlideList2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideMenu|Use this class to customize UI Context Menu items. See [GlideMenu](https://www.servicenow.com/docs/access?context=c_GlideMenuAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|GlideUser|Use this class to get session information about the current user and current user roles. See [GlideUser](https://www.servicenow.com/docs/access?context=c_GlideUserAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|

-   **[Glide stack](r_GlideStack.md)**  
Glide is an extensible Web 2.0 development platform written in Java that facilitates rapid development of forms-based workflow applications \(work orders, trouble ticketing, and project management, for example\).

**Parent Topic:**[Scripting](../../topic/c_Script.md)

