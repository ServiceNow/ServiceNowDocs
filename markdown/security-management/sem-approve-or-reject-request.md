---
title: Approver roles required for Security Exposure Management Workspace
description: You can see the required roles for the approvers in the Security Exposure Management Workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-08-01"
reading_time_minutes: 1
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Approver roles required for Security Exposure Management Workspace

You can see the required roles for the approvers in the Security Exposure Management Workspace.

<table id="table_b32_g4m_zyb"><thead><tr><th>

Approval type

</th><th>

Approver roles

</th></tr></thead><tbody><tr><td>

False positive approvals

</td><td>

sn\_vul.false\_positive\_approver -   sn\_vul.vulnerability\_admin
-   sn\_vul.vulnerability\_analyst

Approvers are required to be in the False Positive Approver user group.

</td></tr><tr><td>

Exception approvals \(deferrals\)

</td><td>

-   sn\_sec\_exception.admin
-   sn\_sec\_exception.read
-   sn\_sec\_exception.approver

</td></tr><tr><td>

Unassign approvals

</td><td>

sn\_vul.unassign\_approver

</td></tr><tr><td>

Risk reduction approvals

</td><td>

sn\_vul.exception\_approver

</td></tr></tbody>
</table>**Parent Topic:**[Exception Management Overview](sem-exception-management-overview.md)

