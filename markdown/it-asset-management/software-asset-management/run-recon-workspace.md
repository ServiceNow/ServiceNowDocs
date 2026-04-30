---
title: Run software reconciliation in the workspace
description: Reconciliation is run as a scheduled job \(default is weekly\), but you can also run reconciliation manually to reconcile software products in the Software Asset Workspace environment on-demand.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Run software reconciliation in the workspace

Reconciliation is run as a scheduled job \(default is weekly\), but you can also run reconciliation manually to reconcile software products in the Software Asset Workspace environment on-demand.

## Before you begin

Reconciliation is run for products that have software entitlements or software installs. Grouping and subgrouping are supported so you can narrow the compliance results.

When running reconciliation manually, allow enough time for the process to complete. For faster results, narrow the scope by selecting specific publishers.

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to the Run Reconciliation dialog box from either of the two ways:

    -   **Software Asset Workspace** &gt; **Software asset overview** &gt; **Run Reconciliation**
    -   **Software Asset Workspace** &gt; **License usage** &gt; **Run Reconciliation**
    ![Run reconciliation process](../image/run-recon-workspace.png) ![]()

    **Note:** If domain separation is enabled on your instance, then the Domain filter drop-down appears in the Run Reconciliation dialog box.

2.  Select a particular publisher for which compliance should be calculated.

    You can also select all publishers.

3.  To narrow results further, select a group or subgroup.

    Available group and subgroup values include None, Country, Department, Company, Region, and Cost Center.

4.  Select **Run Reconciliation**.

    The reconciliation process may take some amount of time to complete. Once reconciliation is complete, the reconciliation results are shown in the **Reconciliation** tab.

<table id="table_lrw_slt_ty"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifying number that is generated during the reconciliation process.

</td></tr><tr><td>

Last reconciled

</td><td>

Date of last reconciliation run.

</td></tr><tr><td>

Status

</td><td>

Status of the reconciliation.-   Completed
-   In Progress
-   Failed


</td></tr><tr><td>

Ran for

</td><td>

All publishers, or specific publishers.

</td></tr><tr><td>

Publishers

</td><td>

Only shown if publishers were specified on which to run reconciliation.

</td></tr><tr><td>

Group

</td><td>

Group specified on which to run reconciliation. Values include **None**, **Country**, **Department**, **Company**, **Region**, and **Cost Center**.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup specified on which to run reconciliation. Values include **None**, **Country**, **Department**, **Company**, **Region**, and **Cost Center**.

</td></tr><tr><td>

Progress

</td><td>

Percent complete and progress bar for the reconciliation run.

</td></tr><tr><td>

Progress summary

</td><td>

Specific step within the reconciliation process.**Note:** This list column is not shown by default. You can personalize your list column settings to add it, if desired.

</td></tr><tr><td>

Updated

</td><td>

The date and time when the particular reconciliation process was completed.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

