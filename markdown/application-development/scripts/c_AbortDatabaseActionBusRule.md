---
title: Abort a database action
description: You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Business rule use cases, Useful scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Abort a database action

You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.

If the before business rule is executed during an insert action, and a condition in the script calls current.setAbortAction\(true\), the new record stored in current is not created in the database.

**Parent Topic:**[Business rule use cases](useful-business-rules.md)

