---
title: Metric weight maps
description: Weight maps are generated for each metric for every fiscal unit set in com.glide.fiscal\_calendar.fiscal\_unit property.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Allocations, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Metric weight maps

Weight maps are generated for each metric for every fiscal unit set in com.glide.fiscal\_calendar.fiscal\_unit property.

Weight map is JSON that holds the weighted breakups to allocate accounts for a metric. Allocation or rollup based on weighted metrics works only if correct weight map is generated for a given fiscal period.

The **Preview Weight Map** \(also available from the application navigator\) in the Weighted Metric Builder form shows how the weight is split across the accounts for a given fiscal period. The Weight Map Preview list view shows the total number of weights and the date and time the weight map was last generated. You can also view the percentage split for each account breakdown and generate or regenerate the weight map in the Preview Weight Maps user interface if the current weight map is not correct or has not generated.

Pre-generated weight maps for the fiscal period also helps in the performance of allocation workbench to avoid generating weight maps spontaneously while allocation page is still in the process of loading.

Following is an example to understand weight maps and percentage allocation if metric is used:

![Weight maps and percentage allocation example](../image/MetricWeightMapReview.png "Weight maps and percentage allocation example")

**Parent Topic:**[Allocations](c_Allocations.md)

**Related topics**  


[Account buckets](c_AccountBuckets.md)

[Grooming and cleansing conditions](c_GroomingConditions.md)

[Expense allocation](c_ExpenseAllocation.md)

[Financial Management example allocations](../reference/r_ITFinanceExampleAllocations.md)

[Use cost analysis to view the allocation of amount](../task/financial-management-cost-analysis.md)

