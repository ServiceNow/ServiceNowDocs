---
title: Create an assignment group
description: Create an Operational Technology \(OT\) specific assignment group to assign to OT incident records.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Create an assignment group

Create an Operational Technology \(OT\) specific assignment group to assign to OT incident records.

## Before you begin

Role required: admin

## About this task

The **Assignment Group** field in an OT incident record only shows assignment groups with the type OT. This helps separate Operational Technology \(OT\) and Information Technology \(IT\) incidents.

You can create OT-specific assignment groups that you want visible on an OT incident record.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the assignment group.|
    |Manager|Group manager or lead.|
    |Type|Category for this group. In the **Select target record** field, search for **OT** to add it to the type field.|
    |Group email|Group email distribution list or the email address of the point of contact.|
    |Parent|Other group that the group is a member of.|
    |Description|Description of the assignment group.|

4.  Select **Submit**.


## Result

Now, the OT-specific assignment group is visible on the incident record.

**Parent Topic:**[Configuring Operational Technology Incident Management](../concept/configuring-operational-technology-incident-mgt.md)

