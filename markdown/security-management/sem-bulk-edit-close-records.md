---
title: Close records in bulk in the Security Exposure Management Workspace
description: Close multiple records \(VITs, AVITs, or CVITs\) concurrently using the bulk edit feature in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-bulk-edit-close-records.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Close records in bulk in the Security Exposure Management Workspace

Close multiple records \(VITs, AVITs, or CVITs\) concurrently using the bulk edit feature in the Security Exposure Management Workspace.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **List**.

2.  On the List page, open Active or All list in one of the following lists:

    -   Host Vulnerable items
    -   Container Vulnerable items
    -   Application Vulnerable items
3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the Only Selected Items option in the [**Record Selection**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-manager-workspace/vmws-bulk-edit-close-records.md) field.
    -   Apply filters if you want to use the All Vulnerable Items that match filter option in the [**Record Selection**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-manager-workspace/vmws-bulk-edit-close-records.md) field.
4.  Select the **Bulk Edit** button.

5.  On the form, select **Closed** in the **State** field, and select a **Reason** to close the selected records.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md).

6.  Click  **Edit**.

    A bulk edit asynchronous job updates the relevant records.


**Related topics**  


[Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md)

