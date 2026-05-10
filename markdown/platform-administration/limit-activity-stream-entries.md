---
title: Limit the number of activity stream entries
description: You can set a system property to limit the number of entries allowed in an activity stream.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Limit the number of activity stream entries

You can set a system property to limit the number of entries allowed in an activity stream.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the Navigation filter.

2.  Search for the property **glide.history.max\_entries**.

3.  Edit the **Value** property to set the maximum number of entries that users can view in an activity stream.

    **Note:** New entries do not count towards the max number until the form is refreshed.

    |Option|Description|
    |------|-----------|
    |Name|glide.history.max\_entries|
    |Description|Maximum number of entries allowed to display in an activity stream. The default number is 250. New entries do not count towards the max number until the form is refreshed.|
    |Type|integer|
    |Default value|250|


**Parent Topic:**[Using formatters](../concept/c_Formatters.md)

**Related topics**  


[Create a UI macro for a formatter](t_CreateAUIMacro.md)

[Create a formatter and add it to a form](t_CreateAFormatter.md)

