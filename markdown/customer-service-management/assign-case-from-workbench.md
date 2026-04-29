---
title: Assign a case from the assignment workbench
description: Users with the customer service manager role can assign a case to an agent from the assignment workbench.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent management, Use, Customer Service Management]
---

# Assign a case from the assignment workbench

Users with the customer service manager role can assign a case to an agent from the assignment workbench.

## Before you begin

Role required: sn\_customerservice\_manager

## About this task

**Note:** The Find Agents feature is available only in the classic environment.

## Procedure

1.  Open a customer service case.

2.  Select the Find Agents icon \(![Find Agents icon.](../image/FindAgentsIcon.png)\) next to the **Assigned to** field to open the assignment workbench.

    If the case has an **Assignment group**, the agents from that group are listed on the workbench. If the case doesn’t have an assigned group, no agents are displayed.

    **Note:** The state of the current record determines the availability of the Find Agents icon. The icon is available for records in the **Open**, **Awaiting**, and **Cancelled** states, and if the user has write access for the **Assigned to** field. The icon isn’t available for records in the **New** or **Closed** states or when the **Assigned to** field is read only for the current user.

3.  Select an assignment group from the **Group** list.

    The list of agents updates based on the selected group.

4.  Add or remove skills from the **Skills** list.

    The selected skills appear in a list below this field. The **Matching Skills** column updates to reflect the selected skills.

    **Note:** Mandatory skills can’t be changed.

5.  Sort the agents by selecting the column header for the desired matching criteria.

6.  Select an agent by enabling the check box by the agent's name and then select **Assign**.

    The assignment workbench closes and the name of the selected agent appears in the **Assigned to** field on the Case form.

7.  Select **Update** to save the agent assignment.


**Related topics**  


[Assignment workbench overview](../concept/case-assignment-workbench.md)

