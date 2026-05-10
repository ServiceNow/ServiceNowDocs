---
title: Request an extension for a deferred remediation task
description: As a remediation owner, you’re no longer required to wait until the deferred due date to make this request. Request an extension for a deferred remediation task before it reaches its deferred until due date.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Request an extension for a deferred remediation task

As a remediation owner, you’re no longer required to wait until the deferred due date to make this request. Request an extension for a deferred remediation task before it reaches its deferred until due date.

## Before you begin

Role required: sn\_sec\_exception.admin

## About this task

You can also request an extension from the Security Exposure Management Workspace.

## Procedure

1.  Navigate to **Security Exposure Management Workspace** &gt; **List** &gt; **Remediation Tasks**.

2.  Open a deferred remediation task.

3.  Select **Request Extension**.

4.  Fill in the fields on the form, as appropriate.

<table id="table_s52_yvn_r6"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Extend Until

</td><td>

Select the date when the Defer state expires and the remediation task is reactivated.

</td></tr><tr><td>

Reason

</td><td>

Enter the reason for deferring the issue. Choices include:

-   Awaiting maintenance window
-   Fix unavailable
-   Risk accepted
-   Mitigating control in place
-   Other


</td></tr><tr><td>

Additional information

</td><td>

Enter any other relevant information.

</td></tr></tbody>
</table>5.  Select **Request Approval**.

    On approval of the request, the changes on the remediation task are rolled down to the vulnerable items as well, which are part of the remediation task. However, the vulnerable items should be in the deferred state and their current until data precedes the updated until date. An email is also triggered on submission of the request and subsequent action by the approver.

    **Note:**

    -   The request goes through multi-levels of approval.
    -   The Request Extension button is unavailable for remediation tasks that are created as part of an exception rule.
    -   If a deferred remediation task is extended again, the extend deferral count increases in the backend.

**Parent Topic:**[Exception Management Overview](../concept/sem-exception-management-overview.md)

