---
title: Bulk edit host vulnerable items with patches and solutions
description: Recommend a patch or solution for multiple host vulnerable items concurrently using the bulk edit feature in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-bulk-edit-patches-solutions.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit host vulnerable items with patches and solutions

Recommend a patch or solution for multiple host vulnerable items concurrently using the bulk edit feature in the Security Exposure Management Workspace.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

In the Bulk edit modal, while adding a preferred solution and patch, you can also unassign or assign multiple host vulnerable items \(VITs\) to an assignment group simultaneously.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

    **Note:** The selected records must be in the Open, Under Investigation, or Awaiting Implementation state.

2.  On the List page, under Host Vulnerable items, open the Active or All list.

3.  Perform one of the following:

    -   Select the check box next to each item if you want to use the **Only Selected Items** option in the **Record Selection** field.
    -   Apply filters if you want to use the **All Vulnerable Items that match filter** option in the **Record Selection** field.
4.  Select the **Bulk Edit** button.

5.  On the Bulk Edit modal, select a **Preferred solution** or **Preferred patch** for the selected host vulnerable items.

    For a description of the other field values, see [Bulk edit form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception-form.md).

6.  Select **Edit**.


## Result

A bulk edit asynchronous job updates the selected host vulnerable items \(VITs\). The preferred solution and patch are added to the relevant host vulnerable items \(VITs\). Open a host vulnerable item, and view the preferred solution and patch in the Remediation section of the Details tab.

