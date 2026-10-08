---
title: Request bulk exception in the Security Exposure Management Workspace
description: Request an exception for multiple findings concurrently using the bulk edit feature instead of manually selecting each record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-bulk-edit-request-exception.html
release: brazil
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 4
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Request bulk exception in the Security Exposure Management Workspace

Request an exception for multiple findings concurrently using the bulk edit feature instead of manually selecting each record.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

When you request an exception for one or more records from the Bulk edit modal, a remediation task is created with the selected records. The remediation task is created only when Deferred or Closed-false positive state is selected.

**Note:** The Application Vulnerable Items \(AVITs\) from the scanners with the **Manage exceptions in ServiceNow** parameter set to false aren't updated.

-   If you select AVITs from various scanners, some with the **Manage exceptions in ServiceNow** parameter set to true and other set to false, the AVITs linked to the scanners with he **Manage exceptions in ServiceNow** parameter set to false aren't updated.
-   If you select AVITs from only the scanners with the **Manage exceptions in ServiceNow** parameter set to false, the Defer option does not appear in the **State** field in the Bulk Edit modal.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  On the List page, open the Active or All list in one of the following lists:

    -   Host Vulnerable items
    -   Container Vulnerable items
    -   Application Vulnerable items
    -   Configuration Test Results
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the Only Selected Items option in the [Record selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-manager-workspace/vmws-bulk-edit-request-exception.md) field.
    -   Apply filters if you want to use the All records that match filter option in the [Record selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-manager-workspace/vmws-bulk-edit-request-exception.md) field.
4.  Select the **Bulk Edit** button.

5.  On the form, select **Deferred** in the **State** field, and select a **Reason** to request an exception for multiple findings \(VITs, AVITs, CVITs, or TRs\) simultaneously.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md).

6.  Select **Update**.

    **Note:** If you have configured Questionnaire for exception requests, this button is labeled **Go to Questionnaire** instead.

7.  On the Questionnaire modal, answer the questions and select  **Submit**.

    A remediation task is created containing the records that you selected. Your request is submitted for approval and the State of the records changes to  In Review.

    **Note:** The **Questionnaire** modal appears only when the questionnaire is enabled for exception requests in the Exception Management form.

    -   For more information on configuring a questionnaire for exception requests, see [Configure Exception Management for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-response/configure-exception-management-settings.md), [Configure Exception Management for Application Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/application-vulnerability-response/configure-exception-management-application-vulnerability-response.md), and [Configure Exception Management for Container Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/container-vulnerability-response/configure-exception-management-for-container-vulnerability-response.md), and [Configuration Compliance Exception Management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/configuration-compliance/cc-ex-mgmt.md).
    -   In case you must modify your questionnaire, refer to KB2713229.
    The approver receives an email notification about your request.


## Result

In the Security Exposure Management Workspace, on the List page, navigate to **Exceptions** &gt; **All**, open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

|Approval state|Result|
|--------------|------|
|Approved|The state of the Remediation task transitions to Deferred with the given Reason as sub-state. The state and reason are rolled down to the records. The state of the Remediation task transitions to Deferred with the given Reason as sub-state. The state and reason are rolled down to the records. When risk reduction is also requested, a separate change approval is created for the risk reduction request. If that approval is also approved, the risk rating of the records is updated to the desired risk rating that was selected during the bulk edit request.|
|Rejected|The state of the Remediation Task and its records doesn’t change.|

In the **Activity stream** of a record or remediation task, you can view the entire workflow of your request.

**Related topics**  


[Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md)

