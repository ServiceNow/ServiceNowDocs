---
title: Request an exception in the IT Remediation Workspace
description: Request an exception for the host vulnerable item \(VIT\), application vulnerable item \(AVIT\), container vulnerable item \(CVIT\) and remediation task \(VUL, AVUL, CVUL, or CRG\) from the IT Remediation Workspace.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request an exception in the IT Remediation Workspace

Request an exception for the host vulnerable item \(VIT\), application vulnerable item \(AVIT\), container vulnerable item \(CVIT\) and remediation task \(VUL, AVUL, CVUL, or CRG\) from the IT Remediation Workspace.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

Some vulnerabilities might not have an existing patch, fix, or solution. Or, you might determine that a remediation task cannot be resolved by its target date. When your remediation can't comply with a published vulnerability management or security policy, standard, or guideline, you can request an exception.

You can request exceptions for remediation tasks \(VUL, AVUL, CVUL, or CRG\) and vulnerable items \(VIT, AVIT, or CVIT\) from the IT Remediation Workspace that are assigned to you.

**Note:** Starting with v19.0 of Vulnerability Response, the following terms have been renamed:

|Terminology prior to v19.0|Terminology v19.0 onwards|
|--------------------------|-------------------------|
|Test Result Groups|Remediation Tasks|
|Configuration Issues|Configuration Test Results|
|Policy|Test group|

Starting with version 18.0, you can request exceptions for application vulnerability items and container vulnerability items.

For more information about requesting exceptions in the classic environment, see [Request an exception for a remediation task](raise-exception-vg.md).

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **IT Remediation Workspace**.

2.  Select the List icon.

3.  In the Remediation tasks list, open a remediation task \(VUL, AVUL, CVUL, or CRG\) or record \(VITs, AVITs, or CVITs\) that you want to request an exception for.

4.  In the UI action buttons on the right, click **Request Exception**.

5.  In the dialog that displays, fill in the end date for the exception, select a reason from the list, and add any other required information.

6.  Click **Request Exception**.

7.  On the **Take Questionnaire** modal, answer the questions and click **Submit**.

    **Note:** The **Take Questionnaire** modal appears only when the **Enable questionnaire to request exception** check box is selected in the **Exception Management Configuration** form.

    A message displays that your request is successfully submitted for approval.

    An exception request for a remediation task is approved using a default, two-level approval workflow. After the request is approved by the level 1 approver, it is sent on to the level 2 approver.

    -   The remediation task or record transitions to In Review while the exception request is open.
    -   The remediation task or record transitions to Deferred if the request is approved.
    -   The exception request record \(VCA\#\) is closed after your exception request is approved.
    To view the status of your approval requests, under Exception Requests on the List page, click **My requests**. The number for the request \(VCA\#\) displays when you open the record or remediation task from the list.

    -   If the request is rejected, the request record \(VCA\#\) displays **Rejected** in the Approval state column in your List view under My requests.
    -   You are required to submit a new exception request if you still want to defer this item.

