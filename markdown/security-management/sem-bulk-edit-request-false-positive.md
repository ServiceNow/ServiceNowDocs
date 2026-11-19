---
title: Bulk edit for false positive in the Security Exposure Management Workspace
description: Mark one or more records \(VITs, AVITs, CVITs, or TRs\) as false positive concurrently using the bulk edit feature from the Security Exposure Management Workspace instead of manually selecting each item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sem-bulk-edit-request-false-positive.html
release: zurich
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

You can mark records as Closed-False positive in bulk as a remediation owner, vulnerability manager, or vulnerability analyst. The records that are updated depend on your persona:

-   Remediation owner: Only the records that are assigned to you or to your assignment groups are updated.
-   Vulnerability manager or vulnerability analyst: All the records that meet the conditions you specify in the Bulk Edit modal are updated.

**Note:** The options in the **Reason** field depend on your role and the record type:

-   Host vulnerable items: If you have the sn\_vul.remediation\_owner role but not the sn\_vul.close\_vi\_vg role, False positive is the only reason available.
-   Application vulnerable items: If you have the sn\_vul.app\_security\_champion role but not the sn\_vul.app\_write\_all role, False positive is the only reason available.
-   Container vulnerable items and configuration test results: False positive is the only reason available for all users.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **List**.

    **Note:** The selected records must be in the Open, Under Investigation, or Awaiting Implementation state.

2.  On the List page, open Active or All list in one of the following lists:

    -   Host Vulnerable items
    -   Container Vulnerable items
    -   Application Vulnerable items
    -   Configuration Test Results
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the Only Selected Items option in the [**Record selection**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/vmws-bulk-edit-request-false-positive.md) field.
    -   Apply filters if you want to use the All records that match filter option in the [**Record selection**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/vmws-bulk-edit-request-false-positive.md) field.
4.  Select the **Bulk Edit** button.

5.  On the form, select **Closed** in the **State** field, and select **False Positive** as the **Reason** to request false positive for multiple records.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception-form.md).

6.  Select **Update**.

    **Note:** If you have configured Questionnaire for false positive requests, this button is labeled **Go to Questionnaire** instead.

7.  On the Take Questionnaire modal, answer the questions and select **Submit**.

    A remediation task is created with the selected records. Your request is submitted for approval and the State of the remediation task changes to  In Review.

    **Note:** The **Questionnaire** modal appears only when the questionnaire is enabled for exception requests in the Exception Management form.

    -   For more information on configuring a questionnaire for exception requests, see [Configure Exception Management for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-response/configure-exception-management-settings.md), [Configure Exception Management for Application Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/application-vulnerability-response/configure-exception-management-application-vulnerability-response.md), and [Configure Exception Management for Container Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/container-vulnerability-response/configure-exception-management-for-container-vulnerability-response.md), and [Configuration Compliance Exception Management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/configuration-compliance/cc-ex-mgmt.md).
    -   In case you must modify your questionnaire, refer to KB2713229.
    The approver receives an email notification about your request.


## Result

In the Security Exposure Management Workspace, on the List page, navigate to **Exceptions** &gt; **All**, open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

|Approval state|Result|
|--------------|------|
|Approved|The state of the Remediation Task transitions to Closed with the Reason as False positive. The state and reason are rolled down to the records.|
|Rejected|The state of the Remediation Task and its records doesn’t change.|

In the **Activity stream** of a record or remediation task, you can view the entire workflow of your request.

**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

**Related topics**  


[Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception-form.md)

