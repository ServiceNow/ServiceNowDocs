---
title: Assign records to an assignment group in bulk
description: Assign multiple records findings concurrently to an assignment group using the bulk edit feature in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-bulk-edit-assign.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
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

    -   Select the check box next to each item if you want to use the **Only Selected Items** option in the [Record selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-manager-workspace/vmws-bulk-edit-assign.md) field.
    -   Apply filters if you want to use the **All records that match filter** option in the [Record selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-manager-workspace/vmws-bulk-edit-assign.md) field.
4.  Select the **Bulk Edit** button.

5.  On the form, select the **Assignment group** to which you want to reassign the records.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md).

6.  Select  **Edit**.


## Result

Open a record for which you updated the assignment group and navigate to the **Overview** tab. The user group to which the record is assigned appears in the **Assignment group** field.

**Related topics**  


[Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md)

