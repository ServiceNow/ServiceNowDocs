---
title: Grooming and cleansing conditions - Legacy
description: Grooming conditions define how expenses are related to each other and to buckets when you make changes in the workbench, while cleansing conditions define how financial data is cleansed by segment.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Allocations - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Grooming and cleansing conditions - Legacy

Grooming conditions define how expenses are related to each other and to buckets when you make changes in the workbench, while cleansing conditions define how financial data is cleansed by segment.

## Grooming conditions

The workbench creates three types of grooming conditions:

-   Data cleansing conditions: Defines the expense combinations that you make during the Cleansing stage. For example, if you drag the expense entry for the Acme vendor onto the Acme Inc. vendor, the application creates a grooming rule that specifies to the workbench that all those expenses should be considered as belonging to the Acme Inc. vendor. The application does not actually add, delete, or modify the expense records in the General Ledger Cleansed Data table \[itfm\_gl\_data\_cleansed\].
-   Bucketing conditions: Defines which expenses you added to buckets during the Bucketing stage.
-   Advanced query conditions: Defines which expenses are allowed to be added to buckets during the Bucketing stage. The application creates data cleansing and bucketing conditions automatically when you use the workbench. The only type of grooming condition that you create manually, either through the form view or through the workbench, is the advanced query condition.

## Cleansing conditions

The application creates cleansing conditions when you merge expenses in the [cleansing stage of the workbench](c_TheDataCleansingStage.md). You do not need to modify these cleansing conditions.

-   **[Modify advanced query conditions](../task/t_ModifyAdvancedQueryConditions.md)**  
You can modify existing advanced query conditions, which define how expenses are added to buckets.

**Parent Topic:**[Allocations - Legacy](c_Allocations.md)

**Related topics**  


[Account buckets - Legacy](c_AccountBuckets.md)

[Expense allocation - Legacy](c_ExpenseAllocation.md)

[Financial Management example allocations - Legacy](../reference/r_ITFinanceExampleAllocations.md)

[Metric weight maps - Legacy](metric-weight-maps.md)

[Use cost analysis to view the allocation of amount - Legacy](../task/financial-management-cost-analysis.md)

