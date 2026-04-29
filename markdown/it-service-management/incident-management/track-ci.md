---
title: Capture information on affected configuration items in an incident
description: Capture information on affected configuration items \(CIs\), with type as asset, in an incident to keep a record of the updated, repaired, swapped, or retired configuration items.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Capture information on affected configuration items in an incident

Capture information on affected configuration items \(CIs\), with type as asset, in an incident to keep a record of the updated, repaired, swapped, or retired configuration items.

## Before you begin

Role required: itil or admin

Activate the Hardware Asset Management Professional plugin \(com.sn\_hamp\).

## About this task

You can tell where the assets are located, by keeping track of the assets, how they are used, and when changes were made to them. This information helps you to monitor and manage the assets in your company using a systematic approach.

If you are not the caller of the incident and have a CI value in the affected CIs list, it is mandatory to provide information on the CI before changing the state of the incident to **Resolved**.

You can enter CI information either from the **Affected CIs** related list or from the form layout of the Affected CIs. You need to manually add the **Asset Action** and the **Swapped CI** fields in the related list.

<table id="table_uz4_lzw_clb"><thead><tr><th>

Where

</th><th>

How

</th></tr></thead><tbody><tr><td>

Related list

</td><td>

-   In the **Affected CIs** related list, click the settings icon ![Personalize list](../image/personalize-setting-list.png).
-   Move the **Asset Action** and the **Swapped CI** fields from the **Available** column to the **Selected** column.
-   Click **OK**.

</td></tr></tbody>
</table>**Note:** The CI value is updated only if the incident state is updated to **Resolved** by any user excluding the caller. The CI value is not updated if:

-   The incident state is updated as **Resolved** by the caller even if the **Asset Action** is populated.
-   The incident is directly moved to **Closed** state.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open an incident.

3.  Navigate to the **Affected CIs** related list before resolving the incident.

4.  If you want to enter information in the form layout, click the CI.

5.  On the related list or the form, fill in the fields.

<table id="table_prw_kpt_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset Action

</td><td>

Information on whether a CI is updated or repaired, swapped with another CI, or retired from the system. The options available are: No action, Update/Repair, Swap, and Retire.**Note:** If you swap or retire a CI, the sn\_hamp\_asset.swap or sn\_hamp\_asset.retire events are generated respectively.

</td></tr><tr><td>

Swapped CI

</td><td>

Information on the new CI that is swapped with the existing CI.**Note:**

-   This field appears only when you select the value of the **Asset Action** field as **Swap**.
-   The CI values available for swapped CI are the ones with asset CI class as hardware.
-   The Swapped CI is assigned to the Caller. If the Caller is an Asset Manager, they have the option to reassign it to the appropriate user.


</td></tr></tbody>
</table>6.  Click **Update**.

    The record is saved and the information about CI is stored in the \[task\_ci\] table.

    **Note:** You can filter the **Affected CIs** related list to have the list of affected CIs with class as Asset.


