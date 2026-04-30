---
title: Resource Plan form tabs
description: Use the resource plan form tabs to create a resource plan.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Resource Plan form, Resource Management reference, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource Plan form tabs

Use the resource plan form tabs to create a resource plan.

<table id="table_cdm_dm1_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource type

</td><td>

Type of resource selected during the creation of resource plan.

</td></tr><tr><td>

Group

</td><td>

Group associated with the resource plan.

</td></tr><tr><td>

Role

</td><td>

Role associated with a role resource plan.

</td></tr><tr><td>

User

</td><td>

User associated with a user resource plan.

</td></tr><tr><td>

Skills

</td><td>

Skills that the requested resources possess to allocate them to the resource plan.**Note:** This field is only available for resource plans with all or any members preference.

</td></tr><tr><td>

Members preference

</td><td>

Specific members, any member, or all members from the selected group or role.

</td></tr><tr><td>

Members list

</td><td>

Resources selected as specific members for specific members preference resource plan.

</td></tr><tr><td>

Confirmed/Allocated users

</td><td>

Resources that are confirmed/allocated by the resource manager for resource plans. By default, this field is displayed for specific members preference type of resource plans.

</td></tr></tbody>
</table><table id="table_vp2_sp1_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Request type

</td><td>

Type of request selected during the creation of resource plan.-   If you select **FTE** in the **Request Type** field, the **FTE** field is displayed.
-   If you select **Person Days** in the **Request Type** field, the **Person days** field is displayed.

</td></tr><tr><td>

Planned hours

</td><td>

Estimated number of work hours required to complete all resource plan work.

</td></tr><tr><td>

Confirmed/Allocated hours

</td><td>

Confirmed or allocated hours rolled up from resource allocations.

</td></tr><tr><td>

Actual hours

</td><td>

Actual hours rolled up from time card entries.

</td></tr><tr><td>

FTE

</td><td>

Number of units for the full-time equivalent selection.

</td></tr><tr><td>

Demand currency

</td><td>

Type of currency associated with the demand task when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and Demand Currency view is enabled. For more information, see the [Multicurrency in Demand Management](../../planning-and-policy/concept/multicurrency-demand.md) topic.

</td></tr><tr><td>

Project currency

</td><td>

Type of currency associated with the project or project task when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and Project Currency view is enabled. For more information, see the [Multicurrency in Project Management](../../project-portfolio-suite-with-financials/concept/multicurrency-pps.md) topic.

</td></tr><tr><td>

Planned cost

</td><td>

Amount in **Planned hours** multiplied by the hourly rate of the specified user or group resource. This amount is a first-draft estimate of the resource plan cost. The hourly rate is derived from one of the following sources:

-   If the **Rate override** option is selected, the hourly rate specified in the **Resource rate** field is used.
-   If a [rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md) is populated on the project or demand to which the resource plan is associated, the hourly rate is derived from the rate model.
-   If the resource plan is assigned to a specific user and the time sheet policy of the user is set for multiple rate types, the planned cost is determined using the labor rate card with the default rate type. If the default rate type is inactive, the system rate is used to determine the planned cost.
-   If the resource plan is assigned to a specific user and the time sheet policy of the user is not set for multiple rate types, the planned cost is determined using the labor rate card with no rate type. Otherwise, the system rate is used.
-   If the hourly rate is in non-functional currency, budget reference rates are used.

**Note:** Setting up rates for resources would provide more accurate forecast and plan costs for resource plans.

 Planned cost is rolled up from Requested Allocations for plans in the Planning or Requested state and from Resource allocations for plans in the Confirmed or Allocated state. While requesting resources from a group, if a resource role is specified, the planned cost is calculated from the hourly rate of the specified role.

</td></tr><tr><td>

Planned cost in demand currency

</td><td>

Planned cost of a resource plan associated to a demand or demand task in the demand currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Demand Currency view is enabled. The Planned cost in demand currency value is derived by multiplying planned hours with the hourly rate of the specified user or group resource, and then converting the result to the demand currency based on the budget reference rates.

</td></tr><tr><td>

Planned cost in project currency

</td><td>

Planned cost of a resource plan associated to a project or project task in the project currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Project Currency view is enabled. The Planned cost in project currency value is derived by multiplying planned hours with the hourly rate of the specified user or group resource, and then converting the result to the project currency based on the budget reference rates.

</td></tr><tr><td>

Confirmed/Allocated cost

</td><td>

Amount of confirmed or allocated hours multiplied by the hourly rate of the confirmed or allocated resources. Provides a more accurate estimation of the cost of the plan that is confirmed or allocated.-   If the **Rate override** option is selected, the hourly rate specified in the **Resource rate** field is used.
-   If a rate model is populated on the project or demand to which the resource plan is associated, the hourly rate is derived from the rate model.
-   If rate model is not available, labor rate card determines the hourly rate.
-   If no labor card is found for the user, the hourly rate is taken from the following time card property: **Default hourly rate used when processing time cards if we can't get a rate from labor rate cards \(in system currency\)**.

</td></tr><tr><td>

Confirmed/Allocated cost in demand currency

</td><td>

Confirmed or allocated cost of a resource plan associated to a demand or demand task in the demand currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Demand Currency view is enabled. The Confirmed/Allocated cost in demand currency value is derived by multiplying the confirmed or allocated hours with the hourly rate of the confirmed or allocated resources, and then converting the result to the demand currency based on the budget reference rates.

</td></tr><tr><td>

Confirmed/Allocated cost in project currency

</td><td>

Confirmed or allocated cost of a resource plan associated to a project or project task in the project currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Project Currency view is enabled. The Confirmed/Allocated cost in project currency value is derived by multiplying the confirmed or allocated hours with the hourly rate of the confirmed or allocated resources, and then converting the result to the project currency based on the budget reference rates.

</td></tr><tr><td>

Actual cost

</td><td>

Based on the same time cards used for the Actual hours, the actual cost is calculated using the hourly rate of each user and the hours worked. Used to inform resource requesters and resource managers of actual costs based on the actual hours that user resources added on their approved time cards.The hourly rate is derived as:

-   If the **Rate override** option is selected, the hourly rate specified in the **Resource rate** field is used.
-   If a rate model is populated on the project or demand to which the resource plan is associated, the hourly rate is derived from the rate model.
-   If the time sheet policy of a user is set for multiple rate types, the actual cost is determined using the labor rate card with the default rate type.
-   If the default rate type is inactive, the system rate is used to determine the actual cost.
-   If the time sheet policy of a user is set for multiple rate types, the actual cost is determined using the labor rate card with no rate type. Otherwise, the system rate is used.

</td></tr><tr><td>

Actual cost in demand currency

</td><td>

Actual cost of a resource plan associated to demand or demand task in the demand currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Demand Currency view is enabled. The Actual cost in demand currency value is derived by multiplying the hourly rate of each user with the hours worked, and then converting the result to the demand currency based on the exchange rates.

</td></tr><tr><td>

Actual cost in project currency

</td><td>

Actual cost of a resource plan associated to a project or project task in the project currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Project Currency view is enabled. The Actual cost in project currency value is derived by multiplying the hourly rate of each user with the hours worked, and then converting the result to the project currency based on the exchange rates.

</td></tr></tbody>
</table><table id="table_iq1_zp1_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Allocation type

</td><td>

Type of resource distribution across the project that determines the type of allocation records. The value in this field determines how the planned hours are distributed across resource plan duration among requested resources:-   **Weekly**: Create week-long allocations up to the end of the planned end date.
-   **Monthly**: Create month-long allocations up to the end of the planned end date. \(Default value.\)
-   **Plan Duration**: Create one allocation for each user for the entire duration of the resource plan.

 For example, if a resource is requested from January 1 to March 31, the following records would be created for each type:

-   **Monthly**: 3 allocation records, one for each month.
-   **Weekly**: 14 allocation records, one for each week with Monday being the first day of the week.
-   **Plan duration**: Only 1 record for the entire duration of the resource plan.

</td></tr><tr><td>

Allocation spread

</td><td>

Type of hard allocation selected during the creation of the resource plan.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Notes|Other correspondence and notes about the resource plan.|

**Parent Topic:**[Resource Plan form](rsrc-plan-form.md)

