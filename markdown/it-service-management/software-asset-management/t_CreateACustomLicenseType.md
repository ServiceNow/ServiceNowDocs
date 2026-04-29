---
title: Create a custom license type for the legacy Software Asset Management plugin
description: Custom license types in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin allow you to create a license type with special conditions.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [License calculations with the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create a custom license type for the legacy Software Asset Management plugin

Custom license types in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin allow you to create a license type with special conditions.

## Before you begin

Role required: sam

## About this task

A custom script can provide detailed information about the number of rights a software install or usage consumes.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **License Calculations**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the software license type.|
    |Query table|The value that is used for queries. This can be either **Software install** to count the number of installations or **Software usage** to count the number of times the software is used.|
    |Count by|The calculation type by which the license type counts software licenses. Make sure this value is set to **Custom** to create a new calculation type.|
    |Entitlement type|The entitlement type of the license, either **Workstation** or **User**. This field is available only when the **Count by** field is set to **Custom**.|
    |Script|The script used for custom license types. This field is available only when the **Count by** field is set to **Custom**.|

4.  Click **Submit**.


**Parent Topic:**[License calculations with the legacy Software Asset Management plugin](../concept/c_UseLicenseCalculations.md)

