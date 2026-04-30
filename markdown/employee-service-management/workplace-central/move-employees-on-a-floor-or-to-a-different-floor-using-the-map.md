---
title: Move employees on a floor or to a different floor using the map
description: Using the building's Floor map view, move single or multiple employees on a floor or to a different floor. Assign or unassign a space to an employee.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Map based space administration, Working with Space Optimization, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Move employees on a floor or to a different floor using the map

Using the building's Floor map view, move single or multiple employees on a floor or to a different floor. Assign or unassign a space to an employee.

## Before you begin

Verify that the building in which you want to move employees has a floor map.

**Note:** You must install the Workplace Move Management plugin to move an employee to a different location.

**Important:** If the employee already has an ongoing move request, you can’t move that employee.

Role required: sn\_wsd\_spcmgmt.space\_planner

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  On the left pane, select **Space Optimization** icon \(![Space optimization icon.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  In the All Buildings section, select the building where you want to make employee movements.

    **Important:** If the employee already has an ongoing move request, you can’t move that employee.

    Select **View all** to view a list of buildings.

    The stack plan of the building opens.

4.  On the Stack plan, select the **Floor map** tab to view the building's floor map.

5.  Select the floor where you want to move employees using the **Floor** option on the map.

6.  On the side panel, select **Users** icon \(![Users icon.](../images/movefloormap-usedetailsoption.png)\).

    The floor map displays user icons based on employee assignments.

    ![Legend displaying user assignments on the floor map.](../images/movefloormap-userandmovecase.png)

    On the map, the spaces assigned to an employee, the spaces that have an ongoing move case and the space that you have currently selected are displayed as follows:

    ![Legends available on the map.](../images/movefloormap-usericonlegend.png)

7.  To view the details of one or more employees assigned to a space, select the ![User icon.](../images/movefloormap-usericon.png) or the Move ![Move icon.](../images/movefloormap-movecase.png) icon on the space.

    After selection, the icon is highlighted with ![Move icon on the map.](../images/movefloormap-selected.png)

    The details of one or more assigned employees is displayed on the **User profiles** panel. If there’s an ongoing move case, then move case details are displayed.

8.  To view the details of the move case on a space, select the ![Move case icon on the map.](../images/movefloormap-movecase.png) icon on the space.

    After selection, the icon is highlighted with ![Move icon on the map.](../images/movefloormap-selected.png) icon.

    The details of the incoming or outgoing move case are displayed on the **User profiles** panel. An incoming move case is tagged as **Incoming** and an outgoing move case is tagged as **Outgoing**. You can select the move case number to view the move case details on a separate tab.

9.  To move an employee to a different location, do the following:

    1.  Select the space on the map where the employee is assigned.

        The employee details are displayed on the **User profiles** panel.

    2.  On the employee details tile, to move the employee, select **Move to**.

    3.  On the form, do the following:

        You can change the floor map view by using the **View space view** option. Upon selection, the floor map displays the space details and the number of employees assigned and doesn’t display employee names. You can also select the destination space from the map by selecting the **View space view** option.

        1.  In the **Actions** field, select the type of move you want to perform. You can select from the following options:

            -   Assign or move to space: Select this option to move the employee to a different space.
            -   Assign or move to area: Select this option to move the employee to a different area.
            -   Assign or move to floor: Select this option to move the employee to a different floor.
            -   Assign or move to building: Select this option to move the employee to another building.
            -   Unassign: Select this option to unassign the space to the employee.
            **Note:** The **Select building** field is set by default with the current building. You can’t change the building.

        2.  In the **Select floor** field, select the floor where you want to move the employee.
        3.  In the **Assign area** field, select the area where you want to move the employee.
        4.  In the **Assign space** field, select the space where you want to move the employee.
        5.  Select **Apply**.
    4.  On the confirmation window, review and select **Confirm**.

        A move request is created to perform the move. On the map, the space from where the employee is moved and the space where the employee is to be moved are marked with the ![Move icon on the map.](../images/movefloormap-movecase.png) icon.

10. To unassign an employee from a space, do the following:

    1.  Select the space on the map where the employee is assigned.

        The employee details are displayed on the **User profiles** panel.

    2.  On the employee details tile, to unassign the employee from the space, select **Unassign**.

    3.  On the form, select **Apply**.

    4.  On the confirmation window, review and select **Confirm**.

        The employee is unassigned from the space.

11. To assign an employee to a space, do the following:

    **Important:** If the employee already has an ongoing move request, you can’t move that employee.

    1.  Select the space on the map where you want to assign one or more employees.

        The details are displayed on the **User profiles** panel. If there’s an existing move case or if there are existing users, the respective details are displayed on the panel.

    2.  Search and select the employees.

        Perform one of the following to search:

        -   In the **Search users** field, search for the employee whom you want to assign.

            From the list, select the user.

        -   For an advanced search, select the Search users slider icon \(![User slider icon.](../images/movefloormap-searchuserslider.png)\).
            1.  On the Select users window, search from a list of **System users** or the **Workplace profiles**.
            2.  Select one or more employees and select **Select users**.
        One or more selected employees is added to the panel.

        -   If the selected employee doesn’t have any existing location, the **Current location** isn’t displayed.
        -   If the selected employee is already assigned to a location, the location details are displayed in the **Current Location**.
    3.  To assign an employee who isn’t assigned to any location already, do the following:

        **Important:** If the employee already has an ongoing move request, you can’t move that employee.

        1.  On the employee details tile of that employee, select **Assign to**.
        2.  On the form, specify the type of assignment in the **Actions** field and the location details in the **Select floor**, **Assign area** and **Assign space** fields accordingly.
        3.  Select **Apply**.
        4.  On the confirmation window, review and select **Confirm**.

            The selected space is assigned to the workplace profile of the employee. If a primary space is already assigned to the workplace profile, the selected space is assigned with the **Is primary** field set to false.

    4.  To assign an employee who is already assigned to a space, do the following:

        **Important:** If the employee already has an ongoing move request, you can’t move that employee.

        1.  On the employee details tile of that employee, select **Assign to**.
        2.  On the form, specify the type of assignment in the **Actions** field and the location details in the **Select floor**, **Assign area** and **Assign space** fields accordingly.
        3.  Select **Apply**.
        4.  On the confirmation window, review and select **Confirm**.

            The selected space is assigned to the workplace profile of the employee and the earlier space is unassigned. If a primary space is already assigned to the workplace profile, the selected space is assigned with the **Is primary** field set to false.

12. To perform multiple employee moves, assignment or unassignment at a time, do the following:

    **Important:** If the employee already has an ongoing move request, you can’t move that employee.

    1.  Select and hold down the **Shift** key to draw a circle \(lasso\) or draw any freehand selection border around the spaces.

        The selected spaces are marked with the selected icon ![Set to true icon.](../images/movefloormap-selected.png) icon. The employee details and the move cases on the selected spaces are displayed on the **User profiles** panel.

    2.  On the panel, perform the steps 9, 10 and 11 accordingly.

        Select the check box on the employee details tile in case of multiple changes and perform the actions.

        To assign a space to an employee, use the **Assign to** option.

        To move an employee from the existing space to another space, use the **Move to** option.

        To unassign an employee from the space, use the **Unassign** option.


**Parent Topic:**[Map based space administration](../concept/map-based-space-administration.md)

**Related topics**  


[Edit a building's spaces using a map](edit-space-details-for-buildings.md)

