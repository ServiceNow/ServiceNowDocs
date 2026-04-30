---
title: Assign records to an assignment group in bulk
description: Assign multiple records findings concurrently to an assignment group using the bulk edit feature in the Security Exposure Management Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Assign records to an assignment group in bulk

Assign multiple records findings concurrently to an assignment group using the bulk edit feature in the Security Exposure Management Workspace.

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
    -   Configuration Test Results
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the **Only Selected Items** option in the [Record selection](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-assign.md#record-slection-field-assign) field.
    -   Apply filters if you want to use the **All records that match filter** option in the [Record selection](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-assign.md#record-slection-field-assign) field.
4.  Select the **Bulk Edit** button.

5.  On the form, fill in the fields to assign the records to an assignment group.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td id="record-slection-field-assign">

Record Selection

</td><td>

Records to update. Choices are:-   Only Selected Items: Select this option if you want to update the records you selected using the check box.
-   All records that match filter: Select this option if you want to update the filtered records.
-   Remediation Task: Select this option if you want to update the records in a remediation task and then select the desired remediation task in the **Remediation task** field.
-   Vulnerability Entry: Select this option if you want to update the records specific to a vulnerability and then select a CVE or TPE in the **Vulnerability Entry** field.

**Note:** This field appears for host vulnerable items, application vulnerable items, and container vulnerable items.

-   Configuration test: Select this option if you want to update the test results specific to a test and then select a test in the **Configuration test** field.

**Note:** This option appears for Configuration test results only.

**Note:**

-   Records with invalid CI or CI decommissioned aren’t updated.
-   Only the records in the Open, Under Investigation, Awaiting Implementation or Deferred state are updated.


</td></tr><tr><td>

Assignment group

</td><td>

Assignment group for the records. All the active assignment groups appear in this field.**Note:** This field is deactivated when you select the Unassign check box for VITs.

</td></tr><tr><td>

Work notes

</td><td>

Text that you enter to describe the changes.

</td></tr></tbody>
</table>6.  Click  **Edit**.


## Result

Open a record for which you updated the assignment group and navigate to the Overview tab, the user group to which the record is assigned appears in the **Assignment group** field.

