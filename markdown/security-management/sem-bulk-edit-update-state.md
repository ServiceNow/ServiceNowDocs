---
title: Update the state of records in bulk in the Security Exposure Management Workspace
description: Update the state of multiple findings concurrently according to their remediation progress using the bulk edit feature in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sem-bulk-edit-update-state.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
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

5.  On the Bulk Edit modal, select the target value in the **State** field.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception-form.md).

    Selecting a value for **State** hides the **Risk rating** field. You can change only one of **State** or **Risk rating** in a single bulk edit action.

6.  Select  **Edit**.

    A bulk edit asynchronous job updates the selected records.


**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

**Related topics**  


[Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception-form.md)

