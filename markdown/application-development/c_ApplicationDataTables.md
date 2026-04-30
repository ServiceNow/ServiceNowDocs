---
title: Application tables
description: Application developers create tables and their associated lists and forms for users to add and update records.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application tables

Application developers create tables and their associated lists and forms for users to add and update records.

An application owns its tables and determines whether other applications can access resources from them. For example, the Book Rooms application can store conference room data in the Conference Rooms \[x\_acme\_book\_rooms\_conference\_rooms\] table and permit other applications to read this data.

The system uses standard access controls to manage user access to application data. During application creation, developers can specify an application-specific user role for these access controls. They can also use application access settings to manage runtime and design time access to application tables.

**Note:** Certain ServiceNow AI Platform subscriptions include custom table entitlements. You can create custom tables for any purpose, up to the entitlement limit in the subscription. To learn more about how your usage administrator maps the custom tables that you create to subscriptions, see [Map custom tables to a product subscription in Subscription Management](https://www.servicenow.com/docs/access?context=allocate-custom-table-subsc-app-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Be aware of these database limitations:

-   The system can only have a maximum of 1000 columns per table. Although 1000 columns is a specified limit, this limit doesn't mean you can physically have 1000 columns within a table. The number of columns within a table is defined by the database used in the ServiceNow datacenter, not by the ServiceNow AI Platform.
-   Every table, regardless of storage engine, has a maximum row size of 65,535 bytes. Storage engines may place additional constraints on this limit, reducing the effective maximum row size.
-   The system can't have more than 10 medium-length or longer **String** fields to a single table. Attempting to save a large number of characters in 11 or more String fields can result in the following error: Syntax Error or Access Rule Violation detected by database \(Row size too large \(&gt; `8126`\).
-   When you create fields, the u\_ prefix is automatically added to the column name. If the column label that you enter contains leading numeric characters, they are replaced by the u\_ prefix.

For more information on database limitations and general questions on tables in your ServiceNow instance, see [KB0749585](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0749585).

**Related topics**  


[Application access settings](c_ApplicationAccessSettings.md)

