---
title: View usage counter results for the legacy Software Asset Management plugin
description: Usage counters for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin track licenses based on how often those licenses are actually used either by a workstation or a user.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# View usage counter results for the legacy Software Asset Management plugin

Usage counters for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin track licenses based on how often those licenses are actually used either by a workstation or a user.

## Before you begin

Role required: sam

## About this task

A usage counter tracks a license based on how often the license is actually used either by a workstation or a user. For example, an asset manager can use a usage counter to determine who is actually using the software they have been entitled. If an individual is not using the software at all or very infrequently, the software can be uninstalled and given to an individual who will use it more often. If you have a way of capturing information, for example a proxy server or gateway, you can capture the IP address and the name of the user accessing the license. The captured data can be added directly into the Software Usages list.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Software Usages**.

2.  Click the **Display Name** in the row containing the software and user to check.

3.  View the **Software Usage** form \(see table\).

    All fields on the form are read-only.

    ![SAM software usage](../image/SAMSoftwareUsage.png "SAM software usage")

    |Field|Description|
    |-----|-----------|
    |Display name|Name of the software usage record.|
    |Publisher|Publisher of the software.|
    |Version|Version of the software.|
    |Discovery model|[Software discovery model](../concept/c_UsingSoftwareDiscoveryModels.md) associated with the installed software.|
    |Primary key|Unique identifier for table row.|
    |Usage|
    |User|User who accessed the software.|
    |Accessed from|Hardware configuration item from which the software was accessed.|
    |Last scanned|Date and time when the software was last discovered on this hardware.|
    |Duration|Duration of all usage.|
    |Times used|Number of times the software was accessed from this hardware.|
    |Last used|Date and time when the software was last used on this hardware.|
    |Software counter|
    |Counted by|The software counter summary record in the Software Counter Summary \[`sam_sw_counter_summary`\] table on which this usage is counted.|
    |Entitlement|The entitlement rights of the software.|
    |Valuation|Number of license rights used by this software usage.|
    |Cached|If selected, indicates that a software count has already been cached.|


**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

