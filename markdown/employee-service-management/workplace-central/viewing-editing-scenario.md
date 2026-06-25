---
title: Viewing or editing a scenario
description: You can view the details like the floor details and space KPIs. You can edit a scenario to allocate spaces to projects and neighborhoods, assign spaces to users, or edit space assignments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/viewing-editing-scenario.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 6
breadcrumb: [Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Viewing or editing a scenario

You can view the details like the floor details and space KPIs. You can edit a scenario to allocate spaces to projects and neighborhoods, assign spaces to users, or edit space assignments.

**Important:** If allocation changes in your instance impact the scenario, the system displays a warning on the Space Details panel. You must review the changes, edit the scenario accordingly, then select **Move to valid** before continuing. For more information about allocation changes, see [Reviewing allocation changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/reviewing-allocation-changes.md).

\[Omitted image "wsd-central-review-changes.png"\] Alt text: Space details panel displaying a warning about reviewing allocation changes.

## Viewing a scenario

While viewing a scenario, you can select a **View by** option to group spaces on the stack plan or the floor map. If you select Workplace Entity, you can also select the entity level that you want to use to view the scenario. The scenario displays all entity levels by default.

You can view a scenario on the stack plan, or on the floor map. For more information about stack plans and floor maps, see [Scenario and Building - Views, states, settings, and key features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/scenario-planning-views-actions-keyfeatures-.md).

The Space details panel displays information about the spaces and profile assignments for a scenario. When you select a building, floor, or bar on the stack plan, the information is updated based on your selection.

\[Omitted image "stack-plan-view.png"\] Alt text: Scenario planning on Workplace Central with the Stack plan tab selected. The space details tab displays the view options and KPIs for spaces and profile assignments.

When you select spaces on the floor map, the Space details panel displays information based on your selection.

\[Omitted image "floor-map-view.png"\] Alt text: Scenario planning on Workplace Central with the Floor map tab selected. The space details tab displays the view options and KPIs for the selected spaces and profile assignments.

The information on the Space details panel is displayed in cards. You can also view the cards while editing the scenario.

-   The first card displays the space count, the total capacity, and the ratio of the capacity to the spaces.

    The name of the card changes based on your selection in the stack plan or floor map.

-   The **Assignment** card displays the number of profiles assigned to the selected spaces, the number of unassigned spaces, and the assignment ratio of users to spaces.
-   The legend card displays the allocations on the selected area of the stack plan or floor map.

    The name of the card changes based on your selection in the stack plan or floor map.

    If the view by option is Workplace Entity, you can view the hierarchy by selecting the tree icon \(\[Omitted image "wsd-central-tree-icon.png"\] Alt text: Tree icon.\) on the legend card.


## Editing a scenario

While editing a scenario, the **Group by** option is used to allocate spaces based on the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property.

For example, if the **Group by** option is **Neighborhood**, then neighborhoods are available for you to edit in the Stack plan tab of the scenario.

You can edit a scenario by using the stack plan, or by using the floor map. For more information about stack plans and floor maps, see [Scenario and Building - Views, states, settings, and key features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/scenario-planning-views-actions-keyfeatures-.md).

-   If **Neighborhood** is selected as the group by option, only assignments that have the **Neighborhood assignment** type are applicable. For any other group by option, assignments that have the **Location assignment** type are applicable.

-   Editing a scenario based on workplace entities is supported from Workplace Space Management version 1.15.0. For earlier versions, you can view spaces based on their workplace entities for a building. For more information, see [Edit or view a building's spaces based on workplace entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/view-a-building-s-spaces-based-on-workplace-entities.md)
-   If you select Workplace Entity as the group by option, the bars of the stack plan are displayed based on the lowest node in the hierarchy. For example, if the hierarchy for the spaces is `Corporate\Europe\Information Technology\IT Support`, the bars are displayed for `IT Support`. While editing a scenario, you can select the entity level that you want to use for the stack plan.

For more information about editing a scenario, see either of the following topics.

-   **[Edit a scenario using the stack plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)**  
Edit a scenario using the stack plan to allocate spaces to departments, cost centers, workplace entities, or neighborhoods.
-   **[Edit a scenario using the floor map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)**  
Edit a scenario using the floor map to add or remove allocations, or to assign users to spaces in your organization.
-   **[Edit user assignments of a neighborhood](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/add-or-edit-user-assignments-of-a-neighbourhood.md)**  
Add a user to a neighborhood or edit the existing user assignments of a neighborhood in a building.

**Parent Topic:**[Working with Space Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/working-with-space-optimization.md)

**Related topics**  


[Create a scenario]()

[Review a scenario]()

[Publish a scenario]()

[Send a scenario for approval]()

[Change owner of a scenario]()

[Deploy a scenario]()

[View scenario change details]()

[Create a copy of an existing scenario]()

[View or edit space allocations of a building]()

[Work on a space assist request]()

[Map based space administration]()

