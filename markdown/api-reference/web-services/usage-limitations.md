---
title: Usage limitations for Live Connect
description: Live Connect imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/usage-limitations.html
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Usage limitations for Live Connect

Live Connect imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.

## Live Connect query rate limit

Live Connect enforces a rate limit of 500 queries per hour per driver type \(ODBC and JDBC\) across all user accounts, and a 5-minute timeout for individual queries. These limits apply to all SQL queries that run through both ODBC and JDBC drivers. The limits help maintain optimal instance performance while providing reliable data access for BI and analytics tools.

When planning your Business Intelligence \(BI\) tool integrations and report schedules, consider this rate limit to confirm your queries complete successfully without interruption. If your use case requires higher query volumes, consider optimizing your queries to retrieve more data per request. Alternatively, spread queries across multiple user accounts \(personal or service accounts\) with appropriate access controls.

**Parent Topic:**[Live Connect reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/troubleshooting.md)

