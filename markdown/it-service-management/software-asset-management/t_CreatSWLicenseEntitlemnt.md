---
title: Software license entitlements for the legacy Software Asset Management plugin
description: Software entitlements enable you to define the people or machines to which a specific, purchased software license is assigned.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software license entitlements for the legacy Software Asset Management plugin

Software entitlements enable you to define the people or machines to which a specific, purchased software license is assigned.

## Before you begin

Role required: asset

## About this task

Asset managers allocate a license to entitle a user or machine to use the license. For example, a company purchases a software license for 100 rights. The software entitlement specifies the 100 employees or machines that are rightfully assigned a license. If the ServiceNow Discovery tool is used and it finds the software installed on 200 machines, the asset manager can identify the employees or computers that have the software installed without a license. The asset manager can ask users to remove the software from their computers.

Built-in rules prevent entitling more licenses than have been purchased. License entitlements use specific software license asset tags. In addition to the mandatory asset tag, an individual person and a specific configuration item can be assigned.

The benefits of using software entitlements include the following.

-   If the overall license entitlement is exceeded, the asset manager can rapidly address the problem and return to compliant status by either removing unauthorized software or ordering more licenses.
-   If the license entitlement is not being used completely, the asset manager can respond by lowering the number of licenses purchased in the future.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Software** &gt; **Asset License Entitlements** and create a new record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Display name|Name used in record lists.|
    |Allocated to|The configuration item consuming the license token.|
    |Licensed by|License granting this token.|
    |Cached|Internal flag set and used by software counters logic.|

2.  Click **Submit**.


-   **[Create an entitlement for the legacy Software Asset Management plugin](t_CreateAnEntitlement.md)**  
You create software entitlements for both CIs and users from the same License Entitlement form.
-   **[Create a software user license entitlement for the legacy Software Asset Management plugin](t_CreateSWUserLicenseEntitlement.md)**  
You can entitle a user to use one of your software licenses.
-   **[Entitle a license to a configuration item using the legacy Software Asset Management plugin](t_EntitleLicenConfigItem.md)**  
Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to entitle a license to a configuration item, such as a computer or server, or a location, such as a city of building.
-   **[Entitle a license to a user or location using the legacy Software Asset Management plugin](t_EntitleALicenseToAUser.md)**  
Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to entitle a license to an individual user.

**Parent Topic:**[Software licenses in the legacy Software Asset Management plugin](../concept/c_SoftwareLicenses.md)

