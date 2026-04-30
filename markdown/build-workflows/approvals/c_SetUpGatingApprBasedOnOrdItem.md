---
title: Set up a gating approval based on the item being ordered
description: In addition to adding approvals via approval rules, you can also add approvals based on what kind of item is being ordered.
locale: en-US
release: xanadu
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Gating approvals, Approval rules, Classic approvals, Build workflows]
---

# Set up a gating approval based on the item being ordered

In addition to adding approvals via approval rules, you can also add approvals based on what kind of item is being ordered.

In addition to adding approvals via approval rules, you can also add approvals based on what kind of item is being ordered. We can, for example, specify that all Blackberrys need to be approved by David Loo.

To do so, navigate to the item in question and scroll to the related list of required approvers. There are two lists:

-   **Approved By Group**: A list of groups that have to approve requests for this item
-   **Approved By**: A list of users who have to approve requests for this item

![Approve list](../image/ApproveList.png "Approve list")

In the example above, this request must be approved by all members of the Hardware group and by David Loo.

Notes and limitations:

1.  As with approval rules, you are protected against duplicate entries. Thus if a person is a member of the hardware group, as well as being a standalone approver, the person will only get one approval request.
2.  Item-based approved work in addition to rather than instead of approval rules so you can \(and probably will\) use both.

