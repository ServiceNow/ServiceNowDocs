---
title: Create a remediation task manually in the IT Remediation Workspace
description: Starting with v25.0.4 of Vulnerability Response, you can create remediation tasks manually from the Host vulnerable items, Application Vulnerable items, Container vulnerable items, and Configuration test results lists on the List page of IT Remediation Workspace.
locale: en-US
release: yokohama
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Create a remediation task manually in the IT Remediation Workspace

Starting with v25.0.4 of Vulnerability Response, you can create remediation tasks manually from the Host vulnerable items, Application Vulnerable items, Container vulnerable items, and Configuration test results lists on the List page of IT Remediation Workspace.

## Before you begin

Role required:

-   sn\_vul.write\_assigned or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_write\_assigned, or sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.writer\_assigned, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace** &gt; **List**.

2.  On the List page, open the Active or All list in one of the following lists:

    -   Host Vulnerable Items
    -   Application Vulnerable Items
    -   Container Vulnerable Items
    -   Configuration Test Results
3.  Select the check box of the records you want to update and then select the [Selected items](itr-ws-create-remediation-task.md#itr-crt-select-items) option in the Record selection field on the Create Remediation Task modal.

4.  Select **Create Remediation Task**.

5.  On the Create remediation task modal, fill in the following details.

<table id="table_o5m_1qc_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record selection

</td><td>

**Selected items**: Updates the selected records only.

</td></tr><tr><td>

Short description

</td><td>

Brief note about the remediation tasks.

</td></tr><tr><td>

Grouping criteria

</td><td>

Choices are:-   **Assignment group**: Records with same assignment group are grouped into one remediation task.
-   **Assignment group and configuration item**: Records with same assignment group and configuration item are grouped into one remediation task.
-   **Assignment group and vulnerability**: Records with same assignment group and vulnerability are grouped into one remediation task.
-   **Assignment group and risk rating**: Records with same assignment group and risk rating are grouped into one remediation task.


</td></tr><tr><td>

Managing records in other remediation tasks

</td><td>

Choices are:-   **Skip records for new remediation tasks**: No action is taken on the records that are part of other remediation tasks.
-   **Move to new remediation tasks**: Records that are part of other remediation tasks are transferred to new remediation tasks.
-   **Keep in both current and new remediation tasks**: Records that are part of other remediation tasks are kept in both old and new remediation tasks.


</td></tr></tbody>
</table>6.  Select **Create remediation task**.


## Result

Remediation tasks are created based on the grouping criteria. An email notification is sent to the remediation owners in the assignment group, informing them that a remediation task has been created and assigned to their group. For examples on how remediation tasks are created based on the grouping criteria and record management criteria, see [Examples for remediation task creation in the Vulnerability Manager Workspace and IT Remediation Workspace](../../vr-vulnerability-manager-workspace/reference/create-remediation-task-examples.md).

