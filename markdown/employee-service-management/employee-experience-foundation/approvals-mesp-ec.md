---
title: Approvals in Now Mobile
description: View all your approval tasks in one place in the Now Mobile app.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Employee Center for mobile, Configure, Employee Center, Employee Service Management]
---

# Approvals in Now Mobile

View all your approval tasks in one place in the Now Mobile app.

Access all your approval tasks under **My Tasks** section in Now Mobile.

-   Approve or reject after checking the details of an approval task on the **Details** tab.
-   Use the **Updates** tab to provide your comments, view comments from someone, or add or see an attachment relevant to the approval task.
-   View the due date information of each task on the list view under **My Tasks** and on the details pages of individual approval tasks.

If you want to reject an approval task, you must provide a reason to submit it. Comments are optional when you approve a task.

The order of priority for the information displayed on the list view in **My Tasks** is as follows:

1.  Short description
2.  Approval For
3.  Approving

## Generic approval

The generic approval that is shipped with the Now Mobile version 29.0 displays all the approval tasks available on the Approval \[sysapprover\_approval\] table.

Users with an approver role can access all their approval tasks in the Now Mobile app under **My Tasks**.

**Note:** The Generic approval is enabled in the base system as:

-   The system property, sn\_me\_todos.all\_approvals\_mobile\_enabled, is enabled by default.
-   The system property, sn\_me\_todos.all\_approvals\_mobile\_enabled, can be disable to stop using the generic approval card.
-   If you want to create a custom approval card within the Approval To-dos list, the value of the **Condition order** field of the custom configuration must be lower than the **Condition order** of the Generic approval card.

For more configuration info, see [Enable task configuration for approvals](../task/approval-hub-to-dos-page-filters.md).

**Parent Topic:**[Configuring Employee Center for mobile](ec-mobile-configrations.md)

