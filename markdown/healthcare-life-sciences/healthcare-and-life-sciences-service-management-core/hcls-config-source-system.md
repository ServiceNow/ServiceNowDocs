---
title: Configure an external Redox healthcare system as a source system for a custom integration
description: Enable a custom integration application to exchange data with an external Redox healthcare system by configuring the source and destination IDs of the healthcare system in your ServiceNow instance.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure an external Redox healthcare system as a source system for a custom integration

Enable a custom integration application to exchange data with an external Redox healthcare system by configuring the source and destination IDs of the healthcare system in your ServiceNow instance.

## Before you begin

Role required: sn\_hcls.admin or admin

## About this task

As a healthcare provider, you can store the source and destination IDs of an external healthcare system in the [Source system \[sn\_hcls\_source\_system\]](../reference/hcls-source-system.md) table for a custom integration with a ServiceNow application.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the **Name** column of the Tables list, search for `sn_hcls_source_system`.

3.  Select **Source system** from the **Label** column.

4.  Click the **Show Form** related link.

5.  On the form, fill in the fields.

<table id="table_mbn_w11_ftb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source ID

</td><td>

ID of the external Redox healthcare system used for processing an inbound API response from the system to your ServiceNow instance.

</td></tr><tr><td>

Destination ID

</td><td>

ID of the external Redox healthcare system used for sending an outbound API request to the system from your ServiceNow instance.

</td></tr><tr><td>

Source

</td><td>

Name to identify the external Redox healthcare system as a source system in your ServiceNow instance.

</td></tr></tbody>
</table>6.  Click **Submit**.


