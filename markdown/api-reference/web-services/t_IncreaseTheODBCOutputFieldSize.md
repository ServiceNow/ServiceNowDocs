---
title: Increase the field length in SQL queries
description: The ODBC driver limits the field length in SQL queries to the maximum length defined by the ServiceNow dictionary entry. You can increase the maximum field length to avoid truncating data.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ODBC behavior, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Increase the field length in SQL queries

The ODBC driver limits the field length in SQL queries to the maximum length defined by the ServiceNow dictionary entry. You can increase the maximum field length to avoid truncating data.

## Before you begin

Role required: admin

## About this task

If the data coming from the ODBC source exceeds the field size of the dictionary entry, ServiceNow truncates the query output to fit the field size. If your data is truncated, you can do the following.

## Procedure

1.  Increase the maximum length in the dictionary entry for the field in question.

2.  Reconnect the ODBC driver to pick up the change.

    **Note:** By default, the ODBC driver uses the VARCHAR data type to store query string output. When strings become very large \(roughly 16000 characters\), the ODBC driver uses the LONGVARCHAR data type instead. It is important to keep in mind, however, that the LONGVARCHAR data type has a more limited set of SQL commands that can be executed on it. For example, it does not support queries using scalar data.


**Parent Topic:**[ODBC behavior](../reference/r_ODBCBehavior.md)

