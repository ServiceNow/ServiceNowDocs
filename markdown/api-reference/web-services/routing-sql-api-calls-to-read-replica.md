---
title: Route SQL API calls to Read Replica
description: You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-15"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Route SQL API calls to Read Replica

You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.

## Before you begin

You must have a secondary database configured for your ServiceNow instance.

Role required: admin

## About this task

Query routing takes the load off the primary database for SELECT queries that take numerous DB CPU cycles on the primary DB. For more information, see [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441).

## Procedure

1.  Navigate to **All** &gt; **Secondary Database** &gt; **Secondary Database Category**.

2.  Select **New** to create a secondary database category for ODBC or JDBC.

3.  In the Name field, enter **odbc** or **jdbc**.

    Don't change any other field on this page. If you must change the default values, first refer to this KB: [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0824441](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441) ![UI screen example for creating secondary database category.](../image/sql-api-read-replica.png)

4.  Select **Map All Pools** to map the database pools to this category.

5.  Select the database pools to be added.

    The selected pools appear under the **Member Secondary Database Pools**.

6.  Select **Save**.


**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)

