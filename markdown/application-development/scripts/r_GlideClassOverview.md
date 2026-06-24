---
title: Glide class overview
description: The ServiceNow Glide classes expose JavaScript APIs that enable you to conveniently work with tables using scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/scripts/r\_GlideClassOverview.html
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Glide class overview

The ServiceNow Glide classes expose JavaScript APIs that enable you to conveniently work with tables using scripts.

Using the Glide APIs, you can perform database operations without writing SQL queries, display UI pages, and define UI actions. The following tables provide brief descriptions of the Glide classes and links to detailed information.

|Class|Description|
|-----|-----------|
|GlideRecord|Use this class for database operations instead of writing SQL queries. GlideRecord is a special Java class that can be used in JavaScript exactly as if it were a native JavaScript class. A GlideRecord is an object that contains records from a single table. See GlideRecord.|
|GlideElement|Use this class to operate on the fields of the current GlideRecord. See GlideElement.|
|GlideSystem|Use this class to get information about the system. See GlideSystem.|
|GlideAggregate|Use this class to perform database aggregation queries, such COUNT, SUM, MIN, MAX, and AVG, for creating customized reports or calculations in calculated fields. See GlideAggregate.|
|GlideDateTime|Use this class to perform date-time operations, such as date-time calculations, formatting a date-time, or converting between date-time formats. See GlideDateTime.|

|Class|Description|
|-----|-----------|
|GlideAjax|Use this class to execute server-side code from the client. See GlideAjax.|
|GlideDialogWindow|Use this class to display a dialog window. See GlideDialogWindow.|
|GlideForm|Use this class to customize forms. See GlideForm.|
|GlideList2|Use this class to customize \(v2\) lists, including normal lists and related lists. See GlideList2.|
|GlideMenu|Use this class to customize UI Context Menu items. See GlideMenu.|
|GlideUser|Use this class to get session information about the current user and current user roles. See GlideUser.|

-   **[Glide stack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/scripts/r_GlideStack.md)**  
Glide is an extensible Web 2.0 development platform written in Java that facilitates rapid development of forms-based workflow applications \(work orders, trouble ticketing, and project management, for example\).

**Parent Topic:**[Scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/scripts/c_Script.md)

