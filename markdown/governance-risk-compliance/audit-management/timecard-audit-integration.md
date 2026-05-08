---
title: Integrating Audit Management with Time Card management
description: Audit users and audit managers can now use the Time Card Management feature to log and capture hours for engagements and other tasks on an engagement.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit Management, Governance, Risk, and Compliance]
---

# Integrating Audit Management with Time Card management

Audit users and audit managers can now use the Time Card Management feature to log and capture hours for engagements and other tasks on an engagement.

The Time Card management feature enables users to submit and track their time for the assigned tasks. With the Time Card Management feature:

-   The time card users can record the time worked on a task using time cards and time sheets. They can then submit their time cards and time sheets for approval.
-   Time cards and time sheets are routed for approval based on the **Non-project time approver** field in the user time sheet policy. Managers with the time card approver role can also log time and submit the time sheet of their resources.

When you integrate Audit Management with Time Card management, you can report a time card for:

-   an engagement
-   audit tasks
-   issues
-   milestones

To use the Time Card management feature integration with GRC Advanced Audit, you must activate the following plugins:

-   Project Portfolio Management
-   GRC: Advanced Audit

**Note:** You must enable advanced planning for the engagement.

When an audit user logs time using time cards, the time cards are sent for approval based on the approvers defined in the time sheets policy. To learn more about time sheets policy, see Time sheet policy

**Note:** If there's no approver identified or **None** is selected in the **Non-project time approver** field on the time sheet policy assigned to the user, then the users in the **Time card approver** field are able to approve the time cards associated to that engagement. If **User Manager** or **Auto** is selected in the **Non-project time approver** field, then the approvers are not overridden and remain as is. For details on the roles required to approve time cards, see [Roles required for Advanced planning capability](../reference/roles-for-audit-and-ppm.md)

To create a time card, see Create a time card.

A user can submit the time cards through the time sheet portal directly without coming to the engagement. To submit a time card, see Submit a time card. To submit a time card from the time sheet portal, see Submit time card from the time sheet portal

## Time cards and rollup of expenses and resources

In the version 12.0.1, release of Audit Management, when an engagement has a project associated with it, after a time card is approved and expense lines are processed, both the **Actual resources** and the **Actual expenses** values roll up on the engagement. Although you can create a time card and log hours before you create a project for an engagement, it is recommended to create a time card after a project is created. This task ensures accurate reporting of the expenses and resources. The Time Cards related list appears on an engagement only after a project is created.

**Related topics**  


[Roles required for Advanced planning capability](../reference/roles-for-audit-and-ppm.md)

