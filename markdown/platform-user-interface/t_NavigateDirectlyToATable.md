---
title: Navigate directly to a table
description: You can use commands in the navigation filter to navigate directly to the list, form, or configuration view of a table.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Navigate directly to a table

You can use commands in the navigation filter to navigate directly to the list, form, or configuration view of a table.

## Before you begin

Role required: none

## About this task

Commands work only for tables you are permitted to access.

**Note:** The table name must match the name in the dictionary entry for the table.

## Procedure

1.  In the navigation filter of the application navigator, enter one of the following commands.

    |Command|Behavior|
    |-------|--------|
    |&lt;table name&gt;.list|Opens the list view of the table in the same window or tab.|
    |&lt;table name&gt;.form or &lt;table name&gt;.do|Opens the form view of the table in the same window or tab.|
    |&lt;table name&gt;.config|Opens the configuration view \[personalize\_all.do\] of the table in the same window or tab.|
    |&lt;table name&gt;.filter|Opens an empty list view of the table in the same window or tab, so that you can apply filters without loading the list. This is helpful for large lists that take a long time to load.|

    For example, enter `change_request.form` to open a new change request.

    **Note:** You can also enter any of the commands above in uppercase to open the list or form in a new window or tab. For example, enter `change_request.FORM` to open a new change request in a new window or tab.

2.  In Core UI, press the Enter key.


**Parent Topic:**[Common UI elements](../../../use/common-ui-elements/topic/p_CommonUIElements.md)

