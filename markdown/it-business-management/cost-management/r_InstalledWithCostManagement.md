---
title: Components installed with Cost Management
description: Several components are installed with the Cost Management application.
locale: en-US
release: zurich
product: Cost Management
classification: cost-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Activate Cost Management, Cost Management, Strategic Portfolio Management]
---

# Components installed with Cost Management

Several components are installed with the Cost Management application.

Demo data is available with Cost Management. The demo data provides sample budgets, distribution costs, expense allocations, contract rate cards, and rate card costs.

## Tables

Cost Management adds the following tables.

|Table|Description|
|-----|-----------|
|Allocation Unit `[allocation_unit]`|Tracks capacity and usage for a business service. Stores reference to business service, total, allocated, and remaining units of capacity.|
|Budget `[fm_budget]`|Tracks planned and total expense allocation amounts for a collection of cost centers.|
|Budget Cost Center `[fm_budget_cost_center]`|Associates one or more cost centers to a budget.|
|CI Cost Center Relationship `[fm_cmdb_rel_cc]`|Associates a cost center to a business service that it consumes and the number of units it uses. This is used to calculate the number of allocated units to update the allocation unit record.|
|CI Rate Card `[fm_ci_rate_card]`|Links configuration items and costs. A classification can also be defined to allow for multiple rate cards for a group of CIs.|
|CI Rate Cards `[fm_ci_rate_card_cmdb_ci_m2m]`|Associates configuration items to a rate card.|
|Contract Rate Card `[fm_contract_rate_card]`|Provides detailed price information for a contract and enables you to generate recurring expenses automatically.|
|Distribution Cost `[fm_distribution_cost]`|Represents costs which can be divided among a group of records. For example, the cost of power at a datacenter which can be divided among the CIs in the datacenter.|
|Distribution Cost Rule `[fm_distribution_cost_rule]`|Determines how the costs are distributed to CIs.|
|Distribution Units `[fm_distribution_units]`|Stores the number of units to associate to configuration items linked to the current rate card.|
|Expense Allocation `[fm_expense_allocation]`|Associates the value of an expense to a target reference. The value is generated from an expense line by processing allocation rules. The target is the record that is responsible for that expense amount. Common targets are cost centers, departments, companies, groups, and users.|
|Expense Allocation Rule`[fm_expense_allocation_rule]`|Determines how to process an expense line into an expense allocation. The logic starts by defining a table and condition to run against. Expenses linked to the selected table will be evaluated by this rule. If the condition is met, an allocation of a defined percentage is created for the reference defined by the allocation field value. Advanced scripts can also be used to define custom allocation generation.|
|Financial Management Log `[fm_log]`|Logs financial management information for tracking and to asset with debugging. Extends the system log table.|
|Labor Rate Card `[fm_labor_rate_card]`|Defines hourly labor rates for expense line generation based on functional roles.|
|Rate Card `[fm_rate_card]`|Associates configuration items to a rate card.|
|Rate Card `[fm_recurring_rate_card]`|Represents a collection of recurring costs.|
|Rate Card Cost `[fm_ci_rate_card_cost]`|Associates a recurring CI cost to a rate card so that it is applied to all CIs associated with the rate card.|
|Rate Card Users `[clm_m2m_rate_card_user]`|Associates users to a rate card.|
|Relationship Path `[fm_relationship_path]`|Defines the relationship between configuration items, such as parent records and child records.|
|Task Rate Card `[fm_task_rate_card]`|Stores records that define task costs.|

## User Roles

Cost Management adds the following user roles. A user with the user\_admin or admin role can assign these roles.

<table id="table_z1c_qd5_jp"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Financial User \(financial\_mgmt\_user\)

</td><td>

Financial users participate in financial processes and have limited access to functionality.

 Can read allocation units and expense allocations. Can create, read, and write rate cards and expense lines. Can create, read, write, and delete fixed assets, depreciation, distribution costs.

</td><td>

None

</td></tr><tr><td>

Financial Admin \(financial\_mgmt\_admin\)

</td><td>

Financial administrators manage financial processes in the system.

 Can create, write, and delete allocation units, fixed assets, depreciation, rate cards, distribution costs, expense lines, and expense allocations.

</td><td>

financial\_mgmt\_user

</td></tr></tbody>
</table>## Properties

Cost Management adds the following properties.

|Name|Description|
|----|-----------|
|**com.snc.time\_card.default\_rate**|Sets a default hourly rate to use if no labor rate cards apply to the user.|
|**glide.cost\_mgmt.calc\_actual\_cost**|Sums all task expense lines and adds the total to the **Work cost** field on the task record when an expense line is created for any task with a **Type** of **Planned task**.|
|**glide.cost\_mgmt.debug**|Enables debugging of cost management processing. All logging events are recorded in the Financial Management Log `[fm_log]` table. This should only be enabled during initial testing or when troubleshooting because it can generate a large number of log records.|
|**glide.cost\_mgmt.process\_task\_cis**|Creates expense lines to affected configuration items when creating a task expense line. The default value is **false**.|
|**glide.cost\_mgmt.service\_allocation.method**|Defines if business service to cost center allocation costs should be calculated based on total units or allocated units.|

## UI Policies

Cost Management adds the following UI policies.

|Name|Table|Description|
|----|-----|-----------|
|Control flat rate vs bill rate fields|`[fm_task_rate_card]`|Hides the **Task rate** field and displays the **Default labor rate** field on the Task Rate Cards form if the **Use time worked** check box is selected.|
|Hide if define condition disabled|`[fm_ci_rate_card]`|Displays the **Table** and **Condition** fields on the CI Rate Cards form if the **Define condition** check box is selected.|
|Hide parent class if all enabled|`[fm_relationship_path]`|Hides the **Parent class** field on the Relationship Paths form if the **All parent classes** check box is selected.|
|Hide recurring fields for one time cost|`[fm_distribution_cost]`|Hides the **End date** and **Interval** fields on the Distribution Costs form if the **Recurring** check box is cleared.|
|Hide relationship type if all enabled|`[fm_relationship_path]`|Hides the **Relationship type** field on the Relationship Paths form if the **All relationships** check box is selected.|
|Hide Show Advanced Field|`[fm_distribution_cost_rule]`|Hides the **Table** and **Condition** fields on the Distribution Cost Rules form and displays the **Script** field if the **Advanced** check box is selected.|
|Hide table field|`[fm_labor_rate_card]`|Hides the **Table** field on the Labor Rate Cards form at all times.|
|Modify value field rules on distribution method|`[fm_contract_rate_card]`|Changes the **Value** field from read-only to mandatory on the Contract Rate Cards form if the **Distribute cost** field is set to **Allocate and distribute cost based on value**.|
|Show script field if advanced|`[fm_expense_allocation_rule]`|Displays the **Script** field on the Expense Allocation Rules form if the **Advanced** check box is selected.|

## Client Scripts

Cost Management adds the following client scripts.

|Name|Table|Description|
|----|-----|-----------|
|Calculate Tax Cost - Base cost|`[fm_rate_card]`|On the contract rate card record, calculates the tax cost and total cost based on changes to the base cost.|
|Calculate Tax Cost - Sales tax|`[fm_rate_card]`|On the contract rate card record, calculates the total cost if the Sales tax option is selected.|
|Calculate Tax Cost - Tax rate|`[fm_rate_card]`|On the contract rate card record, calculates the tax cost and total cost based on changes to the tax rate.|
|Set Rate Card End Date|`[fm_contract_rate_card]`|On the contract rate card record, sets the rate card end date to the contract end date if the contract has an end date.|

## Business rules

Cost Management adds the following business rules.

<table id="table_rs5_ng5_jp"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Calculate Totals with Tax

</td><td>

`[fm_recurring_rate_card]`

</td><td>

Updates the **Tax rate**, **Tax cost**, and **Total cost** fields when **Sales tax**, **Base cost**, or **Tax rate** field values change.

</td></tr><tr><td>

Process time card

</td><td>

`[time_card]`

</td><td>

Creates an expense line after a time card is approved.

</td></tr><tr><td>

fm\_calcBudgetValues

</td><td>

`[fm_budget]`

</td><td>

Updates remaining budget amount when planned or actual values change.

</td></tr><tr><td>

fm\_Disable rate card costs

</td><td>

`[fm_ci_rate_card]`

</td><td>

Disables all rate card costs when a rate card is disabled.

</td></tr><tr><td>

fm\_InsertBudget

</td><td>

`[fm_budget]`

</td><td>

Shows a message with the next budget number when a new record is inserted.

</td></tr><tr><td>

fm\_Populate Month Field

</td><td>

`[fm_expense_allocation]`

</td><td>

Fills in the **Month** field based on the **Expense date** field.

</td></tr><tr><td>

fm\_processExpenseAllocation

</td><td>

`[fm_expense_line]`

</td><td>

Processes expense allocation rules when an expense line is created for pending items.

</td></tr><tr><td>

fm\_Set default next process

</td><td>

`[fm_ci_rate_card_cost]`

</td><td>

Sets the default next process date for a new configuration item rate card cost.

</td></tr><tr><td>

fm\_Set default next process

</td><td>

`[fm_distribution_cost]`

</td><td>

Sets the default next process date for a new distribution cost.

</td></tr><tr><td>

fm\_updateAllocationAvailable

</td><td>

`[allocation_unit]`

</td><td>

Recalculates the number of available units when the number of allocated units is updated.

</td></tr><tr><td>

fm\_updateAllocationUnits

</td><td>

`[fm_cmdb_rel_cc]`

</td><td>

Recalculates the number of allocated units for a business service.

</td></tr><tr><td>

Next process date validation

</td><td>

`[fm_contract_rate_card]`

</td><td>

If the next process date for the contract rate card is after the start date, this business rule sets the next date to the start date.

</td></tr><tr><td>

Prevent more than one allocation per ci

</td><td>

`[allocation_unit]`

</td><td>

Prevents more than one allocation per configuration item.

</td></tr><tr><td>

Process CI Relationships

</td><td>

`[fm_expense_line]`

</td><td>

Processes parent related items and generates expense lines for configuration item source expenses. Processes task cost into affected configuration item expense lines for task source expenses.

</td></tr><tr><td>

Process Task Rate Cards

</td><td>

`[task]`

</td><td>

Processes task rate cards when a task is set to inactive.

</td></tr><tr><td>

Update Contract

</td><td>

`[fm_contract_rate_card]`

</td><td>

Rolls costs from rate card to contract. Updates the contract total cost, tax cost, tax rate, and base cost when total cost, tax cost or tax rate values change.

</td></tr><tr><td>

Update Planned Task Actual Cost

</td><td>

`[fm_expense_line]`

</td><td>

Calculates the total actual costs from related expense lines for planned task source expenses.

</td></tr><tr><td>

Verify rate card's start and end dates

</td><td>

`[fm_contract_rate_card]`

</td><td>

Validates that the rate card start date is specified and is not after the end date. This business rule also:-   Validates that the rate card start date is not before the contract start date and that the rate card end date is not after the contract end date.
-   Sets the rate card end date to the contract end date if a value is not entered and the contract has an end date.

</td></tr></tbody>
</table>**Parent Topic:**[Activate Cost Management](../task/t_ActivatingCostManagement.md)

