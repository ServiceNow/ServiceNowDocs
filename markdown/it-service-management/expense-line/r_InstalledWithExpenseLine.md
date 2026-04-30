---
title: Components installed with Expense Line
description: Several types of components are installed with the Expense Line plugin.Tables are added with activation of Expense Line.Roles are added with activation of Expense Line.Script includes are added with activation of Expense Line.Client scripts are added with activation of Expense Line.Business rules are added with activation of Expense Line.Domain separation is unsupported in Expense Line processing. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Expense Line
classification: expense-line
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Expense Line, IT Service Management]
---

# Components installed with Expense Line

Several types of components are installed with the Expense Line plugin.

**Parent Topic:**[Expense Line](../../asset-and-configuration/concept/c_ExpenseLine.md)

**Related topics**  


[View an expense](../../asset-and-configuration/task/t_ExpenseLinesExample.md)

[Expense lines and expense allocations](../concept/c_ExpenseLinesAndAllocations.md)

[Domain separation and Expense Line](../concept/domain-separation-expense-line.md)

## Tables installed with Expense Line

Tables are added with activation of Expense Line.

<table id="table_d4l_3zy_nr"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expense Line \[fm\_expense\_line\]

</td><td>

Stores information about expense lines, including a link to the associated rate card. Contains the status and next scheduled processing date for the expense line.

</td></tr></tbody>
</table>## Roles installed with Expense Line

Roles are added with activation of Expense Line.

|Role|Contains roles|Description|
|----|--------------|-----------|
|Financial admin \[financial\_mgmt\_admin\]|\[financial\_mgmt\_user\]|Can create, write, and delete allocation units, fixed assets, depreciation, rate cards, distribution costs, expense lines, and expense allocations.|
|Financial user \[financial\_mgmt\_user\]|none|Can read allocation units and expense allocations. Can create, read, and write rate cards and expense lines. Can create, read, write, and delete fixed assets, depreciation, distribution costs.|

## Script includes installed with Expense Line

Script includes are added with activation of Expense Line.

|Script include|Description|
|--------------|-----------|
|ExpenseLine|Helps create expense line records.|
|ExpenseManagementUtils|Provides utilities for financial management modules.|
|ExpenseManagementUtilsAJAX|Provides AJAX utilities for expense lines.|

## Client scripts installed with Expense Line

Client scripts are added with activation of Expense Line.

|Client script|Table|Description|
|-------------|-----|-----------|
|Populate sources if inherited|\[fm\_expense\_line\]|Copies the source fields of the parent expense line to the current line on the Expense Line record if an expense line is inherited.|
|Populate source fields from asset|\[fm\_expense\_line\]|If the source asset changes, updates related source fields on the Expense Line record . For example, if the asset source field changes, the configuration item source field is updated, as well.|
|Populate source fields from ci|\[fm\_expense\_line\]|Updates related source fields if the source configuration item changes on the Expense Line record.|
|Populate source fields from contract|\[fm\_expense\_line\]|Updates related source fields if the source contract changes on the Expense Line record.|
|Populate source fields from task|\[fm\_expense\_line\]|Updates related source fields if the source task changes on the Expense Line record.|

## Business rules installed with Expense Line

Business rules are added with activation of Expense Line.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Create Expense Line|\[alm\_asset\]|Automatically creates an expense line for a new asset based on asset cost unless the asset is a merged software license.|
|Set source allocation fields|\[fm\_expense\_line\]|Sets the related source fields when the source ID changes. For example, when an asset becomes the source ID, the asset source field and configuration item source field are automatically populated.|
|Update Costs|\[alm\_consumable\]|Updates the cost of a consumable when quantity is reduced.|

## Domain separation and Expense Line

Domain separation is unsupported in Expense Line processing. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

### Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

