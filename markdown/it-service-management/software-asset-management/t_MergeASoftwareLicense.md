---
title: Merge software licenses using the legacy Software Asset Management plugin
description: If you have multiple software licenses that are linked to the same model, you can merge the individual licenses into a consolidated license using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Merge software licenses using the legacy Software Asset Management plugin

If you have multiple software licenses that are linked to the same model, you can merge the individual licenses into a consolidated license using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## About this task

To be merged, the individual licenses must meet the following requirements:

-   The licenses cannot already be merged into another consolidated license.
-   The information in the following fields must match for each license:
    -   Model
    -   Allocated condition
    -   Assigned condition
    -   Company
    -   Location
    -   Department
    -   Cost center
    -   State
-   The licenses must have the same set of software upgrades and downgrades and the same set of assets covered. To verify this information, go to **Software Asset** &gt; **Software Licenses** and select a license.
    -   For upgrades and downgrades, go to the **Software Upgrade and Downgrades** related list.
    -   For assets covered, go to the **Assets Covered** embedded list in the Contracts related list.

If a license can be merged, **Merge with similar licenses** appears under **Related Links** on the Software License form.

To merge a license:

## Procedure

1.  Open a license.

2.  Click the **Merge with similar licenses** link.

    Displays a dialog box with a message stating that the merge process is irreversible and that license keys are not merged.

3.  Click **OK**.

    All qualifying licenses, including the current license, are merged into a new consolidated license. An informational message appears until the user is redirected to the newly merged license.

    All qualifying licenses are merged into a new consolidated license unless they can be matched to an existing consolidated license. If they are merged into a new consolidated license, the **Asset tag** field is cleared. After merging, the merged license is marked as **Is merged license** \(field = true\) and the **Merged into** field is set to this license for the consolidated licenses.

    **Note:** Licenses that are marked as merged are not counted.

    For the consolidated licenses:

    -   The number of rights are summed up into a new count.
    -   The asset and user entitlements are transferred to the new license.
    -   The expense lines and assets on contract rate cards are transferred to the new license.
    -   The set of software upgrades and downgrades, as well as the set of assets covered, are copied to the new license.
    -   The cost of each individual license is summed up into the new license using the system base currency.
    -   A history of the consolidated licenses and where they went is maintained.

**Parent Topic:**[Software licenses in the legacy Software Asset Management plugin](../concept/c_SoftwareLicenses.md)

**Related topics**  


[License management with the legacy Software Asset Management plugin](../concept/c_ManageSoftwareLicenses.md)

