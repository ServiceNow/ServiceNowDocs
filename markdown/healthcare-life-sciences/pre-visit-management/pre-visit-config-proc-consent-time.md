---
title: Configure when to send the procedure consent form to a patient
description: Configure the Pre-Visit Management application to when to send the procedure consent document for review and signature to a patient before the procedure appointment date.
locale: en-US
release: xanadu
product: Pre-Visit Management
classification: pre-visit-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Pre-Visit Management, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure when to send the procedure consent form to a patient

Configure the Pre-Visit Management application to when to send the procedure consent document for review and signature to a patient before the procedure appointment date.

## Before you begin

Set the application scope to Pre-Visit Management using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: sn\_previsit.admin or admin

## About this task

By default, the **Send procedure consent schedule** scheduled job is configured to automatically send the procedure consent document to a patient. The lead time when to send the document is set in the **sn\_previsit.procedure\_consent\_lead\_time** property. You can configure this property to specify when to send the procedure consent document to a patient.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_previsit.procedure\_consent\_lead\_time** property.

2.  In the **Value** field, enter a numeric value that indicates the number of days before the procedure appointment date when the procedure consent form is sent to the patient for review or signature.

3.  Click **Update**.


**Related topics**  


[Pre-Visit Management properties](../reference/pre-visit-properties.md)

