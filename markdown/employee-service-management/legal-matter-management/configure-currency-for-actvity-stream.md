---
title: Configure the currency symbol for activity stream
description: Configure currency to be displayed in the activity stream.
locale: en-US
release: xanadu
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Legal Matter Management to engage with outside counsel using Legal Tracker, Setting up Legal Matter Management, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Configure the currency symbol for activity stream

Configure currency to be displayed in the activity stream.

## Before you begin

Role required: sn\_lg\_ops.legal\_config

## About this task

By default, the activity stream displays currency and price fields converted into the user's session locale. Configure the system property `glide.sys.audit_currency_value` to view the currency and price fields as in the value field.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `glide.sys.audit_currency_value` property.

3.  Select the property.

4.  Update the **Value** field to `true`.

5.  Select **Update**.


**Parent Topic:**[Configure Legal Matter Management to engage with outside counsel using Legal Tracker](../concept/configurations-for-legal-tracker-integration.md)

