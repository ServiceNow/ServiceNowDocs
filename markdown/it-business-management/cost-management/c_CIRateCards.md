---
title: CI rate cards
description: A configuration item \(CI\) rate card is a group of recurring configuration item costs associated with multiple configuration items. Rate cards make it easier to enter and track costs that are the same across multiple configuration items.
locale: en-US
release: yokohama
product: Cost Management
classification: cost-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cost Management, Strategic Portfolio Management]
---

# CI rate cards

A configuration item \(CI\) rate card is a group of recurring configuration item costs associated with multiple configuration items. Rate cards make it easier to enter and track costs that are the same across multiple configuration items.

Rate cards usually follow a framework in which all costs are recorded and allocated. For example, the contract costs of a specific model server in a New York datacenter could be different than the same server model running in a Madrid datacenter. Each model would have a separate rate card detailing the costs.

Users with the Financial Admin \(`financial_mgmt_admin`\) and Financial User \(`financial_mgmt_user`\) roles can manage CI rate cards.

-   **[Create a CI rate card](../task/t_CreateACIRateCard.md)**  
You can add a CI rate card that specifies an hourly rate and associate a rate code.
-   **[Add a condition to a CI rate card](../task/t_AddAConditionToACIRateCard.md)**  
If you are adding a condition to a CI rate card, use the **Update CI List** related link to create the relationship between the configuration item or items and the rate card.
-   **[CI rate card costs](c_CIRateCardCosts.md#)**  
CI rate card costs generate expense lines for configuration items on the associated rate card
-   **[Aggregate CI costs](c_AggregateCICosts.md)**  
Expense lines can be aggregated to apply all configuration item expenses to a parent business service or application with relationship paths.
-   **[Enable relationship aggregation](../task/t_EnableRelationshipAggregation.md)**  
The Process Last Month CI Costs scheduled job processes costs of configuration items. To start aggregating expenses to parents, identify the relationships to use for aggregation. Because there are many options for CMDB relationships, using all available paths for aggregation is generally not efficient.

**Parent Topic:**[Cost Management](../reference/r_CostManagement.md)

