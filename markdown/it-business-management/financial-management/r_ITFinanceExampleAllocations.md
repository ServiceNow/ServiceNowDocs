---
title: Financial Management example allocations
description: The demo data that is available with the Financial Management application provides examples of cost allocations that you can use to model allocation rules, methods, and metrics.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Allocations, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management example allocations

The demo data that is available with the Financial Management application provides examples of cost allocations that you can use to model allocation rules, methods, and metrics.

## Allocate by number of servers

This weighted allocation metric allocates to servers based on the server cost.

-   **Metric name**: Servers by Server cost
-   **Type**: weighted

Notice the following field values:

-   **Weight table** is the Server table in the CMDB.
-   **Reference to allocate to** is the field on the weight table that you are allocating to. In this case, you are allocating to individual servers that are identified by their sys\_id.
-   **Aggregate** takes the value of the **Aggregate count** field in the weight table, which in this case is **Cost**.
-   **Aggregate count** is the cost of each server, which is identified on the server record.

![A metric that weights allocations by server cost](../image/Server_number_example.png "A metric that weights allocations by server cost")

**Parent Topic:**[Allocations](../concept/c_Allocations.md)

**Related topics**  


[Account buckets](../concept/c_AccountBuckets.md)

[Grooming and cleansing conditions](../concept/c_GroomingConditions.md)

[Expense allocation](../concept/c_ExpenseAllocation.md)

[Metric weight maps](../concept/metric-weight-maps.md)

[Use cost analysis to view the allocation of amount](../task/financial-management-cost-analysis.md)

