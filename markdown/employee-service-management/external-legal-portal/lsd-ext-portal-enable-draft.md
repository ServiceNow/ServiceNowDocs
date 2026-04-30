---
title: Enable save as draft option for record producer
description: Enable the Save as Draft option for a record producer.
locale: en-US
release: xanadu
product: External Legal Portal
classification: external-legal-portal
topic_type: task
last_updated: "2025-01-10"
reading_time_minutes: 1
breadcrumb: [Configuring up External Legal Service Center, External Legal Service Center, Legal Service Delivery, Employee Service Management]
---

# Enable save as draft option for record producer

Enable the **Save as Draft** option for a record producer.

## Before you begin

Role required: sn\_lg\_ext\_portal.ext\_config

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `glide.sc.enable.save_as_draft.portal.elp` property.

    For more information on the system property, see [Property installed with External Legal Service Center](../reference/lsd-ext-portal-properties.md).

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field to `true`.

6.  Select **Update**.


