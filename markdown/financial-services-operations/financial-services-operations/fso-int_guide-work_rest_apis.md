---
title: Working with ServiceNow REST APIs
description: FSO leverages the REST Table API to enable external sources, such as bank applications, to interact with the FSO data stored on a ServiceNow instance. The Table API provides endpoints that enable you to perform all CRUD operations \(create, read, update, and delete\) on your FSO centric tables from an external source.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Working with ServiceNow REST APIs

FSO leverages the REST Table API to enable external sources, such as bank applications, to interact with the FSO data stored on a ServiceNow instance. The Table API provides endpoints that enable you to perform all CRUD operations \(create, read, update, and delete\) on your FSO centric tables from an external source.

For example, you will use this API to locate customer records and query specific FSO information, such as customer credit cards, payments, and loans. For additional information on the available tables within FSO, see Financial Services Operations data model and the [FSO table definitions](../reference/fso-int_guide-table_defs.md).

You must ensure that the user that you use when calling these REST endpoints has the required roles assigned to them. The following are the roles required based on the table that you are trying to access:

-   Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   Financial Services Card Operations: sn\_bom\_card.admin and admin
-   Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin

For a list of all of the FSO roles and descriptions, see Components installed with Financial Services Operations Core.

## Test driving ServiceNow® REST APIs

The ServiceNow platform provides the [REST API Explorer](https://www.servicenow.com/docs/access?context=use-REST-API-Explorer&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US), which allows you to access the available REST APIs within your instance. Use this tool to interact with the various FSO tables within your instance before trying to implement the endpoint calls within your application.

