---
title: Request an extension for an exception rule in Configuration Compliance
description: Request an extension for a deferred exception rule before it reaches its deferred until due date. As a remediation owner, you’re no longer required to wait until the deferred due date to make this request.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Requesting and approving an exception for a remediation task, Configuration Compliance remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Request an extension for an exception rule in Configuration Compliance

Request an extension for a deferred exception rule before it reaches its deferred until due date. As a remediation owner, you’re no longer required to wait until the deferred due date to make this request.

## Before you begin

Role required: sn\_vul.exception\_approver

## About this task

You can also request an extension from the Vulnerability Response Workspaces. For more information, see [Request an extension for a deferred vulnerable item in the Vulnerability Manager workspace](../../vulnerability-response/task/extend-defer-vul-item-ws.md).

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Exception Rules**.

2.  Select an approved exception rule.

3.  Select **Request Extension**.

4.  Fill in the fields on the form, as appropriate.

<table id="table_s52_yvn_r6"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Extend Until

</td><td>

Select the date until when the exception rule must be extended.

</td></tr><tr><td>

Reason

</td><td>

Enter the reason for deferring the exception rule. Choices include:

-   Risk accepted
-   Awaiting maintenance window
-   Fix unavailable
-   Mitigating control in place
-   Other


</td></tr><tr><td>

Additional information

</td><td>

Enter any other relevant information.

</td></tr></tbody>
</table>5.  Select **Request Approval**.

    On approval of the request, the Deferred until, Reason and Additional information fields get updated on the exception rule and the associated remediation tasks. An email is also triggered on submission of the request and subsequent action by the approver.

    **Note:**

    -   The request goes through two levels of approval.
    -   If a deferred exception rule is extended again, the extend deferral count increases in the backend.

**Parent Topic:**[Requesting and approving an exception for a remediation task](../concept/cc-ex-mgmt-request-approve.md)

