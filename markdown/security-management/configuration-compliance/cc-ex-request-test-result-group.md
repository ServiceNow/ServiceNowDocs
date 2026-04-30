---
title: Request an exception for a remediation task in Configuration Compliance
description: Request an exception to defer the remediation of a remediation task for a specified period if it can’t be remediated immediately.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Requesting and approving an exception for a remediation task, Remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Request an exception for a remediation task in Configuration Compliance

Request an exception to defer the remediation of a remediation task for a specified period if it can’t be remediated immediately.

## Before you begin

Role required: sn\_vulc.remediation\_owner

## About this task

**Important:** You can request an exception for:

-   remediation tasks in the Vulnerability Manager Workspace and IT Remediation Workspace. For more information, see [Request an exception in the IT Remediation Workspace](../../vulnerability-response/task/vr-ws-request-exception.md).
-   multiple test results simultaneously from the Vulnerability Manager Workspace. For more information, see [Request bulk exception in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vmws-bulk-edit-request-exception.md).

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Remediation Tasks** &gt; **All Tasks**.

2.  Select the remediation task that you want to request an exception for.

    The selected task must be in the Open, Under Investigation, or Awaiting Implementation state.

3.  On the Remediation Task form, click **Request Exception**.

    **Note:** Depending on whether Vulnerability Response or GRC: Policy and Compliance Management is selected in the **Configuration Compliance** &gt; **Exception Management** screen, the Request Exception form changes. See [Configure Exception Management for Configuration Compliance](configure-exception-management-configuration-compliance.md)

4.  If Vulnerability Response is selected in the Exception Management screen, then do the following:

    1.  On the form, fill in the fields.

<table id="table_kxh_gh2_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Until

</td><td>

Date on which the exception request expires. This date must be within the duration selected in the **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Exception Management** screen.When the exception request expires, the remediation task reverts to its Open state.

**Note:** Starting with version 14.7 of Configuration Compliance \(CC\), if a deferred remediation task is reopened by a scanner before the exception window expires, then the state of the remediation task changes from Open to Deferred. This functionality is disabled by default. To enable this functionality, set the value of the system property **sn\_vulc.auto\_defer\_test\_result\_in\_active\_exception\_window** to true. Also, the deferred until date persists even after the remediation task reopens after the expiration date.

</td></tr><tr><td>

Reason

</td><td>

Reason for the exception. Choices are as follows:-   Risk Accepted
-   Awaiting Maintenance Window
-   Fix Unavailable
-   Mitigating Control in Place
-   Other
To see how to add new reason choices, see [Define policy reason mappings](define-policy-reason-mappings.md).

</td></tr><tr><td>

Additional information

</td><td>

Details that are related to the reason why this request is being made. This field is to be updated by the remediation owner.

</td></tr></tbody>
</table>    2.  Submit the exception request by clicking **Request Approval**.


## Result

The state of the remediation task changes to In Review. Use the **State Change Approval** tab to track the status of the exception request.

