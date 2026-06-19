---
title: Edit space allocations on the floor plan
description: Use the floor plan to edit space or neighborhood allocations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-central/edit-space-allocations-floor-plan.html
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 2
breadcrumb: [Use Floor Plan, Working with Space Planning, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit space allocations on the floor plan

Use the floor plan to edit space or neighborhood allocations.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager or sn\_wsd\_spcmgmt.space\_planner

**Note:** The sn\_wsd\_core.scenario\_reader role has access to view the map and space allocations.

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

2.  On the side navigation, select the **Space Planning** module.

    The Space Planning workspace opens with the **Floor plan** tab selected by default.

3.  Select a campus, building, and floor to view the map.

4.  Select a **View by** option to group spaces on the map.

    The default view by option is set to **None**.

5.  Select the spaces that you want to edit.

    1.  On the details panel, select **Select spaces**.

        The Select spaces pop-up opens.

        **Note:** Alternatively, you can select multiple spaces on the map by holding the Shift key. You can also hold the Shift key and draw a circle to select spaces on the map.

    2.  Add conditions to filter the spaces.

        For example, `Department is Finance`. For more information about conditions, see .

    3.  Select the spaces from the list, then select **Select**.

6.  Edit the space allocations based on your requirement.

<table id="choicetable_vyl_2qc_f3c"><thead><tr><th align="left" id="d191745e168">

Action

</th><th align="left" id="d191745e171">

Steps

</th></tr></thead><tbody><tr><td id="d191745e177">

**Edit space allocation**

</td><td>

1.  Select the spaces that you want to edit.
2.  On the details panel, select **Allocate**.
3.  From the Neighborhood list, select the neighborhoods that you want to allocate the spaces to.
4.  On the **Edit space allocation** pop-up, fill in the fields.
    -   **Allocation type**: Type of allocation like department or neighborhood.
    -   **Department/Cost Center/Workplace Entity/Neighborhood**: Allocation group that you want to allocate to the space. This field is based on the Allocation type field.
    -   **Allocation profile**: Profile type of the allocation. You can select the user profile or the workplace profile.
    -   **Allocation percentage**: Percentage of spaces that you want to allocate to the allocation group.
5.  Select either of the following options based on your requirement:
    -   **Remove existing and replace**: Replaces the existing allocations with the new allocation.
    -   **Add to existing**: Retains the existing allocations and adds the new allocation.
6.  Select **Apply**.
 **Note:** For Workplace Entities, if you add a parent and child entity as allocations, only the child entity is displayed on the map legend.

</td></tr><tr><td id="d191745e257">

**Remove allocations**

</td><td>

1.  Select the spaces that you want to edit.
2.  On the details panel, select **Unallocate**.

The Remove space allocations pop-up opens.

3.  Select the allocation type that you want to remove from the spaces.

You can also review the current allocation details based on your selection.

4.  Select **Save**.


</td></tr></tbody>
</table>
**Parent Topic:**[Use Floor Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/use-floor-plan.md)

