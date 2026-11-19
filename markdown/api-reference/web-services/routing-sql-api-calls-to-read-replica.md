---
title: Route Live Connect calls to Read Replica
description: Route Live Connect calls to a Read Replica database to reduce the processing load on the primary database in your ServiceNow instance.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/routing-sql-api-calls-to-read-replica.html
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Route Live Connect calls to Read Replica

Route Live Connect calls to a Read Replica database to reduce the processing load on the primary database in your ServiceNow instance.

## Before you begin

A secondary database must be configured for your ServiceNow instance.

Role required: admin

## About this task

Query routing directs SELECT queries to a Read Replica database instead of the primary database, reducing the processing load on the primary database. For more information, see [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441) \(KB0824441\).

## Procedure

1.  Navigate to **All** &gt; **Secondary Database** &gt; **Secondary Database Category**.

2.  Select **New**.

    This creates a secondary database category for ODBC/JDBC.

3.  In the **Name** field, enter **odbc** or **jdbc**.

    **Warning:** Don't change any other field on this form. If you must change the default values, review the [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441) \(KB0824441\) article in the Now Support Knowledge Base before making changes.

4.  Select **Map All Pools**.

    This maps the database pools to this category.

5.  Select the database pools to add.

    The selected pools appear in the **Member Secondary Database Pools** list.

6.  Select **Update**.


## Result

Live Connect SELECT queries are routed to the Read Replica database. The primary database handles only write operations.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configuring-sql-api.md)

