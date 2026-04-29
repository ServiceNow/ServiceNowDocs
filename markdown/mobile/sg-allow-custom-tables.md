---
title: Allow or restrict access to custom tables in mobile data items
description: Use system properties to control whether custom tables are available when creating or modifying data items.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Allow or restrict access to custom tables in mobile data items

Use system properties to control whether custom tables are available when creating or modifying data items.

## Before you begin

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the Application Navigator to open a list of your system properties.

2.  Find the **subscription.custom\_table.enforce\_entitlement** system property.

3.  To permit access to custom tables for data items, set the **Value** field to `false`, otherwise, set the value to `true`.

    This system property is in the global scope. If you are not in the global scope, you see a prompt at the top of the page. Click the **here** link to edit the property.![Out of scope edit warning](../image/scope-edit-warning.png)

4.  Click **Update**.


