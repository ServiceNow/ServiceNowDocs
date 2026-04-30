---
title: Request a false positive in the IT Remediation Workspace
description: Raise a false positive request for host vulnerable item \(VIT\), application vulnerable item \(AVIT\), container vulnerable item \(CVIT\), or remediation task \(VUL, AVUL, CVUL or CRG\) in the IT Remediation Workspace.
locale: en-US
release: xanadu
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request a false positive in the IT Remediation Workspace

Raise a false positive request for host vulnerable item \(VIT\), application vulnerable item \(AVIT\), container vulnerable item \(CVIT\), or remediation task \(VUL, AVUL, CVUL or CRG\) in the IT Remediation Workspace.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

## About this task

A false positive is a condition wherein the scanner reports that a vulnerability exists in the system, but in reality, there is no vulnerability. There can be multiple reasons, such as incorrect classification, improper logic or algorithm in the scanner.

For more information on how to request a false positive for a set of test results, see [Request false positive for a set of test results](../../vr-vulnerability-manager-workspace/task/vmws-tr-false-positive.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  Locate a remediation task \(VUL, AVUL, CVUL or CRG\) or vulnerable item \(VIT, AVIT, or CVIT\) that you want to mark as false positive.

3.  In the UI action buttons on the right, select **Mark as False Positive**.

4.  In the dialog that is displayed, enter information about the request and select **Request Approval**.

5.  On the Take Questionnaire modal, answer the questions to provide additional information about your request to the approver and select **Submit**.

    **Note:** The Take Questionnaire modal appears only when the **Enable questionnaire to mark false positive** check box is selected in the Exception Management Configuration form. For more information, see [Configure Exception Management for Vulnerability Response](configure-exception-management-settings.md),[Configure Exception Management for Application Vulnerability Response](../../vulnerability-app-vuln-mgmt/task/configure-exception-management-application-vulnerability-response.md), [Configure Exception Management for Container Vulnerability Response](../../container-vulnerability-response/task/configure-exception-management-for-container-vulnerability-response.md), and [Configure Exception Management for Configuration Compliance](../../vulnerability-config-compliance/task/configure-exception-management-configuration-compliance.md).

    The state of the vulnerable item \(VIT, AVIT, or CVIT\) or remediation task \(VUL, AVUL, or CVUL\) transitions to In Review.

    Your request is submitted for approval and the approver receives an email notification about your request.


## Result

You will receive an email notification upon approval or rejection of your request.

## What to do next

In the IT Remediation Workspace, on the List page, navigate to **Exception Requests** &gt; **My requests** and open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

<table id="table_abm_tqr_gbc"><thead><tr><th>

Approval state

</th><th>

Record \(VIT, AVIT, or CVIT\)

</th><th>

Remediation task \(VUL, AVUL, CVUL, or CRG\)

</th></tr></thead><tbody><tr><td>

Approved

</td><td>

The State of the record transitions to Closed with Reason as False positive.

</td><td>

The State of the remediation task transitions to Closed with Reason as False positive. The state is rolled down to the records in the remediation task accordingly.Navigate to the Details tab of a Remediation task and set the expiry date for false positive in the **Until** field if required. The remediation task reverts to the Open state after the specified date and the state is rolled down to the test results.

</td></tr><tr><td>

Rejected

</td><td>

The state of the record does not change.

</td><td>

The state of the remediation task and its records reverts to previous state.

</td></tr></tbody>
</table>In the **Activity stream** of a record or remediation task, you can view the entire workflow of the false positive request.

**Related topics**  


[False Positive overview](../concept/vr-false-positive.md)

