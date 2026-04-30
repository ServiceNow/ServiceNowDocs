---
title: Update the state of records in bulk in the Security Exposure Management Workspace
description: Update the state of multiple findings concurrently according to their remediation progress using the bulk edit feature in the Security Exposure Management Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Update the state of records in bulk in the Security Exposure Management Workspace

Update the state of multiple findings concurrently according to their remediation progress using the bulk edit feature in the Security Exposure Management Workspace.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **List**.

2.  On the List page, open the Active or All list in one of the following lists:

    -   Host Vulnerable items
    -   Container Vulnerable items
    -   Application Vulnerable items
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the **Only Selected Items** option in the **Record Selection** field.
    -   Apply filters if you want to use the **All Vulnerable Items that match filter** option in the **Record Selection** field.
4.  Select the **Bulk Edit** button.

5.  On the Bulk Edit modal, fill in the following fields to update the state of the records.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td id="record-slection-field">

Record Selection

</td><td>

Records to update. Choices are:-   Only Selected Items: Select this option if you want to update the records you selected using the check box.
-   All Vulnerable Items that match filter: Select this option if you want to update the filtered records.
-   Remediation Task: Select this option if you want to update the records in a remediation task and then select the desired remediation task in the **Remediation task** field.
-   Vulnerability Entry: Select this option if you want to update the records specific to a common vulnerable entry \(CVE\) and then select the CVE in the **Vulnerability Entry** field.
**Note:** Records with invalid CI or CI decommissioned aren’t updated.

</td></tr><tr><td>

State

</td><td>

Change for the **State** in the record. Choices are:-   Do Not Update
-   Open
-   Under Investigation
-   Awaiting Implementation
-   Deferred

For more information, see[Request bulk exception in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-request-exception.md).

-   Closed

For more information, see [Bulk edit for false positive in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-request-false-positive.md)

-   Resolved
**Note:** Only the records for which the state transition is valid are updated.

</td></tr><tr><td>

Work notes

</td><td>

Text that you enter to describe the changes.

</td></tr></tbody>
</table>6.  Select  **Edit**.

    A bulk edit asynchronous job updates the selected records.


**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](../concept/sem-using-bulk-edit.md)

