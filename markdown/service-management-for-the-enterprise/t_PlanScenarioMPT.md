---
title: Plan a move scenario
description: Facilities administrators create move scenarios when planning and executing large-scale moves. When people are added to the scenario, move\_detail records are created. These records contain all the information about the potential move for a specific person, such as the reference to the sys\_user, destination floor, and destination building.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Enterprise move scenarios, Move planning tool, Enterprise move, Facilities move management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Plan a move scenario

Facilities administrators create move scenarios when planning and executing large-scale moves. When people are added to the scenario, move\_detail records are created. These records contain all the information about the potential move for a specific person, such as the reference to the sys\_user, destination floor, and destination building.

## Before you begin

Role required: move\_agent or facilities\_staff

## Procedure

1.  Navigate to **All** &gt; **Enterprise Move** &gt; **Move Planning Tool**.

2.  Click **Create New Scenario**.

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Provide a name for the scenario.|
    |Notes|Enter additional information about the move that you feel is important for the facilities staff to know.|

4.  Click **Submit**.

5.  On the right-side pane, on the Scenarios tab, select the campus this move applies to.

    Occupancy totals for the campus you selected are displayed per floor in bar charts, showing how many seats are assigned to a department or manager. The total number of open seats are shown also.

6.  Click the Planning tab, and select the **User Manager** or **User Department** view.

    **Note:** User Department refers to the department of the user \(sys\_user\) that is sitting there. It is not showing the department that is assigned the space.

7.  Select the manager or department on the floor bar chart.

8.  Click a highlighted segment on one of the floors.

9.  Fill in the fields on the form, as appropriate.

<table id="table_kmr_lvg_x5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Destination building

</td><td>

The building you are moving employees to.**Note:** If no building or floor is specified, the user is moved to the Lounge.

</td></tr><tr><td>

Destination level

</td><td>

The floor you are moving employees to.

</td></tr><tr><td>

Move group

</td><td>

Enter a name for the group you are planning to move.**Note:** Use a unique name to identify a group. After clicking **Submit**, the group name is saved and can be used again.

</td></tr><tr><td>

Move delegator

</td><td>

The person responsible for assigning users to open spaces in a scenario. Refer to [Activate a delegator](t_ActivateADelegator.md).

</td></tr></tbody>
</table>10. To add or delete users in this scenario, click the arrow to expand the **Users** tab.

11. Select users and click **Add Users to Scenario**.

    Users added to the scenario are shown in the pending assignments in the floor details.

    ![In this figure, the users have been added to the move scenario and show as pending on the floor to which they have been assigned.](../image/AddUsersScenarios.png "Pending assignment")


-   **[Lounge](../concept/c_Lounge.md)**  
When a facilities administrator sets up a move scenario without specifying the destination building or floor, the users are moved to the lounge.

**Parent Topic:**[Enterprise move scenarios](../reference/r_EnterMoveScenarios.md)

