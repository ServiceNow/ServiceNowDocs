---
title: Configure the display limit of iterations in EAP Backlog
description: Create a system property to modify the limit on the number of iterations displayed for an EAP Team in its Backlog in Enterprise Agile Planning \(EAP\).
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure the display limit of iterations in EAP Backlog

Create a system property to modify the limit on the number of iterations displayed for an EAP Team in its Backlog in Enterprise Agile Planning \(EAP\).

## Before you begin

Ensure the application scope in your instance is set to **Strategic Planning**.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

By default, the number of iterations shown in the Backlog page for an EAP Team is 6. If your organization's processes require more iterations to be displayed in the Backlog, create a system property **sn\_apw\_advanced.eap\_backlog\_iterations\_limit** and update the display limit.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Suffix|**sn\_apw\_advanced.eap\_backlog\_iterations\_limit**|
    |Type|Integer|
    |Value|Desired maximum number of iterations in the Backlog|

    For information on the other form fields, see the field description table in [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

4.  Select **Submit**.


