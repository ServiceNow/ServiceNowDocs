---
title: Split a remediation task in the IT Remediation Workspace
description: From a remediation task \(VUL, AVUL, CVUL, or CRG\), identify a subset of records and create a new remediation task for them.
locale: en-US
release: zurich
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Split a remediation task in the IT Remediation Workspace

From a remediation task \(VUL, AVUL, CVUL, or CRG\), identify a subset of records and create a new remediation task for them.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

You can select individual records in the Overview tab of a remediation task and move them to a new remediation task.

Use cases for splitting records \(VITs, AVITs, CVITs or CTRs\) from existing remediation tasks into new tasks might include the following examples:

-   You want to create a change request or change requests for a split task.
-   You want to reassign a split task to another user in your assignment group.
-   You request a deferral or exception for a split task, because you know that some vulnerabilities on specific configuration items \(CIs\) cannot be remediated by the target date.

For more information about change requests and splitting a remediation task in the classic environment and for versions of Vulnerability Response prior to v15.0, see [Split a remediation task](vuln_change_mgmnt_split.md).

**Note:** Starting with v19.0 of Vulnerability Response, the following terms have been renamed:

|Terminology prior to v19.0|Terminology v19.0 onwards|
|--------------------------|-------------------------|
|Test Result Groups|Remediation Tasks|
|Configuration Issues|Configuration Test Results|
|Policy|Test group|

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  Open a remediation task \(VUL, AVUL, CVUL, or CRG\) from Home page or List page.

3.  In the Overview tab, select the records \(VITs, AVITs, CVITs, or CTRs\) that you want to move to a new remediation task.

4.  Click **Split Task**.

5.  In the dialog that is displayed, the number of records \(VITs, AVITs, CVITs, or CTRs\) you selected from the list is displayed.

6.  Click **Split Task** again.

    A confirmation message is displayed with a link to the new remediation task.

    Alternatively, you can use the condition builder to filter records \(VITs, AVITs, CVITs, or CTRs\).

7.  Locate a remediation task that you want to split.

8.  In the UI action buttons on the right, click **Split Task**.

    After a few moments, the condition builder displays.

9.  In the modal that is displayed, use the condition builder to identify the subset of records \(VITs, AVITs, CVITs, or CTRs\) that you want to add into a new remediation task.

10. Click **Split Task**.

    If a message displays that no records match your conditions, you must adjust your criteria and click **Split Task** again. Edit the short description field as required. This field can help you find your new remediation task after it is created.

    If records match your conditions, the number of matching records is displayed in a message.

11. Click the **Preview items** link to view the records that match your filter conditions.

    The new remediation task is displayed as a new tab.


