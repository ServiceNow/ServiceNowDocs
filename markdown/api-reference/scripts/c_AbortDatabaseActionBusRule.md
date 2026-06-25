---
title: Abort a database action
description: You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_AbortDatabaseActionBusRule.html
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business rule use cases, Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Abort a database action

You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.

If the before business rule is executed during an insert action, and a condition in the script calls current.setAbortAction\(true\), the new record stored in current is not created in the database.

**Parent Topic:**[Business rule use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/useful-business-rules.md)

**Related topics**  


[GlideRecord - setAbortAction\(Boolean b\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideRecordAPI.md)

[Scoped GlideRecord - setAbortAction\(Boolean b\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md)

