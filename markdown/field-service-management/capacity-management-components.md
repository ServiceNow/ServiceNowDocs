---
title: Field Service Capacity and Reservations Management components
description: Several types of components are installed with the Field Service Capacity and Reservations Management feature, including tables, business rules, scheduled jobs, and script includes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
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

Capacity Definition\[wm\_capacity\_definition\]

</td><td>

Stores the capacity of a group or internal field service agent and the reservation rules to be used while assigning tasks.

</td></tr><tr><td>

Demand Channel\[wm\_demand\_channel\]

</td><td>

Stores daily capacity and demand data for each assignment, used for the capacity dashboard.

</td></tr><tr><td>

Capacity Demand Metrics\[wm\_capacity\_for\_demand\]

</td><td>

Stores the metrics data for all capacity assignments

</td></tr><tr><td>

Capacity Reservation\[wm\_capacity\_reservation\]

</td><td>

Stores the reservation definition and exclusion conditions.

</td></tr><tr><td>

Capacity Reservation Rule\[wm\_capacity\_reservation\_rule\]

</td><td>

Stores the reservation rules and the conditions for which the reservations should be used.

</td></tr><tr><td>

Capacity Assignment\[wm\_capacity\_assignment\]

</td><td>

Stores capacity definition assignments to groups within a specific time period to help avoid conflicts in capacity in a given time period by validating the **effective from** and **effective to** dates.

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

Add or update capacity whenever a task is assigned or unassigned. You can update capacity whenever the estimated work or travel duration changes.

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

</td></tr></tbody>
</table>**Note:** You must select **using dynamic scheduling** in the **Assignment method for tasks** configuration option to enable your application to distribute work based on the capacity management rules.

## Scheduled Jobs

The Capacity and Reservations Management adds the following scheduled jobs. To find them, navigate to **All** &gt; **sn\_schedulejobs.do**.

|Scheduled job|Description|
|-------------|-----------|
|Compute Capacity Demand Metrics Data|Calculates and generates data for the Field Service Territory Capacity Analytics dashboard.|

## Script Includes

The Capacity and Reservations Management adds the following scheduled jobs. To find them, navigate to **All** &gt; **Script Includes**.

|Script include|Description|
|--------------|-----------|
|FSMDemandManagementQueryUtil|Contains all queries for generating data for the Field Service Territory Capacity Analytics dashboard.|
|FSMDemandManagementUtil|Calculates and generates data for the `Compute Capacity Demand Metrics Data` scheduled job.|

## Roles

The Capacity and Reservations Management adds the following roles. To find them, navigate to **All** &gt; **Roles**.

|Script include|Description|
|--------------|-----------|
|sn\_fsm\_capacity\_mg.wm\_capacity\_write|Allows CRUD access to all the capacity related tables|
|sn\_fsm\_capacity\_mg.wm\_capacity\_read|Allows read access to all the capacity related tables and Capacity console workspace|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

