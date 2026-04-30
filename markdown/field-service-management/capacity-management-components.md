---
title: Field Service Capacity and Reservations Management components
description: Several types of components are installed with the Field Service Capacity and Reservations Management feature, including tables, business rules, scheduled jobs, and script includes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
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
-   **Capacity Allocation Schedules**: Manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for same-day tasks.

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

Capacity Demand Metrics\[wm\_capacity\_demand\]

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

</td></tr><tr><td>

Allocation Schedule \[wm\_allocation\_schedule\]

</td><td>

Stores the default percentage of capacity allocation.

</td></tr><tr><td>

Allocation Schedule Details\[wm\_allocation\_schedule\_detail\]

</td><td>

Stores the relative start date, relative end date, and the percentage of capacity that should be allocated for an allocation schedule.

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

</td></tr><tr><td>

Validate percent allocated

</td><td>

Allocation Schedule\[wm\_allocation\_schedule\]

</td><td>

Validates the default allocation percentage value for an Allocation Schedule. The default allocation percentage should be a non-zero positive integer less than or equal to 100.

</td></tr><tr><td>

Validate range

</td><td>

Allocation Schedule Details\[wm\_allocation\_schedule\_detail\]

</td><td>

Validates the dates entered in the **Relative start** and **Relative end** fields in the **Allocation Schedule Details** table. The **Relative start date** should always be the current date or future date, and earlier than or equal to **Relative end** date.

The **Relative end** date should always be current date or a future date, later than or equal to **Relative start date**.

</td></tr><tr><td>

Validate percent allocated

</td><td>

Allocation Schedule Details\[wm\_allocation\_schedule\_detail\]

</td><td>

Validates the allocation percentage value for Allocation Schedule Details.

 The allocation percentage should be a non-zero positive integer less than or equal to 100.

</td></tr><tr><td>

Validate fields

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Validates the values provided for the fields of Capacity Assignment Override table.

</td></tr><tr><td>

Prevent updating record to inactive

</td><td>

Demand Channel\[wm\_demand\_channel\]

</td><td>

Validates if the Demand channel is used by any reservation rule. This rule prevents you from deleting or deactivating the demand channel if used in a reservation rule.

</td></tr><tr><td>

Update Demand channel on WOT

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Updates Demand Channel for a Work Order Task as per the conditions set for the Demand Channel.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Assignment Override\[wm\_capacity\_override\]

</td><td>

Updates Capacity Demand Metrics table when Capacity Assignment Override table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Updates Capacity Demand Metrics table when Capacity Assignment Override table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Schedule \[cmn\_schedule\]

</td><td>

Updates Capacity Demand Metrics table when Schedule table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Agent Work Schedule \[agent\_work\_schedule\]

</td><td>

Updates Capacity Demand Metrics table when Agent Work Schedule table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Agent Personal Schedule \[agent\_events\]

</td><td>

Updates Capacity Demand Metrics table when Agent Personal Schedule table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Schedule Entry \[cmn\_schedule\_span\]

</td><td>

Updates Capacity Demand Metrics table when Schedule Entry table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Territory Group \[sn\_tp\_territory\_group\]

</td><td>

Updates Capacity Demand Metrics table when Territory Group table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Territory Membership \[sn\_tp\_territory\_membership\_override\]

</td><td>

Updates Capacity Demand Metrics table when Territory Membership table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Allocation Schedule Details\[wm\_allocation\_schedule\_detail\]

</td><td>

Updates Capacity Demand Metrics table when Allocation Schedule Details table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Allocation Schedule \[wm\_allocation\_schedule\]

</td><td>

Updates Capacity Demand Metrics table when Allocation Schedule table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Buckets \[wm\_capacity\_bucket\]

</td><td>

Updates Capacity Demand Metrics table when Capacity Buckets table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Reservation Rule\[wm\_capacity\_reservation\_rule\]

</td><td>

Updates Capacity Demand Metrics table when Capacity Reservation Rule table is updated.

</td></tr><tr><td>

Update capacity demand metrics table

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td><td>

Updates Capacity Demand Metrics table when Capacity Assignment table is updated.

</td></tr><tr><td>

Update Capacity for appointment task

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Updates the Capacity Usage table when an appointment booking task is created or updated.

</td></tr><tr><td>

Prevent Duplicate Name, Condition

</td><td>

Demand Channel \[wm\_demand\_channel\]

</td><td>

Validates the name and condition specified in the Demand Channel table. Checks if there is already a Demand Channel with this name and if the condition specified is used by another Demand channel.

</td></tr><tr><td>

Validate fields based on type

</td><td>

Capacity Assignment \[wm\_capacity\_assignment\]

</td><td>

Validates the values provided for the fields of the Capacity Assignment table.-   **Territory** field cannot be blank.
-   Only Active Assignment Territories are supported.
-   When **Type** is Territory Contractor Group, a Vendor Group must be specified.
-   Agent Schedule capacity definition is not supported when the **Type** is Territory Contractor Group.
-   When **Type** is None, **Group** is not applicable.

If Territory Planning plugin is not installed, **Group**should be non-blank.

</td></tr><tr><td>

Disallow capacity definition changes

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Restricts you from updating the values of the fields **Capacity By** and **Frequency** if the Capacity Definition is in use or if there is an active Capacity Assignment Override defined for the Capacity Definition.

</td></tr><tr><td>

Disallow override for agent-schedule

</td><td>

Capacity Assignment Override \[wm\_capacity\_override\]

</td><td>

Prevents you from overriding the Capacity Definition if the Capacity Definition is based on Agent Schedule.

</td></tr><tr><td>

Remove capacity for unsupported task

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Removes capacity allocated for unsupported tasks.

</td></tr><tr><td>

Restrict changes to definition

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Restricts you from updating the **Capacity by** value to Agent Schedule if there an active Capacity Override Assignment for this Capacity Definition.

</td></tr><tr><td>

Validate overall definition

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Validates if the value of **Set capacity by buckets** field is applicable for the specified **Frequency**.

</td></tr><tr><td>

Validate on deleting definition

</td><td>

Capacity Definition \[wm\_capacity\_definition\]

</td><td>

Restricts you from deleting a Capacity Definition if it has active Capacity Assignments.

</td></tr><tr><td>

To verify usage not less than 0

</td><td>

Capacity Usage \[wm\_capacity\_usage\]

</td><td>

Validates the value of **Capacity used** field. The value should be greater than or equal to zero.

</td></tr><tr><td>

Validate total percentage

</td><td>

Capacity Buckets \[wm\_capacity\_bucket\]

</td><td>

Validates the total percentage of the workload capacities assigned to buckets. The total percentage should be between 1 and 100.

</td></tr><tr><td>

Disllow update on capacity usage

</td><td>

Capacity Buckets \[wm\_capacity\_bucket\]

</td><td>

Restricts you from updating the **% Capacity**, **Start**, and **End** fields for a Capacity Bucket that is in use.

</td></tr><tr><td>

Validate percent allocated

</td><td>

Allocation Schedule \[wm\_allocation\_schedule\]

</td><td>

Validates the allocation percentage value for an Allocation Schedule. The value should be a non-zero positive integer less than or equal to 100.

</td></tr><tr><td>

Validate overlapping capacity buckets

</td><td>

Capacity Buckets \[wm\_capacity\_bucket\]

</td><td>

Validates the **End** time provided. The **End** time should be greater than the **Start** time. This rule checks if the given time period overlaps with the time period of any other Capacity Bucket.

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

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

