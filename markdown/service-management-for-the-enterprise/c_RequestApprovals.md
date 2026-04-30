---
title: Request approvals
description: Approving a request in an SM application means that the request is ready for task creation and assignment.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request Management in a Service Management application, Service Management]
---

# Request approvals

Approving a request in an SM application means that the request is ready for task creation and assignment.

When a request is sent to a user with the \[SM application\]\_approver\_user role, the approver has several choices. If you select **Approval is required for new requests** in the applications Configuration screen, a newly created request automatically moves to the **Awaiting Approval** state. Otherwise, the request moves to the next configured state.

<table id="table_syj_r13_yq"><thead><tr><th>

Approval Choice

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approved

</td><td>

The request is approved.

</td></tr><tr><td>

Rejected

</td><td>

The request is not qualified and it is moved to the canceled state. Also, the following work note is added to the request:

 **The \[SM application\] request is rejected.**

</td></tr><tr><td>

More information required

</td><td>

The request does not contain enough information. It reverts to the **Draft** state and the following work note is added to the request:

 **The \[SM application\] request needs more information for further approval.**

</td></tr><tr><td>

Duplicate

</td><td>

The request is no longer required, because another request has already performed the work. The request is moved to the **Cancelled** state and the following work note is added to the request:

 **This is a duplicate \[SM application\] request.**

</td></tr></tbody>
</table>**Parent Topic:**[Request Management in a Service Management application](rm-sm-application.md)

