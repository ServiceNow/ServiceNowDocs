---
title: Abort a database action
description: You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Business rule use cases, Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Abort a database action

You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.

If the before business rule is executed during an insert action, and a condition in the script calls current.setAbortAction\(true\), the new record stored in current is not created in the database.

**Parent Topic:**[Business rule use cases](useful-business-rules.md)

**Related topics**  


[GlideRecord - setAbortAction\(Boolean b\)](../../../app-store/dev_portal/API_reference/GlideRecord/concept/c_GlideRecordAPI.md#)

[Scoped GlideRecord - setAbortAction\(Boolean b\)](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)

