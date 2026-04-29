---
title: Add wearable devices assigned to employees
description: Add wearable devices such as Bluetooth LE-enabled devices that are assigned to employees to enable them to connect to the Wi-Fi network in your workplaces.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Retrieving Wi-Fi access log data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Add wearable devices assigned to employees

Add wearable devices such as Bluetooth LE-enabled devices that are assigned to employees to enable them to connect to the Wi-Fi network in your workplaces.

## Before you begin

The wearable device data is stored in the Wearable Technology \[cmdb\_ci\_wearable\] table. The table is installed with the CMDB CI Class Models application available on ServiceNow Store. Ensure that you have the CMDB CI Class Models application installed and active. For more information, see [CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-iot&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Role required: sn\_imt\_tracing.wifi\_manager

## About this task

You can also import your wearable devices data from an Excel spreadsheet. For more information, see [Easy import data from a list](https://www.servicenow.com/docs/access?context=c_EasyImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Wearables**.

2.  Click **New** to add details of a new device or select an existing device to edit.

3.  On the form, fill in the following fields required for contact tracing.

<table id="table_k4m_3mp_ylb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the wearable device.

</td></tr><tr><td>

Asset tag

</td><td>

Unique ID to identify the wearable device.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the employee who has the device.

</td></tr><tr><td>

Category

</td><td>

Category of the device.

</td></tr><tr><td>

MAC address

</td><td>

MAC address of the device.Follow the steps in [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) to add this field to the Wearables form.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Retrieving Wi-Fi access log data](../concept/wifi-access-management.md)

