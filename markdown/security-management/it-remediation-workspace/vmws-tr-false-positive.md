---
title: Request false positive for a set of test results
description: Starting with v22.0 of Vulnerability Response, you can raise a false positive request for a set of test results within a remediation task, in the IT Remediation Workspace.
locale: en-US
release: xanadu
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Request a false positive in the IT Remediation Workspace, Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request false positive for a set of test results

Starting with v22.0 of Vulnerability Response, you can raise a false positive request for a set of test results within a remediation task, in the IT Remediation Workspace.

## Before you begin

Role required: sn\_vulc.remediation\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  On the List page, open a Configuration Compliance Remediation Task.

3.  In the Overview related item, under the Test Results tab, select the test results that you want to mark as false positive.

    **Note:** You can request a false positive for a set of test results within a Remediation Task only when:

    -   At least one selected test result is in the Active state.
    -   Remediation Task has at least two test results.
    -   All the test results aren’t selected.
4.  Select the **Mark as False Positive** button on the Configuration Test Results tab.

5.  In the dialog that is displayed, enter information about the request and select **Request Approval**.

6.  On the Take Questionnaire modal, answer the questions to provide additional information about your request to the approver and select **Submit**.

    **Note:** The Take Questionnaire modal appears only when the **Enable questionnaire to mark false positive** check box is selected in the Exception Management Configuration form. For more information on how a questionnaire is configured, see [Configure Exception Management for Configuration Compliance](../../vulnerability-config-compliance/task/configure-exception-management-configuration-compliance.md).

    The selected test results are moved to a new remediation task and your request is submitted for approval. The task number appears in the **Activity stream** of the old Remediation Task. The approver receives an email notification about your request.


## Result

You will receive an email notification on the approval or rejection of your request.

In the **Activity stream** of a test result or remediation task, you can view the entire workflow of the false positive request.

## What to do next

1.  In the IT Remediation Workspace, on the List page, navigate to **Exception Requests** &gt; **My requests**.
2.  Open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

    |Approval state|Result|
    |--------------|------|
    |Approved|The State of the new remediation task transitions to Closed with Reason as False positive.|
    |Rejected|The state of the new remediation task changes to Open.|

3.  After the request is approved, navigate to the Details tab of the new Remediation Task, and set the expiry date for false positive in the **Until** field if necessary.

    The remediation task will revert to the Open state after the specified date and the State is rolled down to the test results.


