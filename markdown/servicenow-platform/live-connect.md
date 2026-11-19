---
title: Live Connect
description: Live Connect provides read-only SQL access to your ServiceNow tables. You can write queries, build reports, and analyze data in your existing tools while your security controls continue to apply.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/live-connect.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Live Connect

Live Connect provides read-only SQL access to your ServiceNow tables. You can write queries, build reports, and analyze data in your existing tools while your security controls continue to apply.

Live Connect queries data in place. Because external tools read directly from your instance, there is no data synchronization to schedule and no risk of reporting on a stale copy.

The Live Connect plugin \(SQL API\) uses ServiceNow web services support to provide a query-only interface. By default, the plugin supports only SELECT statements against authorized tables. It permits a limited set of additional SQL commands so that you can compose more complex queries and retrieve only the data you need.

External applications connect through ODBC and JDBC drivers. Any SQL-compatible reporting or analytics tool that can use those drivers can query authorized tables.

## What you need

To use Live Connect, your instance must run RaptorDB Professional, and the Live Connect plugin must be installed. Access is configured per user account, and the tables a query can reach are governed by the access controls already in place on your instance.

## Where to go next

For configuration and query syntax, see [Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md).

