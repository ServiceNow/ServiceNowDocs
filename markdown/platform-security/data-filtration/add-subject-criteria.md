---
title: Add subject attributes to your data filtration rule
description: Optionally, use subject attributes to narrow the scope of your data filtration rule based on attributes such as IP network address, user groups and roles, or subject criteria.
locale: en-US
release: yokohama
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating data filtration rules, Data filtration\(Legacy\), Access Management]
---

# Add subject attributes to your data filtration rule

Optionally, use subject attributes to narrow the scope of your data filtration rule based on attributes such as IP network address, user groups and roles, or subject criteria.

## Before you begin

Role required: admin

## Procedure

1.  On your data filtration record, open the **Subject Criteria** tab.

2.  Use the condition builder to filter the table records based on one or more of the following criteria.

    |Option|Description|
    |------|-----------|
    |Network Criteria|Allows access to records based on network IP range or IP subnet.|
    |Subject Criteria|Allows access to records based on subject criteria. Select a subject criteria record to apply it's conditions to your data filtration rule. For details on creating subject criteria records, see [Creating subject criteria](df-create-criteria.md).|
    |Subject Group|Allow access if the user is a member of a specific group. Select a group from the **Groups**\[sys\_user\_group\] table.|
    |Subject Role|Allow access if the user is a member of a specific group. Select a group from the **Roles**\[sys\_user\_role\] table.|

    **Important:** Subject criteria conditions only support the **is** operator.

3.  After adding your subject criteria click **Save**.


