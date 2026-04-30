---
title: Add a property to enable creating knowledge articles from HR cases
description: Add a property, which is required to allow users to create a knowledge article from an HR case.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable actionable knowledge feedback, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a property to enable creating knowledge articles from HR cases

Add a property, which is required to allow users to create a knowledge article from an HR case.

## Before you begin

Role required: admin

Ensure that the Developer Application is set to **Human Resources: Core**.

## Procedure

1.  In the Filter navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|enable\_kcs\_hr|
    |Description|Enable Knowledge Centered Services \(KCS\) for HR Service Delivery.|
    |Type|true\|false|
    |Value|true|

4.  Click **Submit**.


## Result

The property is added and you can now create knowledge articles from an HR case.

