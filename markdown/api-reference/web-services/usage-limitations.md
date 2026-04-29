---
title: Usage Limitations for SQL API
description: The SQL API imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.
locale: en-us
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Usage Limitations for SQL API

The SQL API imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.

## SQL API query rate limit

The SQL API enforces a rate limit of 500 queries per hour per driver type \(ODBC and JDBC\) across all Service Accounts. This limit applies to all SQL queries executed through both ODBC and JDBC drivers and helps maintain optimal instance performance while providing reliable data access for business intelligence and analytics tools.

When planning your BI tool integrations and report schedules, consider this rate limit to confirm your queries complete successfully without interruption. If your use case requires higher query volumes, consider optimizing your queries to retrieve more data per request or spreading queries across multiple Service Accounts with appropriate access controls.

**Parent Topic:**[SQL API reference information](troubleshooting.md)

