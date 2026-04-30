---
title: Map handheld computing devices assigned to employees
description: Map handheld computing devices that are assigned to employees and running the Zebra MotionWorks software to record proximity logs for contact tracing using those devices.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Map handheld computing devices assigned to employees

Map handheld computing devices that are assigned to employees and running the Zebra MotionWorks software to record proximity logs for contact tracing using those devices.

## Before you begin

Handheld computing device data is stored in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table. The table is installed with the CMDB CI Class Models application available on the ServiceNow Store. Ensure that you have that application installed and active. For more information, see [CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-iot&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Role required: sn\_imt\_tracing.wearable\_manager

## About this task

You can also import your handheld computing devices data from an Excel spreadsheet that you use with the Zebra MotionWorks software. For more information, see [Easy import data from a list](https://www.servicenow.com/docs/access?context=c_EasyImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Handheld Devices**.

2.  Click **New**.

3.  On the form, fill in the following fields required for contact tracing.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the handheld computing device.|
    |Asset tag|Unique ID to identify the handheld computing device.|
    |Serial number|Unique serial number of the handheld computing device.|
    |Assigned to|Name of the employee who has the handheld computing device.|

4.  Click **Submit**.


## Result

A mapping of the handheld computing device and the employee to whom it is assigned is created.

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

