---
title: Defining distribution rules
description: Define distribution rules to view distribution costs that are distributed according to the rules.
locale: en-US
release: xanadu
product: Cost Management
classification: cost-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using distribution costs and rules, Cost Management, Strategic Portfolio Management]
---

# Defining distribution rules

Define distribution rules to view distribution costs that are distributed according to the rules.

To define new distribution rules, navigate to **Financial Management** &gt; **Admin** &gt; **Distribution Cost Rules**, and select New and populate the following:

|Field|Input Value|
|-----|-----------|
|Name|A unique name for the rule.|
|Active|Determines if the rule is actively used.|
|Advanced|If checked, the distribution rule will be determined by script. If not checked, it will be determined by table and conditions.|
|Description|A description of the rules and any notes on its use.|
|Script|If Advanced is true, the script which will determine the rule's behavior.|
|Table|If Advanced is false, a list list of tables to find the records to distribute the cost to.|
|Condition|If Advanced is false, a condition builder to determine which records will receive the distributed cost, on the table determined by the Table field. Cost amount will be distributed evenly across the records identified by the table and condition values. This field uses the Condition Count Widget to preview what records would be returned by the conditions.|

Once submitted, the Distribution Costs related list is displated, which helps determine which costs will be distributed according to the rules.

## Scripted distribution

Scripted distributions allow for custom distribution amounts, versus the evenly split distributions when using table and condition filters.

To enable scripted processing on a distribution rule:

-   Check the advanced field check box, this will display the script field.
-   Build the script using the following concepts:
    -   Query for target records and data to use for calculating the allocation amount.
    -   Create expense line records using the ExpenseLine API.

        For more information, see [ExpenseLine](https://developer.servicenow.com/dev.do#!/reference/api/sandiego/server_legacy/c_ExpenseLineAPI).


As noted in the default script, when the advanced field is enabled, the following variables are available during the script processing:

-   *distCost* - GlideRecord for the distribution cost, allowing access to all fields.
-   *distCostAmount* - cost amount in the system currency.

## Processing Distribution Costs

A scheduled job called Process FM Costs automatically processes distribution costs daily.

**Parent Topic:**[Using distribution costs and rules](r_UsingDistributionCostsAndRules.md)

