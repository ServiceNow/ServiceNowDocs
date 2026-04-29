---
title: Create application restricted caller access for provider application
description: Create restricted caller access \(RCA\) privilege for the provider application to allow inbound updates to Workplace case or task.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup Integrated Facilities Management Integration Framework, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create application restricted caller access for provider application

Create restricted caller access \(RCA\) privilege for the provider application to allow inbound updates to Workplace case or task.

## Before you begin

Role required: admin

## About this task

You can create application‑restricted caller access limited to inbound updates, allowing FM providers to update fields or add comments on Workplace cases or tasks.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Source Scope|Scope of the calling application. Select the application from the list.|
    |Application|Scope of the ServiceNow application where this routing rule applies. This field is automatically set to Workplace Case Management.|
    |Source Type|Type of record that is calling the application resource. Select **Scope**.|
    |Target Scope|Scope of the requested resource. Select **Workplace Case Management**.|
    |Status|Status of the access request. Select **Allowed**.|
    |Target Type|Type of the requested resource. Select **Scope**.|
    |Description|The reason for access from the source to the target.|

4.  Select **Submit**.


