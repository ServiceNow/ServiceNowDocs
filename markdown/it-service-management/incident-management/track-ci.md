---
title: Capture information on affected configuration items
description: Capture information about the asset configuration items \(CIs\) that are affected by an incident to keep a record of the CIs that are updated, repaired, swapped, or retired.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/track-ci.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Capture information on affected configuration items

Capture information about the asset configuration items \(CIs\) that are affected by an incident to keep a record of the CIs that are updated, repaired, swapped, or retired.

## Before you begin

Role required: itil or admin

The Hardware Asset Management Professional plugin \(com.sn\_hamp\) must be activated.

## About this task

Tracking assets shows where they're located, how they're used, and when they changed. This information helps you monitor and manage the assets in your organization.

If you aren't the incident caller and the Affected CIs related list contains a CI, provide CI information before changing the incident state to **Resolved**.

You can enter CI information either from the **Affected CIs** related list or from the form layout of the Affected CIs. You need to manually add the **Asset Action** and the **Swapped CI** fields in the related list.

<table id="table_uz4_lzw_clb"><thead><tr><th>

Where

</th><th>

How

</th></tr></thead><tbody><tr><td>

Related list

</td><td>

-   In the **Affected CIs** related list, select the settings icon \[Omitted image "personalize-setting-list.png"\] Alt text: Personalize list.
-   Move the **Asset Action** and the **Swapped CI** fields from the **Available** column to the **Selected** column.
-   Select **OK**.

</td></tr></tbody>
</table>**Note:** The CI value is updated only if the incident state is updated to **Resolved** by any user other than the caller. The CI value isn't updated if:

-   The incident state is set to **Resolved** by the caller, even if the **Asset Action** field is populated.
-   The incident is moved directly to the **Closed** state.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open an incident.

3.  Navigate to the **Affected CIs** related list before resolving the incident.

4.  To enter information in the form layout, select the CI.

5.  On the related list or the form, fill in the fields.

<table id="table_prw_kpt_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset Action

</td><td>

Information on whether a CI is updated or repaired, swapped with another CI, or retired from the system. The options available are: No action, Update/Repair, Swap, and Retire.**Note:** If you swap or retire a CI, the **sn\_hamp\_asset.swap** or **sn\_hamp\_asset.retire** events are generated respectively.

</td></tr><tr><td>

Swapped CI

</td><td>

Information on the new CI that is swapped with the existing CI.**Note:**

-   This field appears only when **Swap** is selected from the **Asset Action** field.
-   Only CIs with the hardware asset CI class are available to swap.
-   The swapped CI is assigned to the caller. If the caller is an asset manager, they can reassign it to the appropriate user.


</td></tr></tbody>
</table>6.  Select **Update**.

    The record is saved and the information about CI is stored in the \[task\_ci\] table.

    **Note:** You can filter the **Affected CIs** related list to show only the affected CIs with the Asset class.


