---
title: Usage Limitations for Live Connect
description: The Live Connect imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/usage-limitations.html
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Usage Limitations for Live Connect

The Live Connect imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.

## Live Connect query rate limit

The Live Connect enforces a rate limit of 500 queries per hour per driver type \(ODBC and JDBC\) across all Service Accounts. This limit applies to all SQL queries executed through both ODBC and JDBC drivers and helps maintain optimal instance performance while providing reliable data access for business intelligence and analytics tools.

When planning your BI tool integrations and report schedules, consider this rate limit to confirm your queries complete successfully without interruption. If your use case requires higher query volumes, consider optimizing your queries to retrieve more data per request or spreading queries across multiple Service Accounts with appropriate access controls.

**Parent Topic:**[Live Connect reference information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/troubleshooting.md)

