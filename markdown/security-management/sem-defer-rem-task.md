---
title: Defer a Remediation task
description: If you identify a finding or remediation task for which a fix is not yet available and can be safely deferred without additional analysis, you can use the Request Exception feature.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 2
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Defer a Remediation task

If you identify a finding or remediation task for which a fix is not yet available and can be safely deferred without additional analysis, you can use the **Request Exception** feature.

## Before you begin

Role required: sn\_sec\_exception.admin

## About this task

You can defer a finding or remediation task directly from its respective form in the Security Exposure Management workspace. Once submitted, the request is sent for approval.

A scheduled job runs every day checking for deferred remediation tasks that have reached their reopen date. On the day the task's deferral is set to expire, the task is reopened.

**Note:** You can manually move change requests and remediation tasks through the states of their life cycles on their respective records with state synchronization enabled, but when the system registers that a CHG has changed its state, or you add a CHG or remove it from a remediation task, state synchronization potentially can override your manual intervention. However, change request states do not automatically move remediation tasks from the Closed or Deferred states.

## Procedure

1.  Navigate to **Security Exposure Management Workspace** &gt; **List** &gt; **Remediation Tasks**.

2.  Open a record.

3.  Click **Request Exception**.

4.  Fill in the fields on the form, as appropriate.

<table id="table_s52_yvn_r6"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Until

</td><td>

Select the date when the Defer state expires and the remediation task is reactivated.

 After the record is submitted, if [email notifications](../../vulnerability-response/task/t_DefineEmailNotifications.md) are defined, members of the group receive an email when the expiration date is within one week. When the defer date expires, the remediation task is set back to **Open** and a second email notification is sent out.

</td></tr><tr><td>

Reason

</td><td>

Enter the reason for deferring the issue. Choices include:

-   Awaiting maintenance window
-   False positive
-   Fix unavailable
-   Risk accepted
-   Mitigating control in place
-   Other


</td></tr><tr><td>

Additional information

</td><td>

Enter any other relevant information.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The group is marked In Review. A **Reopen** related link appears. The reopen date and reason appear in work notes under the **Change Approvals** tab.


**Parent Topic:**[Exception Management Overview](../concept/sem-exception-management-overview.md)

