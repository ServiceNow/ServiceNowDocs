---
title: Assign TPRM roles to users and user groups
description: Assign roles to users before you implement or use the Third-party Risk Management application. Assigning roles in a well-organized manner simplifies and improves process management and helps to ensure that users are promptly notified of tasks in their areas of responsibility.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Assign TPRM roles to users and user groups

Assign roles to users before you implement or use the Third-party Risk Management application. Assigning roles in a well-organized manner simplifies and improves process management and helps to ensure that users are promptly notified of tasks in their areas of responsibility.

## Before you begin

Role required: admin

## About this task

The roles discussed in this procedure are described in [Roles in Third-party Risk Management](../reference/tprm-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Administration** &gt; **User Groups**.

2.  Select the Roles related list to assign roles to the group.

    1.  In the search field for the **Collection** list, enter `sn_vdr` to view the list of roles that relate to the TPRM application.

        TPRM roles are described in [Roles in Third-party Risk Management](../reference/tprm-roles.md).

    2.  Move the roles that are appropriate for the group from the **Collection** list to the **Roles** list and then select **Save**.

        In this example, the **sn\_vdr\_risk\_asmt.vendor\_risk\_manager** role is assigned to the group that the user has named `Third-party Risk Managers`.

        ![Adding a role to the "Third-party Risk Managers" group.](../image/vrm-group-role-list.png)

3.  On the Group Members related list, select **Edit**.

4.  Move all appropriate users from the **Collection** list to the **Group Members List** and then select **Save**.

5.  Use the Groups related list to add subgroups to the group that you are defining.


**Related topics**  


[Roles in Third-party Risk Management](../reference/tprm-roles.md)

[TPRM and the Explicit Roles plugin](../../grc-vendor-risk/concept/vrm-and-explicit-roles-plugin.md)

