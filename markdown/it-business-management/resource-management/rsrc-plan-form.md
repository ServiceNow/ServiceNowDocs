---
title: Resource Plan form
description: Field descriptions for the resource plan form fields.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Resource Management reference, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource Plan form

Field descriptions for the resource plan form fields.

<table id="table_ResourcePlanFieldFormDescriptions"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated identification number for the plan.

</td></tr><tr><td>

Resource type

</td><td>

Category of resource. To select a group, select **Group**. To select an individual user, select **User**. To select a resource by role, select **Role**.

</td></tr><tr><td>

Group

</td><td>

Specific group resource to associate with the plan.If you select **Role** in the **Resource type** field, then the **Group** list contains groups only for the selected role.

</td></tr><tr><td>

User

</td><td>

Specific user resource to associate with the plan. This field appears if you select **User** in the **Resource type** field.

</td></tr><tr><td>

Role

</td><td>

Specific [resource role](../task/create-resource-role.md) that you want to associate with the plan. This field appears if you select **Role** in the **Resource type** field.

</td></tr><tr><td>

Members preference

</td><td>

Specific members, any member, or all members from the selected group or role. The default is **All members**. This field appears only when the **Group** or **Role** option is selected in the **Resource type** field.

 -   To request all members of a group or role, select **All members**. The requested time gets split among all members of the selected group or role proportionally depending on their capacity. Before making the hard allocation, if all members are not required, the resource manager can select only the desired members of the group or role.
-   To request specific members of a group or role, select **Specific members**, and then select members from the **Members list**. The requested time gets split among the selected members of the selected group or role proportionally depending on their capacity.
-   To select any member of a group or role, select **Any member**. Resources that are most available during the plan duration are requested first. Soft allocation is created only for these resources on confirmation.

 For more information about the effect of members preference on the calculation of hours for soft and hard allocations, see [Resource allocation](r_AllocatingResources.md).

**Note:** This field is not available by default on the form when opened from the resource grid. If required, you can configure these fields. If the resource plan is created from the list view, the fields are already available.

</td></tr><tr><td>

Skills

</td><td>

Specific skills the requested resources should possess to allocate them to the resource plan. This field appears if you select **Group** or **Role** in the **Resource type** field, and **All members** or **Any member** in the **Members preference** field.

 For more information, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Request type

</td><td>

Type of request. To specify a request in hours, select **Hours**. To specify a request in full-time equivalents, select **FTE**.

</td></tr><tr><td>

FTE

</td><td>

Number of units for the full-time equivalent selection. This field appears if you select **FTE** in the **Request type** field.

 For more information, see [Resource plans](../concept/c_ResourcePlans.md).

</td></tr><tr><td>

Planned hours

</td><td>

Estimated number of work hours required to complete all resource plan work.**Note:** If all users in a resource plan have the same schedule and that schedule is different from the resource management schedule, then the user's schedule is considered to calculate planned hours,

</td></tr><tr><td>

Name

</td><td>

Descriptive name for the plan. If you do not enter a name, the name becomes the **Number** + **Short description**. If the short description for the task is empty, the plan number is used.

</td></tr><tr><td>

Task

</td><td>

Task to which the plan applies. If the resource plan was created from a project task, the task number appears here.

</td></tr><tr><td>

Start Date

</td><td>

Start date for the resource plan. By default, this field shows the **Planned start date** of the associated project record or task record. Edit the default date, if necessary.**Note:** The start date of the resource plan cannot be before the project or demand start date if the **Do not allow resource plan dates to be outside the Project/Demand dates** property is enabled.

</td></tr><tr><td>

End Date

</td><td>

End date for the resource plan. By default, the date is derived from the **Planned end date** of the associated project record or task record. Edit the default date, if necessary.**Note:** The end date of the resource plan cannot be after the project or demand start date if the **Do not allow resource plan dates to be outside the Project/Demand dates** property is enabled.

</td></tr><tr><td>

Allocation spread

</td><td>

Type of hard allocation. The value in this field determines the manner in which the allocated hours are spread while creating hard allocations. Select either option:-   **Even**: Create resource events for the resource by splitting the hours evenly across all working days for the allocation duration.
-   **Front load**: Create resource events for the resource by filling up all available slots of the resource from the start date of the allocation.

 For example, if a resource is requested for 30 hours in Week 10:

-   Selecting **Even** equally divides 30 hours to all weekdays, that is, 6 hours per day for a five-day work week.
-   Selecting **Front load** first consumes all available hours on Monday, then move on to Tuesday, and so on, until all 30 hours are allocated. If the resource is not available for 30 hours in Week 10, Front load over-allocates by filling up the remaining hours from start date up to 24 hours per day.

**Note:** This field is not available by default on the form when opened from the resource grid. If required, you can configure these fields. If the resource plan is created from the list view, the fields are already available.


</td></tr><tr><td>

State

</td><td>

State of the resource plan. The plan starts in the Planning state.

**Note:** This field is not available by default on the form when opened from the resource grid. If required, you can configure these fields. If the resource plan is created from the list view, the fields are already available.

</td></tr><tr><td>

Rate override

</td><td>

Option for overriding the hourly rate derived from the rate model or the labor rate card.

 When the option is selected,

-   The planned, confirmed, and allocated costs of the resource plan is derived from the rate specified in the **Resource Rate** field.
-   When the user submits the time card for the resource plan, the rate specified in the **Resource Rate** field is used to calculate the actual cost of the resource plan.

 The option is enabled only if the resource plan is in the Planned state.

 By default, the option is not selected.

</td></tr><tr><td>

Resource rate

</td><td>

Hourly rate of resource that overrides the hourly rate returned from the rate model to calculate the planned and actual costs of the resource plan.This field appears when the **Rate override** option is selected. If you clear the **Rate override** check box, the resource rate value is also cleared and removed from all calculations. On selecting the **Rate override** check box again, the previous resource rate is not retrieved.

</td></tr></tbody>
</table>**Note:** The **Members Preference**, **Allocation spread**, and **State** fields are not available by default on the form when opened from the resource grid. If required, you can configure these fields. If the resource plan is created from the list view, the fields are already available.

-   **[Resource Plan form tabs](rsrc-plan-form-tabs.md)**  
Use the resource plan form tabs to create a resource plan.

**Parent Topic:**[Resource Management reference](../task/rsrc-mgmt-reference.md)

