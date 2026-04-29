---
title: Create an entitlement for the legacy Software Asset Management plugin
description: You create software entitlements for both CIs and users from the same License Entitlement form.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software license entitlements for the legacy Software Asset Management plugin, Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create an entitlement for the legacy Software Asset Management plugin

You create software entitlements for both CIs and users from the same License Entitlement form.

## Before you begin

Role required: asset

## About this task

You can create these entitlements from the Asset Management application. Navigate to one of these locations and click **New**:

-   **Asset** &gt; **Software** &gt; **Asset License Entitlements**
-   **Asset** &gt; **Software** &gt; **User License Entitlements**

## Procedure

1.  Navigate to **Software Asset** &gt; **Software Licenses**.

2.  Click an **Asset tag**.

3.  Click **Add Entitlement** and complete the License Entitlement form using the fields in the table.

4.  Click **Submit**.

    The view returns to the Software License form.

5.  Set a condition in the **Allocated conditions** section.

    The configuration items given this license must meet the specified conditions. For example, you might set a condition that allocates this software license to CIs in a certain department only.

6.  Click **Update**.

    |Field|Description|
    |-----|-----------|
    |Display name|Name used in record lists.|
    |Assigned to|User of the entitlement token.|
    |Allocated to|The configuration item consuming the license token.|
    |Licensed by|License granting this token.|
    |Cached|Internal flag set and used by software counters.|


**Parent Topic:**[Software license entitlements for the legacy Software Asset Management plugin](t_CreatSWLicenseEntitlemnt.md)

