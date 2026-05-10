---
title: Request a false positive for a vulnerable item or remediate task
description: Indicate a false positive request for a finding or a remediation task in the Security Exposure Management Workspace. A false positive is a condition where a scanner incorrectly reports that a finding exists in the system due to situations such as an incorrect classification, improper logic, or an algorithm in the scanner.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Request a false positive for a vulnerable item or remediate task

Indicate a false positive request for a finding or a remediation task in the Security Exposure Management Workspace. A false positive is a condition where a scanner incorrectly reports that a finding exists in the system due to situations such as an incorrect classification, improper logic, or an algorithm in the scanner.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select List icon .

3.  Select the remediation task or vulnerable item.

4.  Select **Mark as False Positive**.

5.  Enter information about the request.

6.  Select **Request Approval**.

7.  Provide additional information about your request to the approver and select **Submit**.

    **Note:** The Take Questionnaire modal appears only when the **Enable questionnaire to mark false positive** check box is selected in the Exception Management Configuration form. .


## Result

The state of the vulnerable item or remediation task transitions to In Review.

Your request is submitted for approval and the approver receives an email notification about your request.

You will receive an email notification upon approval or rejection of your request.

## What to do next

In the Security Exposure Management Workspace, on the List page, navigate to **Exception Requests** &gt; **My requests** and open the corresponding state change approval record \(VCA\#\) and check the status of your request in the Approval state column:

<table id="table_abm_tqr_gbc"><thead><tr><th>

Approval state

</th><th>

Record

</th><th>

Remediation task

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

**Parent Topic:**[Exception Management Overview](../concept/sem-exception-management-overview.md)

