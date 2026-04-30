---
title: Add a property to enable creating knowledge article from incidents
description: Add a property, which is required to allow users to create a knowledge article from an incident.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Knowledge article creation from an incident, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a property to enable creating knowledge article from incidents

Add a property, which is required to allow users to create a knowledge article from an incident.

## Before you begin

Role required: admin

## Procedure

1.  In the Filter navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|enable\_kcs\_incident|
    |Description|Enable Knowledge Centered Services \(KCS\) for Incident Management.|
    |Type|true\|false|
    |Value|true|

4.  Click **Submit**.


**Parent Topic:**[Knowledge article creation from an incident](../concept/article-from-incident.md)

