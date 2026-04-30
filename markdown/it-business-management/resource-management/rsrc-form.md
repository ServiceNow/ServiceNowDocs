---
title: Resource form
description: Use the resource form to create an operational resource plans.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Resource Management reference, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource form

Use the resource form to create an operational resource plans.

<table id="table_OperationalResourcePlanFieldFormDescriptions"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated identification number for the operational resource plan.

</td></tr><tr><td>

Resource type

</td><td>

Resource category. To select a group, select the **Group** option. To select an individual user, select the **User** option. To select a resource by role, select **Role**.

</td></tr><tr><td>

Group

</td><td>

Group for which the operational resource plan is created.If you select **Role** in the **Resource type** field, then the choice list displays the groups for the selected role.

</td></tr><tr><td>

User

</td><td>

User for whom the operational resource plan is created. This option appears if you select **User** in the **Resource type** field.

</td></tr><tr><td>

Role

</td><td>

Specific [resource role](../task/create-resource-role.md) that you want to associate with the plan. This option appears if you select **Group** or **Role** in the **Resource type** field.If you select **Group** in the **Resource type** field, then the choice list displays the roles for the selected group.

</td></tr><tr><td>

Members preference

</td><td>

Specific members or all members from the selected group or role. The default is set to **All members**. This field appears only when the **Group** or **Role** option is selected in the **Resource type** field.-   If the **All members** option is selected, the resource plan includes all members of the selected group or role. Time is proportionally divided among the selected group or role members, depending upon their capacity. Before making the hard allocation, if all members are not required, as a resource manager, you can select only specific members from the group or role.
-   If the **Specific member** option is selected, a request is made for the specified members. The requested hours are proportionately split among specified users of the group or role, based on their available capacity.

</td></tr><tr><td>

Skills

</td><td>

Specific skill\(s\) that you want to associate with the plan. This field appears only when the **All members** option is selected in the **Members preference** field.For more information on skills management, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Request type

</td><td>

Type of request: **Hourly** or **% Capacity**. To estimate the work in hours, select the **Hourly** option. To estimate the work in percentage of capacity, select the **%Capacity** option.

</td></tr><tr><td>

Planned hours

</td><td>

Estimated number of hours required to complete the operational work.

</td></tr><tr><td>

Confirmed/Allocated hours

</td><td>

Hours of a resource confirmed or allocated for operational work.

</td></tr><tr><td>

Actual hours

</td><td>

Hours spent on a planned operational task.**Note:** When you submit a time card, upon approval of the time card, actual hours are updated for an allocation record of an operational resource plan.

</td></tr><tr><td>

Name

</td><td>

Descriptive name for the operational resource plan.

</td></tr><tr><td>

Operational work type

</td><td>

Type of operational work: KTLO, Admin, Meeting, Training, Out of office, External labor, Time off, Appointment, and Phone call. The default is **KTLO**.

</td></tr><tr><td>

Rate model

</td><td>

Rate model assigned to the operational resource plan. The [rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md) is used to derive hourly rates for the resource plan.If you change or remove the rate model assigned to an operational resource plan, the cost fields on the plan are re-calculated.

</td></tr><tr><td>

Start date

</td><td>

Date when the operational resource plan starts.

</td></tr><tr><td>

End date

</td><td>

Date when the operational resource plan ends.

</td></tr><tr><td>

Allocation type

</td><td>

Resource distribution type that determines the type of allocation records. The value in this field determines how the planned hours are distributed across the resource plan duration, among requested resources. Select any of the following options:-   **Weekly**: Creates week-long allocations up to the end of the planned end date.
-   **Monthly**: Creates month-long allocations up to the end of the planned end date. Monthly is the default value.
-   **Plan Duration**: Creates one allocation for each user for the entire duration of the resource plan.

 For example, if a resource is requested from Jan. 1st to Mar. 31st, the following records are created for each type:

-   **Monthly**: 3 allocation records, one for each month.
-   **Weekly**: 14 allocation records, one for each week with Monday being first day of the week.
-   **Plan Duration**: Only 1 record for the entire duration of the resource plan.

</td></tr><tr><td>

Allocation spread

</td><td>

Type of allocation spread. The value in this field determines the manner in which the allocated hours are spread while creating hard allocations:-   **Even**: Creates resource events for the resource by splitting the hours evenly across all the working days for the allocation duration.
-   **Front Load**: Creates resource events for the resource by filling up all the available slots of the resource from the start date of the allocation.

 For example, if a resource is requested for 30 hours in week 10, then:

-   Selecting **Even** equally divides 30 hours between all weekdays, which is 6 hours per day for a five-day work week.
-   Selecting **Front Load**consumes all the available hours on Monday, moves on to Tuesday, and so on, until all the 30 hours are allocated. If the resource is not available for 30 hours in week 10, it over-allocates by filling up the remaining hours from the start date up to 24 hours per day.

</td></tr><tr><td>

State

</td><td>

A plan starts in the **Planning** state. The plan moves to the Requested state after its submission.

</td></tr><tr><td>

Planned cost

</td><td>

Amount, in **Planned Hours**, multiplied by the hourly rate of the specified user or group resource. Planned cost is a first draft estimate of the resource plan cost.Planned cost is rolled up from Requested Allocations for plans in the Planning or Requested states and from resource allocations for plans in the Allocated state.

The hourly rate is derived from one of the following sources:-   [Rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md), if it is populated on the operational resource plan.
-   Labor rate card, if rate model is not available.
-   System property **com.snc.time\_card.default\_rate** if all the other conditions fail.

 **Note:** When requesting resources from a group, if a resource role is specified, the planned cost is calculated from the hourly rate of the specified role.

</td></tr><tr><td>

Confirmed/Allocated cost

</td><td>

Amount of confirmed or allocated hours multiplied by the hourly rate of the confirmed or allocated resources. Provides a more accurate estimation of the cost of the plan that is confirmed or allocated. The hourly rate is derived from one of the following sources:

 -   [Rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md), if it is populated on the operational resource plan.
-   Labor rate card, if rate model is not available.
-   System property **com.snc.time\_card.default\_rate** if all the other conditions fail.

</td></tr><tr><td>

Actual cost

</td><td>

Amount of actual hours multiplied by the hourly rate of the specified resource.**Note:** When you submit a time card, upon approval of the time card, actual cost is updated for an allocation record of an operational resource plan.

</td></tr><tr><td>

Notes

</td><td>

Additional correspondence and information.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Copy Resource Plan|Copies the opened resource plan to create a new resource plan.|

<table id="table_zdk_zr1_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requested Allocations

</td><td>

List of [requested allocations](../task/request-allocation.md) for the resource plan.The number of requested allocation records created depends on the value in the **Allocations type** field. For example, if a resource is requested from Jan first to Mar. 31st, the following requested allocation records are created for each type:

-   Monthly: 3 allocation records, one for each month.
-   Weekly: 14 allocation records, one for each week with Monday being the first day of the week.
-   Plan Duration: Only 1 record for the entire planned duration of the resource plan.

</td></tr><tr><td>

Resource Allocations

</td><td>

List of [resources allocated](r_AllocatingResources.md) to the plan.

</td></tr></tbody>
</table>**Parent Topic:**[Resource Management reference](../task/rsrc-mgmt-reference.md)

