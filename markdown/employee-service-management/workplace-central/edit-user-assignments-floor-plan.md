---
title: Edit user assignments on the floor plan
description: Use the floor plan to edit location or neighborhood assignments for the users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-central/edit-user-assignments-floor-plan.html
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Floor Plan, Working with Space Planning, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit user assignments on the floor plan

Use the floor plan to edit location or neighborhood assignments for the users.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager or sn\_wsd\_spcmgmt.space\_planner

**Note:** The sn\_wsd\_core.scenario\_reader role has access to view the map and user assignments.

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

2.  On the side navigation, select the **Space Planning** module.

    The Space Planning workspace opens with the **Floor plan** tab selected by default.

3.  Select a campus, building, and floor to view the map.

4.  Select a **View by** option to group spaces on the map.

    The default view by option is set to **None**.

5.  Edit the user assignments based on your requirement.

<table id="choicetable_vyl_2qc_f3c"><thead><tr><th align="left" id="d452638e113">

Action

</th><th align="left" id="d452638e116">

Steps

</th></tr></thead><tbody><tr><td id="d452638e122">

**Assign a single user**

</td><td>

1.  Select the space that you want to assign the user to.

If you don't select any space, the user is assigned to the floor selected on the map.

2.  On the details panel, select **Add users**.
3.  On the Add users pop-up, search for the user that you want to assign.
4.  Select the user from the list.
5.  Select either of the following assignment type for the user.
    -   **Location**: Creates a location assignment on the workplace profile.
    -   **Neighborhood**: Creates a neighborhood assignment on the workplace profile.
6.  Based on your assignment type, fill in the following fields.
    -   **Move from location**: Existing location assignment of the user. This field is displayed only for the **Location** assignment type.
    -   **Select neighborhood to move the user from**: Existing neighborhood assignment of the user. This field is displayed only for the **Neighborhood** assignment type.
    -   **Select neighborhood to move the user to**: New neighborhood assignment of the user. This field is displayed only for the **Neighborhood** assignment type.
7.  Select **Confirm**.


</td></tr><tr><td id="d452638e202">

**Assign multiple users**

</td><td>

1.  Select the spaces that you want to assign the users to.

If you don't select any space, the users are assigned to the floor selected on the map.

2.  On the details panel, select **Add users**.

If you can select a single space, then from the Users section, select **Add**.

3.  On the Add users pop-up, select the **Select users by criteria** tab.
4.  Select either of the following assignment type for the users.

    -   **Location**: Creates a location assignment on the workplace profiles.
    -   **Neighborhood**: Creates a neighborhood assignment on the workplace profiles.
For the **Neighborhood** assignment, you must select the neighborhood you want to assign the users to.

5.  Add conditions to filter the users.

For example, `Workplace profile is Active`. For more information about conditions, see .

6.  Select the users that you want to assign, then select **Confirm**.


</td></tr><tr><td id="d452638e274">

**Move a user**

</td><td>

**Note:** Moving a user requires the Workplace Move Management plugin.

 1.  Select a user on the map.

Alternatively, you can select a space that has a user assigned.

2.  On the details panel, on the user card, select **Move**.
3.  In the **From location** section, select the location that the user must move from.
4.  In the **To location** section, select the building, floor, and space the user must move to.
5.  Select **Apply**.


</td></tr><tr><td id="d452638e321">

**Unassign users**

</td><td>

1.  Select spaces or users on the map.
2.  On the details panel, select **Unassign**.

The Unassign users pop-up opens.

3.  Select the following options based on your requirement.
    -   **From the selected location**: Removes the selected assignment from the selected users.
    -   **From all location assignments**: Removes all location assignments from the selected users.
    -   **From all neighborhood assignments**: Removes all neighborhood assignments from the selected users.
4.  Select **Confirm**.


</td></tr></tbody>
</table>
**Parent Topic:**[Use Floor Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/use-floor-plan.md)

