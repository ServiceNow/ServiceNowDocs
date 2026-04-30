---
title: Add a software license using the legacy Software Asset Management plugin
description: You can add a new software license using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Add a software license using the legacy Software Asset Management plugin

You can add a new software license using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Software Licenses**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Display name|Read-only. Name of the software license. Created automatically.|
    |Model category|Model category for the software license. **Software License** is selected by default.|
    |Model|Software model of the license you are matching to. For example, Microsoft Excel.|
    |Rights|Number of entitlements to be granted by this license. If an enterprise contract is attached to the license, the Rights field does not display.|
    |General|
    |Asset tag|Number from the asset tag. The tag contains the serial number and bar code for tracking the software license.|
    |State|Current status of the software license, such as **On order** or **In use**.|
    |Assigned to|User currently assigned to this software license.|
    |Managed by|User or department that maintains the software license. Can be different than the owner. For example, a specified user can own a software license, but the IT department manages it.|
    |Owned by|User or department with financial ownership of the software license. Can be different than the manager.|
    |Parent|Parent asset of the software license, if any. For example, the parent asset of Microsoft Word software is often the Microsoft Office suite.|
    |Class|\[Read-only\] Automatically created as Software License.|
    |License metric|\[Optional\] A single metric which the software license is counted against.|
    |Serial number|Unique number assigned for identification.|
    |Substate|More details about the software license stage. The available substate settings depend on the **State** selected. For example, if you select the **Retired** state, the substate options available are **Disposed**, **Sold**, **Donated**, and **Vendor credit**.|
    |Location|Where the license will be used. For example, a specific site, country, or region.|
    |Department|Department of the person **Assigned to** this software license.|
    |Company|Company that created the software.|
    |Assigned|Date on which the software license was assigned.|
    |Installed|Date on which the software license was installed.|
    |Comments|Information about the software license that would be helpful for others to know.|

    For information about the fields in the **Financial** and **Contracts** sections of the form, see [Create assets](../concept/c_ManagingAssets.md#).

4.  Click **Submit**.


**Parent Topic:**[Software licenses in the legacy Software Asset Management plugin](../concept/c_SoftwareLicenses.md)

