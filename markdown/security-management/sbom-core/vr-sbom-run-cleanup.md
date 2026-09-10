---
title: Configure rules and run an SBOM cleanup job
description: Create and run a one-time cleanup rule to permanently purge older SBOM records that match the conditions you specify.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sbom-core/vr-sbom-run-cleanup.html
release: zurich
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 3
breadcrumb: [Removing older SBOM records, Uploading and viewing your SBOM files in the SBOM Workspace, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Configure rules and run an SBOM cleanup job

Create and run a one-time cleanup rule to permanently purge older SBOM records that match the conditions you specify.

## Before you begin

The SBOM Response application is required to access the SBOM cleanup module.

**Warning:**

Pause all SBOM uploads and any data imports before you run a cleanup job to avoid potential conflicts.

Role required: sn\_sbom\_core.admin

## About this task

## Procedure

1.  Navigate to **SBOM Workspace** &gt; **Configuration** &gt; **SBOM cleanup**.

2.  Select **Create cleanup run** if this is the first cleanup rule for your instance, or **New Cleanup run** if one or more cleanup runs already exist.

    Only one cleanup can run at a time. If you submit a new cleanup while another is in progress, the new cleanup is queued and runs after the current one completes.

3.  In the SBOM cleanup dialog, fill out the fields to you want to use to define the cleanup scope.

<table id="table_vr_sbom_run_cleanup"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Delete SBOMs older than \***

</td><td>

Select the minimum age of the records to delete: **90 days**, **180 days**, **1 year**, or **2 year**. Record age is calculated using the SBOM creation date.

</td></tr><tr><td>

**Include all associated Product models and Business applications in the cleanup**

</td><td>

Selected by default. When selected, all product models and business applications that match your age condition are included in the cleanup.

 Deselect the **Product models to exclude** and **Business applications to exclude** fields to preserve specific product models or business applications.

</td></tr><tr><td>

**Product models to exclude**

</td><td>

Available when **Include all associated Product models and Business applications in the cleanup** is deselected. Add one or more product models, for example `glibc`, to preserve from the cleanup.

</td></tr><tr><td>

**Business applications to exclude**

</td><td>

Available when **Include all associated Product models and Business applications in the cleanup** is deselected. Add one or more business applications, for example `production-api`, `payments-core`, or `HR Portal`, to preserve from the cleanup.

</td></tr></tbody>
</table>4.  Select **Run cleanup**.

5.  On the Review cleanup details modal, review the cleanup summary, including the age threshold, cleanup scope, and any excluded product models or business applications.

    Select **Back** to return to the previous dialog and modify the scope, or **Cancel** to exit without running the cleanup.

    **Danger**

    Cleanup runs are permanent and can't be undone. Deleted SBOM records can't be restored. Review the cleanup scope and exclusions carefully before running a cleanup.

6.  Select **Run cleanup** to submit the cleanup run.

    A confirmation modal indicates that your cleanup run was submitted. The cleanup run is queued and runs in the background. Completion time varies based on the number of records being processed. Select **Ok, got it** to close the dialog.

    You can monitor the progress of your cleanup run in the **Cleanup runs** table on the SBOM cleanup page. The table includes the following information.

<table id="table_result_vr_sbom_run_cleanup"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created on

</td><td>

Date and time the cleanup run was submitted.

</td></tr><tr><td>

Created by

</td><td>

User who submitted the cleanup run.

</td></tr><tr><td>

Delete SBOMs older than

</td><td>

Age threshold specified for the cleanup run.

</td></tr><tr><td>

Cleanup scope

</td><td>

Activated by default. When selected, all product models and business applications that match your age setting are removed.

 Deselect the check box and list the product models and business applications that fall within your age setting that you want skipped during the cleanup.

</td></tr><tr><td>

Status

</td><td>

Current state of the cleanup run, for example `In progress`

 **Note:** If you select **New cleanup run** in the Review cleanup details modal while a run is currently in process, your new run is displayed with the `Queued` state.

</td></tr><tr><td>

SBOM deleted

</td><td>

Number of SBOM records deleted so far out of the total number of records matched by the cleanup conditions, for example `20/2500`.

</td></tr></tbody>
</table>    While a cleanup run is queued, you can select **Cancel queued run** to cancel it before it starts.

7.  To cancel a queued cleanup run, select a run in the `Queued` state from the list at **SBOM Workspace** &gt; **Configuration** &gt; **SBOM cleanup** and select **Cancel queued cleanup run**.

    The cleanup run transitions from `Queued` to `Cancelled`. You can cancel a scheduled job while another job is running.


