---
title: Move employees on a floor or to a different floor using the map
description: Using the building's Floor map view, move single or multiple employees on a floor or to a different floor. Assign or unassign a space to an employee.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 7
breadcrumb: [Map based space administration, Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Move employees on a floor or to a different floor using the map

Using the building's Floor map view, move single or multiple employees on a floor or to a different floor. Assign or unassign a space to an employee.

## Before you begin

Verify that the building in which you want to move employees has a floor map.

**Note:** You must install the Workplace Move Management plugin to move an employee to a different location.

**Important:** You can't move an employee who already has an ongoing move request.

Role required: sn\_wsd\_spcmgmt.space\_planner

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  Select the **Space Optimization** icon \(![Space optimization icon.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  In the All Buildings section, select the building where you want to make employee movements.

    **Important:** You can't move an employee who already has an ongoing move request.

    Select **View all** to view a list of buildings.

    The stack plan of the building opens.

4.  On the Stack plan, select the **Floor map** tab to view the building's floor map.

5.  Select the floor where you want to move employees using the **Floor** option on the map.

6.  On the side panel, select **Users**

    The floor map displays user icons based on employee assignments.

    ![Legend displaying user assignments on the floor map.](../images/movefloormap-userandmovecase.png)

    On the map, spaces assigned to an employee, spaces with move cases, and selected spaces are displayed with the following icons:

7.  To view the details of the employees assigned to a space, select the User or the Move options on the space.

    You can also search for an employee to view their details.

    You can select multiple users by drawing a circle \(lasso\) around them or by using the Shift key on the keyboard.Selected spaces are highlighted with the Selected employee icon \(![Selected employees icon.](../images/movefloormap-selected.png)\).

    The details of the assigned employees are displayed on the **User profiles** panel.For the Neighborhood view by configuration, the neighborhood details are displayed on the user card. If there’s an ongoing move case, then move case details are displayed.

8.  To view the details of the move case on a space, select the move case option on the space.

    You can select multiple users by drawing a circle \(lasso\) around them or by using the Shift key on the keyboard.Selected spaces are highlighted with the Selected employee icon \(![Selected employees icon.](../images/movefloormap-selected.png)\).

    The details of the incoming or outgoing move case are displayed on the **User profiles** panel. An incoming move case is tagged as **Incoming** and an outgoing move case is tagged as **Outgoing**. You can select the move case number to view the move case details on a separate tab.

9.  To move an employee to a different location, follow these steps:

    **Important:**

    If **Neighborhood** is selected as the group by option, only assignments that have the **Neighborhood assignment** type are applicable. For any other group by option, assignments that have the **Location assignment** type are applicable.

    1.  Select the space on the map where the employee is assigned.

        The employee details are displayed on the **User profiles** panel.

    2.  On the employee details tile, to move the employee, select **Move to**.

        You can also select the destination space by selecting the space from the floor map.

    3.  In the **Actions** field, select the type of move you want to perform.

        You can select from the following options:

        -   Assign or move to space: Select this option to move the employee to a different space.
        -   Assign or move to area: Select this option to move the employee to a different area.
        -   Assign or move to floor: Select this option to move the employee to a different floor.
        -   Assign or move to building: Select this option to move the employee to another building.
        -   Unassign: Select this option to unassign the space to the employee.
        **Note:** The **Select building** field is set by default with the current building. You can’t change the building.

    4.  In the **Select neighborhood** field, select the neighborhood where you want to move the employee.

        This field is available only if the View by configuration is neighborhood.

        To move employees with neighborhood assignments, you can only select spaces that are assigned to a neighborhood.

        **Note:** If an employee is selected more than once, all actions related to the employee are set to invalid.

    5.  In the **Select floor** field, select the floor where you want to move the employee.

    6.  In the **Assign area** field, select the area where you want to move the employee.

    7.  In the **Assign space** field, select the space where you want to move the employee.

    8.  Select **Apply**.

    9.  On the confirmation window, review the entries, then select **Confirm**.

        A move request is created to perform the move. The map displays the space from where the employee is moved and the space where the employee is to be moved are marked with the move symbol.

10. To unassign an employee from a space, do the following:

    1.  Select the space on the map where the employee is assigned.

        The employee details are displayed on the **User profiles** panel.

    2.  On the employee details tile, to unassign the employee from the space, select **Unassign**.

    3.  On the form, select **Apply**.

    4.  On the confirmation window, review and select **Confirm**.

        Unassigning a neighborhood assignment for an employee deactivates the assignment in the Workplace Profile.

        The employee is unassigned from the space.

11. To assign an employee to a space, do the following:

    **Important:** You can't move an employee who already has an ongoing move request.

    1.  Select the space on the map where you want to assign the employees.

        The details are displayed on the **User profiles** panel. If there’s an existing move case or if there are existing employees, the respective details are displayed on the panel.

    2.  Search and select the employees.

        Perform one of the following to search:

        -   In the **Search users** field, search for the employee whom you want to assign.

            From the list, select the user.

        -   For an advanced search, select the Search users slider icon \(![User slider icon.](../images/movefloormap-searchuserslider.png)\).
            1.  On the **Select users** window, search from a list of **System users** or **Workplace profiles**.
            2.  Select the employees and select **Select users**.
        The selected employees are added to the panel.

        -   If the selected employee doesn’t have any existing location, the **Current location** isn’t displayed.
        -   If the selected employee is already assigned to a location, the location details are displayed in the **Current Location**.
    3.  To assign an employee who isn’t assigned to any location already, do the following:

        **Important:** You can't move an employee who already has an ongoing move request.

        1.  On the employee details tile of that employee, select **Assign to**.
        2.  On the form, specify the type of assignment in the **Actions** field and the location details in the **Select floor**, **Assign area**, and **Assign space** fields accordingly.
        3.  Select **Apply**.
        4.  On the confirmation window, review and select **Confirm**.

            The selected space is assigned to the workplace profile of the employee. If a primary space is already assigned to the workplace profile, the selected space is assigned with the **Is primary** field set to false.

    4.  To assign an employee who is already assigned to a space, do the following:

        **Important:** You can't move an employee who already has an ongoing move request.

        1.  On the employee details tile of that employee, select **Assign to**.
        2.  On the form, specify the type of assignment in the **Actions** field and the location details in the **Select floor**, **Assign area**, and **Assign space** fields accordingly.
        3.  Select **Apply**.
        4.  On the confirmation window, review and select **Confirm**.

            The selected space is assigned to the workplace profile of the employee and the earlier space is unassigned. If a primary space is already assigned to the workplace profile, the selected space is assigned with the **Is primary** field set to false.

12. To perform multiple employee moves, assignment or unassignment at a time, do the following:

    **Important:** You can't move an employee who already has an ongoing move request.

    1.  Select and hold down the **Shift** key to draw a circle \(lasso\) or draw any freehand selection border around the spaces.

        The selected spaces are marked with the selected icon ![Set to true icon.](../images/movefloormap-selected.png) icon. The employee details and the move cases on the selected spaces are displayed on the **User profiles** panel.

    2.  On the panel, perform the steps 9, 10 and 11 accordingly.

        Select the check box on the employee details tile if you have multiple changes and perform the actions.

        To assign a space to an employee, use the **Assign to** option.

        To move an employee from the existing space to another space, use the **Move to** option.

        To unassign an employee from the space, use the **Unassign** option.


**Parent Topic:**[Map based space administration](../concept/map-based-space-administration.md)

**Related topics**  


[Edit a building's spaces using a map](edit-space-details-for-buildings.md)

