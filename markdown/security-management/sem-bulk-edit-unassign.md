---
title: Remove assignments for host vulnerable items in bulk
description: Remove yourself or your groups from the  Assigned to  and  Assignment group  fields on the findings if you determine that the records aren’t within your scope for remediation, or if you think that records have been incorrectly assigned to you or to your groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sem-bulk-edit-unassign.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Remove assignments for host vulnerable items in bulk

Remove yourself or your groups from the  **Assigned to ** and  **Assignment group ** fields on the findings if you determine that the records aren’t within your scope for remediation, or if you think that records have been incorrectly assigned to you or to your groups.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

The  unassign  feature is applicable for records in any state other than Closed or Resolved. When you remove assignments for host vulnerable items using the bulk edit feature, only relevant records are updated.

You can remove assignments in bulk as a remediation owner, vulnerability manager, or vulnerability analyst. The records that are updated depend on your persona:

-   Remediation owner: Only the records that are assigned to you or to your assignment groups are updated.
-   Vulnerability manager or vulnerability analyst: All the records that meet the conditions you specify in the Bulk Edit modal are updated.

You can remove assignments in bulk for host vulnerable items \(VITs\), application vulnerable items \(AVITs\), container vulnerable items \(CVITs\), and configuration test results. The **Unassign** option appears only when the assignment rules plugin \(com.snc.sec.wf\) is active.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  On the List page, open the Active or All list in one of the following lists:

    -   Host Vulnerable items
    -   Application Vulnerable items
    -   Container Vulnerable items
    -   Configuration Test Results
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the **Only Selected Items** option in the [Record Selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/vmws-bulk-edit-unassign.md) field.
    -   Apply filters if you want to use the **All Vulnerable Items that match filter** option in the [Record Selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/vmws-bulk-edit-unassign.md) field.
4.  Select the **Bulk Edit** button.

5.  On the form, select the **Unassign** check box to remove assignments in bulk.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception-form.md).

6.  Select  **Edit**.

    A remediation task is created with the selected host vulnerable items \(VITs\).

    Your request is submitted for approval and the approver receives an email notification about your request.

    The state of the host vulnerable items \(VITs\) and remediation task \(VUL\) transitions to In Review. If a remediation task is updated with this feature, the  **Assigned to ** and **Assignment group ** fields on all of its associated VITs are also cleared upon approval of your request.


## Result

In the Security Exposure Management Workspace, on the List page, navigate to **Exception Requests** &gt; **All** and open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

|Approval state|Result|
|--------------|------|
|Approved|The **Assigned to** and  **Assignment group** fields of all the host vulnerable items are cleared.|
|Rejected|The **Assigned to** and  **Assignment group** fields of all the host vulnerable items are not updated.|

In the **Activity stream** of a record or remediation task, you can view the entire workflow of your request.

**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

**Related topics**  


[Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception-form.md)

