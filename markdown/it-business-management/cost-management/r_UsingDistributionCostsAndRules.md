---
title: Using distribution costs and rules
description: Distribution Costs are costs which can be divided among a group of records.
locale: en-US
release: xanadu
product: Cost Management
classification: cost-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cost Management, Strategic Portfolio Management]
---

# Using distribution costs and rules

Distribution Costs are costs which can be divided among a group of records.

For example, the cost of power at a datacenter which can be divided among the CIs in the datacenter.

Distribution Rules determine how the Distribution Costs are divided among the CIs.

## Defining Distribution Costs

To define new distribution costs, navigate to **Financial Management** &gt; **Cost Management** &gt; **Distribution Costs**, and select **New**. Populate the following fields:

|Field|Input Value|
|-----|-----------|
|Number|A system-generated unique identifier for the Distribution Cost.|
|Name|A human-readable identifier for the cost.|
|Amount|The amount of the cost, with a currency list. To add a new currency, use the **Edit** link.|
|Distribution Rule|Select a Distribution Rule to determine how the costs are distributed to CIs. For more information, see Distribution Rules.|
|Active|Determines if the cost is actively used.|
|Start Date|The date of the cost, or if the cost is recurring, the first date of the cost.|
|Recurring|If checked, the cost will recur, and will be added regularly.|
|End Date|If Recurring is true, the last date to add the distribution cost.|
|Summary Type|Identifies a high-level type of expense for easier summary reports. This value will be used to set the expense line summary type field.|
|Interval|If Recurring is true, the time between each addition of the distribution cost between Start Date and End Date.|
|Last Processed|A read-only display of the last time the distribution cost was processed.|
|Next Process|A read-only display of the scheduled next process date.|

-   **[Defining distribution rules](r_DefiningDistributionRules.md)**  
Define distribution rules to view distribution costs that are distributed according to the rules.

**Parent Topic:**[Cost Management](r_CostManagement.md)

