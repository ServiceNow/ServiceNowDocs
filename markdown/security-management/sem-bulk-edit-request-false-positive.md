---
title: Bulk edit for false positive in the Security Exposure Management Workspace
description: Mark one or more records \(VITs, AVITs, CVITs, or TRs\) as false positive concurrently using the bulk edit feature from the Security Exposure Management Workspace instead of manually selecting each item.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit for false positive in the Security Exposure Management Workspace

Mark one or more records \(VITs, AVITs, CVITs, or TRs\) as false positive concurrently using the bulk edit feature from the Security Exposure Management Workspace instead of manually selecting each item.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

When you raise a false positive request for one or more records from the Bulk edit modal, a remediation task is created with the selected records.

**Note:** When you raise a false positive request for the Application Vulnerable Items \(AVITs\) using the bulk edit feature, the AVITs from the scanners with the **Manage False positive with Servicenow** parameter set to false are not updated.

-   If you select AVITs from various scanners, some with the **Manage False positive with Servicenow** parameter set to true and other set to false, the AVITs linked to the scanners with the **Manage False positive with Servicenow** parameter set to false are not updated.
-   If you select AVITs from only the scanners with the **Manage False positive with Servicenow** parameter set to false, the False positive option does not appear in the **Reason** field in the Bulk Edit modal.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **List**.

    **Note:** The selected records must be in the Open, Under Investigation, or Awaiting Implementation state.

2.  On the List page, open Active or All list in one of the following lists:

    -   Host Vulnerable items
    -   Container Vulnerable items
    -   Application Vulnerable items
    -   Configuration Test Results
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the Only Selected Items option in the [**Record selection**](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-request-false-positive.md#record-slection-field) field.
    -   Apply filters if you want to use the All records that match filter option in the [**Record selection**](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-request-false-positive.md#record-slection-field) field.
4.  Select the **Bulk Edit** button.

5.  On the form, fill in the fields to request false positive for multiple records.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td id="record-slection-field">

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
-   Only the records in the Open, Under Investigation, or Awaiting Implementation state are updated.


</td></tr><tr><td>

State

</td><td>

Select the **Closed** state.

</td></tr><tr><td>

Reason

</td><td>

Select the Reason as False positive.

**Note:**

-   When you select this option, the Short description, and Additional information fields appear.
-   A remediation task is created when you mark the records as False-positive and this task is sent for approval.
 **Note:** The **Reason** field appears when you select the State as Deferred or Closed.

</td></tr><tr><td>

Short description

</td><td>

Brief note describing the reasons for Closed-False positive request. This information reflects in the **Description** field of the remediation task that is created for a Closed-False positive request.**Note:** This field appears when you select the State as Deferred or Closed-False positive.

</td></tr><tr><td>

Additional information

</td><td>

Any other necessary information. This information reflects in the Additional Information field in the Overview tab of the remediation task that is created for Closed-False positive request. If your false positive request is approved, this additional information appears as notes for both VIT and remediation task.**Note:** This field appears when you select the State as Deferred or Closed-False positive.

</td></tr><tr><td>

Work notes

</td><td>

Text that you enter to describe the changes.

</td></tr></tbody>
</table>6.  Click  **Edit**.

7.  On the Take Questionnaire modal, answer the questions and select **Submit**.

    A remediation task is created with the selected records. Your request is submitted for approval and the State of the remediation task changes to  In Review.

    **Note:** The **Take Questionnaire** modal appears only when the questionnaire is enabled for false positive requests in the Exception Management form. For more information on configuring a questionnaire for false positive requests, see [Configure Exception Management for Vulnerability Response](../../vulnerability-response/task/configure-exception-management-settings.md), [Configure Exception Management for Application Vulnerability Response](../../vulnerability-app-vuln-mgmt/task/configure-exception-management-application-vulnerability-response.md), and [Configure Exception Management for Container Vulnerability Response](../../container-vulnerability-response/task/configure-exception-management-for-container-vulnerability-response.md).

    The approver receives an email notification about your request.


## Result

In the Security Exposure Management Workspace, on the List page, navigate to **Exceptions** &gt; **All**, open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

|Approval state|Result|
|--------------|------|
|Approved|The state of the Remediation Task transitions to Closed with the Reason as False positive. The state and reason are rolled down to the records.|
|Rejected|The state of the Remediation Task and its records doesn’t change.|

In the **Activity stream** of a record or remediation task, you can view the entire workflow of your request.

