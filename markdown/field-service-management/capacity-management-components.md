---
title: Field Service Capacity and Reservations Management components
description: Several types of components are installed with the Field Service Capacity and Reservations Management feature, including tables, business rules, scheduled jobs, and script includes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Capacity and Reservations Management components

Several types of components are installed with the Field Service Capacity and Reservations Management feature, including tables, business rules, scheduled jobs, and script includes.

Install the Field Service Contractor Management plugin \(com.snc.fsm\_contractor\_management\) to take the external groups into account while reserving, defining, and assigning the work capacity. For more information, see [Activate Field Service Contractor Management](../task/activate-contractor-management-plugin.md).

Activation of Field Service Capacity and Reservations Management adds the Capacity Management menu to the application navigator and the following modules:

-   **Capacity Reservations**: Reserve a capacity percentage of a group or agents availability to meet specific demands. For example, 60% for Break-Fix Work types and 40% for Install work types.
-   **Capacity Definitions**: Allocate the correct amount of work to internal or external work groups based on defined hours, task count, or agent work schedules. You can define capacity for a day, week, month, or year.
-   **Capacity Assignments**: Assign the capacity and capacity reservations to internal work groups and external groups of contractor companies.
-   **Capacity Usages**: View the record of capacity used by different groups and agents.

**Note:** You must select **using dynamic scheduling** in the **Assignment method for tasks** configuration option to enable your application to distribute work based on the capacity management rules.

## Tables

Capacity management adds the following tables.

<table id="table_h1q_d3c_vmb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capacity Assignment\[wm\_capacity\_assignment\]

</td><td>

Stores capacity definition assignments to groups within a specific time period to help avoid conflicts in capacity in a given time period by validating the **effective from** and **effective to** dates.

</td></tr><tr><td>

Capacity Definition\[wm\_capacity\_definition\]

</td><td>

Stores the details like source of capacity, allocation schedule, frequency of capacity definitions of a group or internal field service agent and the reservation rules to be used while assigning tasks.

</td></tr><tr><td>

Demand Channel\[wm\_demand\_channel\]

</td><td>

Stores the details like name, conditions, and order of execution of a demand channel.

</td></tr><tr><td>

Capacity Demand Metrics\[wm\_capacity\_for\_demand\]

</td><td>

Stores the metrics data for all capacity assignments.

</td></tr><tr><td>

Capacity Reservation\[wm\_capacity\_reservation\]

</td><td>

Stores the reservation definition and exclusion conditions.

</td></tr><tr><td>

Capacity Reservation Rule\[wm\_capacity\_reservation\_rule\]

</td><td>

Stores the reservation rules and the conditions for which the reservations should be used.

</td></tr><tr><td>

Capacity Usage\[wm\_capacity\_usage\]

</td><td>

Stores the capacity used by an internal field service agent or a group within a specific time period.

</td></tr></tbody>
</table>## Business rules

Capacity management adds the following business rules.

<table id="table_axb_clr_jnb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Avoid Conflict in Capacity Time Period

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td><td>

Monitor the time period defined for the Capacity Assignment to ensure that any group does not have multiple capacity assignments in the same time period or overlapping intervals.

</td></tr><tr><td>

Update Capacity on task change

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Add or update capacity when a task is assigned or unassigned. You can update capacity when the estimated work or travel duration changes.

</td></tr><tr><td>

Update Capacity on task delete

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Update the capacity used whenever an open task is deleted within the given window.

</td></tr><tr><td>

Validate Capacity Value

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Validates the value of the provided capacity for the capacity definition. Capacity should be a non-zero positive integer value.

</td></tr><tr><td>

Validate Effective to and Effective from

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td><td>

Validates the dates entered in the **Effective to** and **Effective from** fields in the capacity assignment table. The system calculates the **Effective to** date based on the value entered in the **Repeat for** field if the **Capacity by** value is not selected as for the agent schedule. The **Effective from** value should always be on or after the current date, and before or equal to the **Effective to** date. While updating the capacity assignment, the**Effective to** value cannot be set to a date before capacity usage exists.

</td></tr><tr><td>

Validate Percent Allocated value

</td><td>

Capacity Reservation Rule \[wm\_capacity\_reservation\_rule\]

</td><td>

Validates the allocated percentage value in the Capacity Reservation Rule table. This value should be a non-zero positive integer less than or equal to 100.

</td></tr><tr><td>

Update Domain for capacity assignment

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td><td>

The system assigns domains to records based on information in the **Type** field. If the Type is 'Territory internal agents' or 'Territory contractor group', the domain is set using the **Territory** field. For any other type, the domain is determined by the **Group** field.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Assignment Override \[wm\_capacity\_override\]

</td><td>

Updates the **Capacity Demand Metrics** table when the aggregated agent schedule cutoff date or days is updated for a territory.

</td></tr><tr><td>

Update Capacity on task change

</td><td>

WorkOrder Task \[wm\_task\]

</td><td>

Enables you to customize the calculation of capacity by defining conditions for deducting capacity from the capacity usage.

</td></tr><tr><td>

Disallow capacity definition changes

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Prevents modifications to capacity definitions when they're in use.

</td></tr><tr><td>

Disallow override for agent-schedule

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Prevents overrides for schedules managed by agent scheduling system.

</td></tr><tr><td>

Disllow update on capacity usage

</td><td>

Capacity Buckets\[wm\_capacity\_bucket\]

</td><td>

Prevents updating capacity and time values when capacity usage records exists.

</td></tr><tr><td>

Limit one Demand channel per reservation

</td><td>

Capacity Reservation Rule\[wm\_capacity\_reservation\_rule\]

</td><td>

Ensures that each capacity reservation rule is associated with only one demand channel.

</td></tr><tr><td>

Prevent Duplicate Name, Condition

</td><td>

Demand Channel\[wm\_demand\_channel\]

</td><td>

Ensures that demand channels don't have duplicate names and conditions.

</td></tr><tr><td>

Prevent updating record to inactive

</td><td>

Demand Channel\[wm\_demand\_channel\]

</td><td>

Prevents changing the status of the demand channel to **Inactive** when the demand channel is still in use.

</td></tr><tr><td>

Remove capacity for unsupported task

</td><td>

WorkOrder Task\[wm\_task\]

</td><td>

Removes capacity allocations from tasks that don't support capacity management.

</td></tr><tr><td>

Restrict changes to definition

</td><td>

Capacity Definition\[wm\_capacity\_definition\]

</td><td>

Prevents changing **Capacity by** value of capacity definition to Agent Schedule when there are capacity assignment override records.

</td></tr><tr><td>

To verify usage not less than 0

</td><td>

Capacity Usage\[wm\_capacity\_usage\]

</td><td>

Validates that capacity usage values are greater than or equal to 0.

</td></tr><tr><td>

Validate different types of overrides

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Validates that different types of overrides comply with business constraints.

</td></tr><tr><td>

Validate fields

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Ensures that the required fields are populated for capacity override.

</td></tr><tr><td>

Validate fields based on type

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td><td>

Ensures that the required fields are populated based on the type of capacity assignment.

</td></tr><tr><td>

Validate on deleting definition

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Ensures that the capacity definitions are not in use before their deletion.

</td></tr><tr><td>

Validate overall definition

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Validates the capacity definition before adding or updating it.

</td></tr><tr><td>

Validate overlapping capacity buckets

</td><td>

Capacity Buckets\[wm\_capacity\_bucket\]

</td><td>

Prevents defining overlapping time ranges in capacity buckets.

</td></tr><tr><td>

Validate percent allocated

</td><td>

Allocation Schedule \[wm\_allocation\_schedule\]

</td><td>

Validates the allocated percentage value. The value should be a positive integer less than or equal to 100.

</td></tr><tr><td>

Validate percent allocated

</td><td>

Allocation Schedule Details \[wm\_allocation\_schedule\_detail\]

</td><td>

Validates the allocated percentage value. The value should be a positive integer less than or equal to 100.

</td></tr><tr><td>

Validate range

</td><td>

Allocation Schedule Details \[wm\_allocation\_schedule\_detail\]

</td><td>

Validates that the time ranges don't overlap.

</td></tr><tr><td>

Validate recurrence

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Validates that the recurrence rules in capacity override are configured correctly.

</td></tr><tr><td>

Validate total percentage

</td><td>

Capacity Buckets\[wm\_capacity\_bucket\]

</td><td>

Ensures that the total allocated percentage across all the capacity buckets doesn’t exceed 100.

</td></tr><tr><td>

Validation for rank

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Validates the ranking order for capacity reservations to ensure proper priority.

</td></tr></tbody>
</table>Capacity management adds the following business rules for Shift Scheduling for Field Service. The com.snc.sn\_fsm\_shift\_schdlng plugin must be installed to enable these business rules.

<table id="table_hcq_r2g_bgc"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update Capacity For Demand

</td><td>

Agent Schedule \[sn\_shift\_planning\_agent\_schedule\]

</td><td>

Updates capacity when demand metrics is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Agent Schedule Time Off Request \[sn\_shift\_planning\_agent\_schedule\_request\]

</td><td>

Updates demand metrics table for territory planning.

</td></tr></tbody>
</table>Capacity management adds the following business rules for Field Service Territory Planning. You must install the com.snc.fsm\_territory\_planning plugin to enable these business rules.

<table id="table_kmx_rtj_bgc"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td rowspan="15">

Updates the Capacity Demand Metrics \(wm\_capacity\_for\_demand\) table on updating the values for **Aggregated agent schedule cut off** or **Aggregated agent schedule cutoff date** fields for a Field Service Territory.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Schedule Entry cmn\_schedule\_span

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Territory\[sn\_tp\_territory\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Buckets\[wm\_capacity\_bucket\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Agent Work Schedule \[agent\_work\_schedule\]

</td></tr><tr><td>

Update Demand channel on WOT

</td><td>

WorkOrder Task\[wm\_task\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Agent Personal Schedule \[agent\_events\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Reservation Rule \[wm\_capacity\_reservation\_rule\]

</td></tr><tr><td>

Update demand metrics table for 1 day

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Allocation Schedule \[wm\_allocation\_schedule\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Schedule \[cmn\_schedule\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Allocation Schedule Details \[wm\_allocation\_schedule\_detail\]

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Territory Group \[sn\_tp\_territory\_group\]

</td></tr><tr><td>

Validate Aggregated agent schedule cutof

</td><td>

Territory\[sn\_tp\_territory\]

</td><td>

Validates the value Aggregated agent schedule cutoff days or date field in the Territory table. The agent schedule cut off days must be a non-zero integer value greater than or equal to 0 and less than or equal to 30.

</td></tr></tbody>
</table>**Note:** You must select **using dynamic scheduling** in the **Assignment method for tasks** configuration option to enable your application to distribute work based on the capacity management rules.

## Scheduled job

The Capacity and Reservations Management adds the following scheduled job. To find them, navigate to **All** &gt; **sn\_schedulejobs.do**.

|Scheduled job|Description|
|-------------|-----------|
|Compute Capacity Demand Metrics Data|Calculates and generates data for the Field Service Territory Capacity Analytics dashboard.|

## Script includes

The Capacity and Reservations Management adds the following Script includes. To find them, navigate to **All** &gt; **Script Includes**.

<table id="table_dzh_mml_stb"><thead><tr><th>

Script include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

FSMCapacityAjax

</td><td>

Provides AJAX endpoints that allows client scripts to check agent capacity for tasks and retrieve assignment details dynamically from the server.

</td></tr><tr><td>

FSMCapacityAppnmtBookingUtil

</td><td>

Utility methods to support appointment booking in FSM. This utility method retrieves dispatch groups for a location and filters groups based on the configuration. It also determines the eligible groups for task assignment during appointment scheduling.

</td></tr><tr><td>

FSMCapacityBaseUtil

</td><td>

Customizable utility class that extends FSMCapacityBaseUtilSNC. This utility class provides methods to validate and calculate capacity.

</td></tr><tr><td>

FSMCapacityBaseUtilSNC

</td><td>

Provides read-only utility scripts to validate and calculate capacity.

</td></tr><tr><td>

FSMCapacityBucketApi

</td><td>

Manages capacity buckets, including CRUD operations and bucket allocation.

</td></tr><tr><td>

FSMCapacityBucketApiSNC

</td><td>

Contains utility methods to retrieve and map capacity buckets used by a task, based on assignment and schedule details. It supports advanced bucket-based capacity calculations and integrates with usage, reservation, and definition APIs.

</td></tr><tr><td>

FSMCapacityConstants

</td><td>

Holds customizable constants. It extends the base constants class \(FSMCapacityConstantsSNC\) and allows you to override or add new constant values specific to the requirements, without modifying the base constants.

</td></tr><tr><td>

FSMCapacityConstantsSNC

</td><td>

Holds read-only constants like table names, default values, and configuration options. It centralizes important static values used throughout the workflow.

</td></tr><tr><td>

FSMCapacityCoreApi

</td><td>

Provides methods to retrieve and calculate capacity details for tasks, supporting advanced capacity planning and usage tracking.

</td></tr><tr><td>

FSMCapacityDefinitionApi

</td><td>

Provides API class for capacity definitions. It extends the base API \(FSMCapacityDefinitionApiSNC\) and allows you to manage and override capacity definition as per the business requirement.

</td></tr><tr><td>

FSMCapacityDefinitionApiSNC

</td><td>

Provides API methods to calculate total capacity, handle overrides, and support different capacity calculation strategies based on assignment, agent schedule, or hours.

</td></tr><tr><td>

FSMCapacityManagement

</td><td>

Integrates with various Capacity and Reservation Management APIs to orchestrate capacity checks, calculations, and updates. It provides methods to manage capacity by determining the capacity for tasks and agent availability.

</td></tr><tr><td>

FSMCapacityQueryUtil

</td><td>

Utility class that provides query to find agent schedule assignments within a time window and retrieve all relevant assignments based on qualifiers and date ranges.

</td></tr><tr><td>

FSMCapacityReservationAllocationApi

</td><td>

Provides customizable utility class to manage capacity, reservations, and allocations. It extends FSMCapacityReservationAllocationApiSNC.

</td></tr><tr><td>

FSMCapacityReservationAllocationApiSNC

</td><td>

Read-only utility class that handles capacity, reservations, and allocations. It provides methods to calculate allocation percentages and reservation capacities, supporting advanced scheduling and capacity planning.

</td></tr><tr><td>

FSMCapacityUsageApi

</td><td>

Customizable API class that manages capacity usage records. It extends FSMCapacityUsageApiSNC and provides customizable methods to handle capacity usage calculations.

</td></tr><tr><td>

FSMCapacityUsageApiSNC

</td><td>

Provides methods to calculate and retrieve total and reserved capacity usage. It leverages caching and integrates with Capacity definition and reservation APIs to validate and track usage efficiently.

</td></tr><tr><td>

FSMCapacityUtil

</td><td>

Provides utility functions to ensure integrity checks and safe deletion Capacity and Reservation Management entities. It checks if the capacity definitions, reservations, or reservation rules are referenced in usage records.

</td></tr><tr><td>

ScheduleOptimizationCapacityResponse

</td><td>

Contains a utility class that provides methods to calculate the capacity horizons for groups or territories, to determine the available and allocated capacity for task optimization within a specified date range.**Note:** The Schedule Optimization plugin \(com.snc\_schedule\_optimization\) for Field Service Management must be installed to enable this script include.

</td></tr></tbody>
</table>The Capacity and Reservations Management adds the following Script includes for Field Service Territory Planning. You must activate the Field Service Territory Planning plugin \(com.snc.fsm\_territory\_planning\) for Field Service Management to enable these script includes.

|Script include|Description|
|--------------|-----------|
|FSMDemandManagementConstants|Extends the constants class FSMDemandManagementConstantsSNC. It allows you to override or add new constant values specific to your requirements without modifying the base read-only constants.|
|FSMDemandManagementConstantsSNC|Defines read-only constants such as queue names, metric calculation keys, and configuration values. It centralizes important string and numeric constants for reuse across the application.|
|FSMDemandManagementUtilSNC|Provides read-only core utility functions, including methods to calculate and update metrics data for territories and capacity assignments.|
|FSMDemandManagementUtil|Customizable class that extends FSMDemandManagementUtilSNC. It allows you to override or add demand management utility methods specific to your requirements.|
|FSMDemandManagementExtPoint|Provides method to retrieve the default demand channel. Implements the FSMDemandManagementExtPoint extension point, allowing you to customize demand management.|
|FSMDemandManagementQueryUtil|Customizable class that extends the read-only FSMDemandManagementQueryUtilSNC class. You can override or add new methods in FSMDemandManagementQueryUtil to customize demand management for your requirements.|
|FSMDemandManagementQueryUtilSNC|Defines utility functions such to fetch the default demand channel, retrieve future work order tasks, and delete metric records. It provides reusable logic to support Demand Management features.|

## Roles

The Capacity and Reservations Management adds the following roles. To find them, navigate to **All** &gt; **Roles**.

|Roles|Description|
|-----|-----------|
|sn\_fsm\_capacity\_mg.wm\_capacity\_write|Allows CRUD access to all the capacity related tables|
|sn\_fsm\_capacity\_mg.wm\_capacity\_read|Allows read access to all the capacity related tables and Capacity console workspace|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

