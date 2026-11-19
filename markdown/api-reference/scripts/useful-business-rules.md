---
title: Business rule use cases
description: Use cases for business rules include aborting a database action and restricting record access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/scripts/useful-business-rules.html
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Business rule use cases

Use cases for business rules include aborting a database action and restricting record access.

-   **[Abort a database action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_AbortDatabaseActionBusRule.md)**  
You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.
-   **[Restricting record access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_ExScptDftBfrQryBsnRu.md)**  
You can use a query business rule that executes before the database query to prevent users from accessing certain records.

**Parent Topic:**[Useful scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/usefulScripts.md)

