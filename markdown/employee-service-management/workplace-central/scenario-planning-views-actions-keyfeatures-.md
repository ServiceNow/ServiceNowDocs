---
title: Scenario and Building - Views, states, settings, and key features
description: Create or view a scenario using a stack plan and a floor map view. Scenario planning enables you to allocate spaces and define user assignments efficiently with different views, simple settings, and several key features.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 25
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Scenario and Building - Views, states, settings, and key features

Create or view a scenario using a stack plan and a floor map view. Scenario planning enables you to allocate spaces and define user assignments efficiently with different views, simple settings, and several key features.

When you create or open a scenario, the scenario is opened in a stack plan view by default. If the building for which you’re creating a scenario or viewing the scenario has floor maps configured, you can view the space allocations on the floor map directly. You can work on a scenario only if it’s owned by you or if you’re assigned as an owner by your colleague.

## Stack plan view

A stack plan is a visual representation of space allocations based on their department, cost center, workplace entity or neighborhood. The stack plan displays the different departments, cost centers, neighborhood or workplace entities of your organization in different color codes.

![Stack plan view.](../images/stack-plan-view.png "Stack plan view")

A stack plan is similar to a graph. The Y-axis of the plan shows the different floors of a building and the X-axis shows the length of the bar, which is determined from the total capacity of the building. For example, if the sum of the capacities of all the spaces is 1000, then the length of the bar is 1000 plus other spaces that are assigned to the selected bar.

When you create a scenario, you must specify on what basis you want to group your space allocations. For example, the basis can be grouped by department, cost center, or neighborhood in the **Group by** field. The stack plan displays the allocations based on this selection. The stack plan is then opened in the scenario mode directly. The scenario mode is the grouping mode that is selected in the **Group by** field. When you open a scenario that is in the Published state to review the allocations, the scenario is opened in its scenario mode by default.

You can change a scenario only if you’re the owner and if the scenario is in the Published state. If you open a scenario that is not owned by you, then you can view the plan only in a read-only mode.

In a scenario, you can view all the details related to the building such as its capacity, space count, unallocated spaces, and more. You can change your space allocations view of a scenario by using the **View by** option.

The stack plan view includes the following features:

-   **View or edit space allocations**

    View space allocations based on departments, cost centers, workplace entity or neighborhood. The spaces on a floor that belong to the same allocation are grouped as a bar. The bars on a floor are color-coded for simple identification. You can view the legend of the color codes in the right panel.

    **Important:** You can view workplace entity-based allocation only in a building stack plan view.

-   **View details**

    The details panel of a scenario contains the following:

    -   **View Options**: In this section, you can specify whether you want to edit or view a scenario. From Workplace Space Management version 1.13.0, the view-by types are sorted alphabetically by default. You can change the order or add view types from the View by Configuration \[sn\_wsd\_spcmgmt\_view\_by\_configuration\] table. For more information, see [Create a view-by configuration](../../workplace-space-management/task/create-view-by-config.md). The following options are available by default:
        -   **Edit scenario**: Option to edit the scenario. You can edit only if you’re a space planner.
        -   **View scenario**: Option to view the scenario in read-only mode. By default, the scenario is displayed based on the **Group by** selection that you specified. You can view scenarios based on the following:
            -   Assignment type
            -   Cost center
            -   Department
            -   Neighborhood
            -   Occupancy status
            -   Space functions
            -   Space status
            -   Space type
            -   Workplace Entity

                If you select Workplace Entity, you can specify the entity type to group the spaces.

    -   **Space/floor/bar details**: The details of a space such as count and capacity.
        -   **Space count**: Number of spaces. The value is derived from the values specified in the **Capacity** field of all the space records.
        -   **Total capacity**: The total capacity of the space. The values are derived from the capacities specified in the **Capacity ratio** field of all the space records. A capacity ratio can be more than 1 for a space. Which means, a space can have more than a user assigned to it. The length of a stack plan bar is determined based on the total capacity.
        -   **Capacity ratio**: The ratio of capacity determined by dividing the **Space count** and **Total capacity** values.
    -   **Assignment**: Number of users assigned to a space. The values are displayed based on your selection on the plan

        **Note:** In Workplace Space Management version 1.13.0, user profiles that have location assignments associated to schedule plans are excluded from scenario planning.

        -   **Profiles assigned**: Number of user profiles assigned to the building/floor/selected bar.
        -   **Assignment ratio**: The ratio of the people assigned to the total capacity of that building/floor/selected bar.
        -   **Unassigned spaces**: Number of unassigned spaces to the building/floor/selected bar.
        -   **Assigned profiles**: The details of the users who are assigned to the select space or spaces.
        If a scenario is grouped by neighborhood, you can also make user assignments to a neighborhood from the scenario stack plan using the **Edit user assignments** option. You can add a user, remove a user, or update a user to a neighborhood.

        If **Neighborhood** is selected as the group by option, only assignments that have the **Neighborhood assignment** type are applicable. For any other group by option, assignments that have the **Location assignment** type are applicable.

    -   **Legend**: This section depends on the view selected in the **View by** field. For example, if you select Department as the view option, then the legend of all the departments available in the building is displayed.
-   **Change views**

    Change the view of the bar based on different types. The following view types are available:

    **Note:** From Workplace Space Management version 1.13.0, the view types are sorted alphabetically by default. You can change the order or add view types from the View by Configuration \[sn\_wsd\_spcmgmt\_view\_by\_configuration\] table. For more information, see [Create a view-by configuration](../../workplace-space-management/task/create-view-by-config.md).

    -   **Assignment type**: View the spaces on a floor based on their assignment type such as permanent or flexible.
    -   **Cost center**: View the spaces on a floor based on cost centers. The bars are labeled with the different cost centers of your organization.
    -   **Department**: View the spaces on a floor based on departments. The bars are labeled with different departments of your organization.
    -   **Neighborhood**: View the spaces on a floor based on the neighborhood. The bars are labeled with different neighborhoods of your organization.
    -   **Occupancy status**: View the spaces on a floor based on the occupancy status.
    -   **Space functions**: View the spaces on a floor based on different space functions. The bars are labeled with different space functions of your organization.
    -   **Space status**: View the spaces on a floor based on their status such as active, future, retired, or temporary. The bars are labeled with the different space statuses.
    -   **Space type**: View the spaces on a floor based on their space types such as workspace/desk, room, restroom, and more. The bars are labeled with the different space types of your organization.
    -   **Workplace Entity**: View the spaces on a floor based on the Workplace Entity. After you select the Workplace Entity option, you can also select the type of entity to group the spaces.
-   **Use keyboard shortcuts**

    Click the Keyboard shortcuts icon\(![Keyboard shortcuts.](../images/keyboard-shortcut.png)\) to view the shortcuts that you can use during scenario planning. You can use keyboard shortcuts such as:

    -   Left/right keys: To navigate between stack plan bars in a row \(floor\).
    -   Up/down keys: To navigate between to the previous or next row \(floor\).
    -   Space key: To view the additional details of the highlighted stack plan bar in the tooltip.
    -   Enter: To select the highlighted stack plan bar.
-   **View the details of an allocation**

    See the details of an allocation on the plan in the details panel that is displayed on the right side. The details on the right panel of a scenario depend on the selection that you make on the plan and the **View by** option.

    -   If you select a floor, the right panel displays details such as the floor name, space count on the floor, total capacity ratio of the floor, capacity of the floor, profiles assigned, assignment ratios, unassigned spaces, and department/cost center allocated on that floor. The bar is displayed based on your view selection. The details of the bar is displayed in the bottom of the right panel. For example, if you select **Space type** as the **View by** option, the bar is displayed based on space types and the details of the space types that are assigned on a floor are displayed on the bottom of the right panel.
    -   If you select a bar, for example Department ABC, the right panel displays details such as the bar name, which is Department ABC, space count of Department ABC, capacity ratio of Department ABC, total capacity of Department ABC, profiles assigned to Department ABC, assignment ratio of Department ABC, unassigned spaces in Department ABC, color code of Department ABC.

        When you select only a bar \(Department ABC\), you can change the space count, and also assign that bar \(Department ABC\) to another floor using the **Space count** and **Assign to** fields.

    -   If you have not made any selection on the stack plan, then the overall details related to the building are displayed with the same fields as above.
-   **View unallocated spaces**

    Check unallocated spaces on a floor. Unallocated spaces are those spaces that aren’t assigned to any cost center, department, workplace entity or neighborhood. Based on the unallocated spaces you can increase or decrease the number of spaces to a department. If you allocate spaces more than the unallocated space count, then the bar doesn’t allow you to make the allocation.

    **Important:** You can view workplace entity-based allocation only in a building stack plan view.

-   **Allocate a bar to another floor**

    Move a bar from one floor to another. For example, move Department ABC from Floor 1 to Floor 5.

-   **Move a bar to the clipboard**

    Move a bar to the clipboard if you’re uncertain about its allocation. A clipboard is similar to a working space used to hold bars temporarily.

-   **Merge bars that are split**

    Combine the bars that are split in different floors to one floor, by merging. The spaces are grouped automatically.

-   **View the capacity or capacity ratio**

    Check the capacity or capacity ratio of a building, floor, or a bar.


## Building view

Not just during scenario planning, but, you can also view a building's spaces and their allocation, and various space details on a stack plan at any time. On the Space optimization dashboard, you can select the building that you want to view. The building is displayed on a stack plan. For more information, refer to [View or edit space allocations of a building](../task/view-or-edit-space-alloctions-of-a-building.md). The stack plan displays the floors of the building and the allocations like how it is displayed for a scenario. In a building view, you can perform the following actions exclusively:

-   You can view the spaces of a building based on the workplace entities that they are associated with. The **View by** option in a building view displays an addition option **Workplace entity** using which you can view the spaces. Additionally, after selection, you can specify the entity type based on which the spaces must be displayed.
-   When you select a workplace entity-based allocation on the stack plan, the details of the hierarchy of that selected space allocation and the number of spaces assigned to each parent-child hierarchy are displayed in detail.
-   You can edit user assignments of a neighborhood allocation in a building view. You can add, remove, or change the allocation of a user. For more information, refer to [Edit or view a building's spaces based on workplace entities](../task/view-a-building-s-spaces-based-on-workplace-entities.md).

## Scenario - Floor map view

View the space allocations on a floor using the floor map view. The floor map view for a floor is available only if the floor map is configured using Workplace Indoor Mapping. The floor map view makes its easier for you to view the allocations, user assignments, department/cost center/workplace entity/neighborhood movement on a floor with easy actions. Select the **Floor map** tab on the scenario plan to view the floor map.

![Floor map view.](../images/floor-map-view.png "Floor map view")

The Floor map view provides you with the following features:

-   **View the individual allocation**

    You can view the allocations of individual spaces on the map directly. The spaces are colored based on the allocation that they’re assigned to. The legend is displayed on the right panel.

-   **View any scenario**

    You can view any scenario at any time. When you open a scenario opened by others, you can view the allocations and details in a read-only mode. A scenario is opened it the scenario mode that is configured on it. You can hover over the spaces on the floor map to view the details in a tooltip.

-   **Zoom**

    Zoom in or zoom out on the map to view the allocations.

-   **Change floors**

    You can select different floors of the building using the floor selection option available on the map. If you select a floor on the stack plan and then open the Floor map view, then the floor map of that floor is displayed. If you have not made any selection on the stack plan, then the Floor 1 of the building is opened by default.

-   **Select a space**

    Select a space on the map directly and view the details of that space on the right panel. You can select a single or multiple spaces by drawing a circle \(lasso\) around them or by using the Shift key on the keyboard. The details on the Space details panel are displayed based on your selection.

    The spaces that are flexible, assigned, and unassigned spaces are highlighted with different color codes. The legend of these color codes is displayed on the map.

    While editing a scenario, you can select a check box from the space details section to select all the spaces that have the same color code.

    If a space is assigned to any user, an avatar icon is displayed with the number of users assigned to that space.

-   **Share a floor or space**

    To share a floor, select the floor on the map, then select the copy link \(![Copy link icon](../images/copy-link-icon.png)\) icon from the Space details pane. Make sure that no spaces are selected.

    To share a space, select the space on the map, then select the copy link \(![Copy link icon](../images/copy-link-icon.png)\) icon from the Space details pane. You can only share one space by using the link.

-   **View details**

    You can view the following details on the right panel:

    -   **View by**: Option to change the view of the map. The view options are determined from the space types available on a Space record. The spaces are highlighted on the map based on your selected view.
    -   **Actions**: This field is displayed only if you’ve selected a single or multiple spaces on the floor. The following options are displayed in the field:
        -   **Allocation**: Option to make allocation-related changes such as adding, changing, or removing an allocation.
        -   **Assignment type**: Option to change the assignment type such as changing a space from permanent to flex or vice versa. You can also remove the existing user assignment.
    -   **Space/floor details**: The details of a space such as count and capacity are displayed.
        -   **Space count**: Number of spaces. The value is derived from the values specified in the **Capacity** field of all the space records.
        -   **Total capacity**: The total capacity of the space. The value is derived from the capacities specified in the **Capacity ratio** field of the space records. A capacity ratio can be more than one for a space. Which means, a space can have more than one user assigned to it. The length of the bar is determined based on the total capacity.
        -   **Capacity ratio**: Ratio of capacity determined by dividing the Space count and Total capacity values.
    -   **Assignment**: Number of users assigned. The values are displayed based on your selection on the plan

        **Note:** In Workplace Space Management version 1.13.0, user profiles that have location assignments associated to schedule plans are excluded from scenario planning.

        -   **Profiles assigned**: Number of user profiles assigned on the building/floor/selected bar.
        -   **Assignment ratio**: Ratio of the people assigned on the total capacity of that building/floor/selected bar.
        -   **Unassigned spaces**: Number of unassigned spaces in the building/floor/selected bar.
        If **Neighborhood** is selected as the view by option, only assignments that have the **Neighborhood assignment** type are applicable. For any other view by option, assignments that have the **Location assignment** type are applicable.

    -   **Legend**: This section depends on the view selected in the **View by** field. For example, if you select Department as the view option, then the legend of all the Departments available on the floor is displayed.
-   **Adjust map settings**

    Change the map settings. You can switch between Floor plan view details and Map settings details on the right panel. The floor plan details displayed on the panel depend on the map settings. The following settings are available:

    -   **Assigned to**: Option to view the user or users to whom the space is assigned.
    -   **Assignment type**: Option to view the assignment type of the space that is flexible or permanent.
    -   **Opacity %**: Opacity of the colored spaces on the map. You can reduce the opacity if some map elements are hidden due to the colored spaces.
    -   **Show base map**: Option to view spaces on the map as defined in the Map Studio.
-   **Change space allocations**

    When you move a department to a floor, the spaces assigned to that department are grouped with the existing spaces of that department on the floor. You can view these space allocations on the floor department wise. You can also select a single space or multiple spaces of that department and allocate it to another department using the **Actions** option.


## Building - Floor map view

You can also view a building stack plan or a floor map at anytime and make changes specifically on the building. You can perform actions directly using the floor map of the building if the building has a Workplace Indoor Mapping floor map configured.

Similar to the scenario, the stack plan view of a building also enables you to perform space allocations, view the spaces on the floor based on various options.

The **Floor map** view of a building enables you to perform map based space administration. For more information, refer to [Map based space administration](../concept/map-based-space-administration.md).

![Floor map of a building.](../images/building-floormapview.png)

On a floor map, you can do the following:

-   You can view the spaces of the floor directly. From Workplace Space Management version 1.13.0, the view types are sorted alphabetically by default. You can change the order or add view types from the View by Configuration \[sn\_wsd\_spcmgmt\_view\_by\_configuration\] table. For more information, see [Create a view-by configuration](../../workplace-space-management/task/create-view-by-config.md). The following categories are available by default:

    -   **Assignment type**
    -   **Cost center**
    -   **Department**
    -   **Neighborhood**
    -   **Occupancy status**
    -   **Space function**
    -   **Space status**
    -   **Space type**
    -   **Workplace Entity**

        When you select **Workplace Entity**, an additional field **Workplace Entity Type** is also displayed in which you can specify the entity type, based on which you want to view the spaces.

    **Note:** In Workplace Space Management version 1.13.0, user profiles that have location assignments associated to schedule plans are excluded from the building view.

    For more information, refer to [View or edit space allocations of a building](../task/view-or-edit-space-alloctions-of-a-building.md).

-   You can edit the spaces on a floor. For more information, refer to [Edit a building's spaces using a map](../task/edit-space-details-for-buildings.md).
-   Assign or unassign an employee from a space. [Move employees on a floor or to a different floor using the map](../task/move-employees-on-a-floor-or-to-a-different-floor-using-the-map.md).
-   You can also change the opacity of the colored spaces in the **Map Settings** pane. Changing the opacity is helpful if some elements on the map are hidden due to the color.
-   You can view the base map \(as defined in the Map Studio\) from the **Map Settings** pane by selecting **Show base map**.

While viewing or editing spaces, you can select a check box from the space details section to select all the spaces that have the same color code.

## Related scenarios

The Related scenarios tab appears when you open a building using the Space Optimization module. All the scenarios related to the selected building are listed.

Details related to scenarios such as the name, state, owner, date when it was created, group for which it’s created and more are displayed. You can refresh the list, edit the columns, and apply filters.

## Scenario states

A scenario, since its creation to the deployment, undergoes different state changes based on the actions implemented on it. Based on the state of a scenario, you can share it with your colleagues or stake holders to review the plan and implement it on the main production data.

A scenario has the following states:

-   **Processing**: A scenario is set to **Processing** when its creation is in process. Also, if you’re copying an existing scenario, then during the copying process, the newly created scenario is set to **Processing**.

    Also, at any time, when a scenario is saved, the state of the scenario will be set to **Processing** when the saving process in running.

-   **Draft**: A scenario is set to Draft when it’s ready to use, that is, when it’s being worked on. During this state, only the owner of the scenario can view it.
-   **Ready**: A scenario is set to Ready when it’s published. When a scenario is published and after the scenario is set to the Ready state, you can share it with your colleagues or stake holders for their feedback. The scenario is available only in read-only mode to others.
-   **Awaiting approval**: A scenario is set to Awaiting approval when it is sent for approval after publishing. When a scenario is sent for approval, the scenario can no longer be edited unless the state changes to Rejected.
-   **Rejected**: A scenario is set to Rejected if an approver has rejected the scenario. When the scenario is rejected, you can implement the changes suggested by the approver using their comments and send it for approval again.
-   **Approved**: A scenario is set to Approved if an approver approves the scenario. When a scenario is approved, you can no longer edit a scenario. You can only deploy a scenario.
-   **Deployed**: A scenario is set to Deployed when it’s deployed to the main production data. You can’t make any changes to a deployed scenario. To make any changes, you must create a copy of that scenario and make changes.
-   **Archived**: A deployed scenario is set to Archived if it’s older than six months.

## Settings

The Settings tab appears when you open a building directly using the Space Optimization module. The Settings tab enables you to apply the space qualifying filter on the spaces displayed on the stack plan. You can apply a filter based on what type of spaces or how you want to see the spaces.

For example, if you want to see all the spaces of type workplace/desk then apply the Space type filter. In the Stack plan tab, these spaces are displayed based on the view that you’ve selected in the **View by** option.

## Approver

The Approver tab displays details of all the approvers who are configured to approve a scenario. The Approver tab displays details such as the approvers who are allowed to approve, the state of the approval, the comments related to the approval and the time of approval. After you send a scenario for approval, if the scenario is rejected by the approver, you can view the details of the rejection in the **Comments** of the Approver tab and implement the changes.

The application provides a default approval definition **Scenario Plan Approval**, in which workplace managers are configured as approvers for scenarios. You can create a new approval definition or edit the default defintion. To create a new approval definition, refer to [Create an approval definition](../../workplace-service-delivery/task/create-approval-defintion.md).

**Note:** To add an approver to the approval definition, the approver must be configured in the performer criteria. To do so, refer to [Create a workplace performer criteria](../../workplace-service-delivery/task/create-workplace-performer-criteria.md).

## Space Deployment plan and User Deployment plan

The Space Deployment plan and User Deployment plan tabs appear when you are creating a scenario. The changes that you make on a scenario are logged in the respective deployment plans. After you save the changes made on the stack plan, the plan displays each change with the changed details.

**Space Deployment Tab**: The plan displays the allocations and space assignment type changes performed on the scenario.

**User Deployment Tab**: The plan displays the user assignment-related changes such as Add, Update, and Delete performed on the scenario.

After publishing the changes, and after finalizing the space allocations, to execute it to production, you must deploy the changes. The plan enables you to deploy the changes using the **Deploy** option.

After the scenario is deployed, a workplace case is created for every change. After the deployment, additional details such as the workplace cases associated with each change are displayed in the deployment plans. The following workplace move cases are created for each change accordingly:

-   Workplace User Assignment and Move Service via Scenario Planning: Workplace move case created to change the user assignment and move the space.
-   Workplace Assignment Type Service: Workplace case created to change the assignment type of a space.
-   Workplace Allocation Change Service: Workplace case created to change the space allocation.

**Parent Topic:**[Workplace Central reference](../concept/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central](components-installed-with-workplace-central.md)

[Space Optimization - Key features and actions](space-optmization-features-and-actions-.md)

[Workplace Central Event planner](event-planner-key-features-actions-views.md)

[Space request approvals, states, actions, and key features](space-request-states-and-view.md)

[Move management key features and actions](move-mgmt-views-states-actions.md)

[Case Management - Key features, Actions &amp; Case details](case-management-key-features-actions-case-details.md)

[Schedule Plan details form](schedule-plan-details-form.md)

[Scenario details form](scenario-details-form.md)

[Space Deployment Plan](space-deployment-plan.md)

[User Deployment Plan](user-deployment-plan.md)

[Excel column lengths for move projects](move-excel-char-limit.md)

[Move conflicts for projects created via Excel upload](excel-upload-conflicts.md)

[Workplace Central troubleshooting](workplace-central-troubleshooting.md)

[Workplace Task form - Space Assignment task](workplace-task-space-assignment.md)

[Neighborhood User Assignment Rule form](user-assignment-rule-form.md)

[User Workplace Profile form](user-workplace-profile-form.md)

