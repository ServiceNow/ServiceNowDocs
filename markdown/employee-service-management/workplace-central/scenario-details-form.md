---
title: Scenario details form
description: Use the scenario details form to select the scenario owner, location, group by selection, and space selection criteria.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2025-03-25"
reading_time_minutes: 4
breadcrumb: [Workplace Central reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Scenario details form

Use the scenario details form to select the scenario owner, location, group by selection, and space selection criteria.

<table id="table_sfz_b5n_1vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scenario name

</td><td>

Name of the scenario

</td></tr><tr><td>

Scenario owner

</td><td>

Scenario owner's name or ID. This is a read-only field and auto-populated. After the scenario is created, the field name changes to **Owned by**. After the scenario is created, you can assign it to another user.

</td></tr><tr><td>

Locations

</td><td>

Locations that are added to the scenario.This field is displayed after a scenario is created.

The locations are displayed based on the **Space Selection Criteria** of the scenario.

</td></tr><tr><td>

Group by

</td><td>

Option to select and group a scenario based on the allocation type. After the scenario is created, this field becomes read-only.Allocation types are defined in the **sn\_wsd\_core.ALLOCATION\_TYPE** system property.

-   Department
-   Cost center
-   Neighborhood
-   Workplace Entity

If you select Workplace Entity as the group by option, the bars of the stack plan are displayed based on the lowest node in the hierarchy. For example, if the hierarchy for spaces is `Corporate\Europe\Information Technology\IT Support`, the bars are displayed for `IT Support`.


**Note:**

-   If Neighborhood is selected as the group by option, only assignments that have the Neighborhood assignment type are applicable. For any other group by option, assignments that have the Location assignment type are applicable.
-   Creating or viewing a scenario based on workplace entities is supported from Workplace Space Management version 1.15.0. Workplace Entity is not supported for scenarios created in earlier versions.

For earlier versions, you can view spaces based on their workplace entities for a building. For more information, see [Edit or view a building's spaces based on workplace entities](../task/view-a-building-s-spaces-based-on-workplace-entities.md).


</td></tr><tr><td>

Space Selection Criteria

</td><td>

Option to apply filter and select locations for a scenario.-   Select field: Select campus, building, or floor as required. For example: Building is B1A2.

You can select and add multiple buildings using the space selection criteria.

-   Select operator: Select **And** **Or** operators as required.
-   Enter value: Option to provide the value for the selected field. For example, if you select Building, then enter the value as the name of the building \(Building A\).

Location names are displayed based on the filter conditions. Select the refresh icon \( ![Refresh icon to refresh the filter criteria and get locations for multi-building scenario.](../images/refresh-icon.png)\) to view results matching filter conditions.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Central reference](../concept/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central](components-installed-with-workplace-central.md)

[Space Optimization - Key features and actions](space-optmization-features-and-actions-.md)

[Workplace Central Event planner](event-planner-key-features-actions-views.md)

[Scenario and Building - Views, states, settings, and key features](scenario-planning-views-actions-keyfeatures-.md)

[Space request approvals, states, actions, and key features](space-request-states-and-view.md)

[Move management key features and actions](move-mgmt-views-states-actions.md)

[Case Management - Key features, Actions &amp; Case details](case-management-key-features-actions-case-details.md)

[Schedule Plan details form](schedule-plan-details-form.md)

[Space Deployment Plan](space-deployment-plan.md)

[User Deployment Plan](user-deployment-plan.md)

[Excel column lengths for move projects](move-excel-char-limit.md)

[Move conflicts for projects created via Excel upload](excel-upload-conflicts.md)

[Workplace Central troubleshooting](workplace-central-troubleshooting.md)

