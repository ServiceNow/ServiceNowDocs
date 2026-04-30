---
title: Display field values as interaction record tab titles
description: Display field values, such as contact or consumer names, as titles on interaction record tabs in CSM Configurable Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Display field values as interaction record tab titles

Display field values, such as contact or consumer names, as titles on interaction record tabs in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

**Note:** This task applies to CSM Configurable Workspace.

Configure the **sessionTabTitle** property to identify the fields that can be used in interaction record tab titles. Enter fields in this property as a comma separated string.

The system evaluates these fields in the order that they appear in the string. The first field that has a value is used as the interaction record tab title. If none of the fields in the string have values, the system displays the record number as the tab title.

**Note:** Configured fields must appear on the interaction record.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences** &gt; **CSM/FSM Configurable Workspace**.

2.  In the UX Page Properties list, click the **sessionTabTitle** property.

3.  In the **Value** field, enter the fields to use in interaction record tab titles.

    Enter the fields as a comma separated string. The default string is **contact,consumer,number**.

    **Note:** Configured fields must appear on the interaction record.

4.  Click **Update**.


