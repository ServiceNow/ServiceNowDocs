---
title: Generating controlled cost lines
description: Generating controlled cost lines helps you to control the allocation lines that are required for your business needs.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a cost model from Cost Model form, Cost models, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Generating controlled cost lines

Generating controlled cost lines helps you to control the allocation lines that are required for your business needs.

If you're a new customer, by default, the allocation engine automatically generates the controlled cost lines.

If you're upgrading from a previous version to the Xanadu release, the following changes are made to the Controlled Cost Lines and GL Expense Lines options:

-   When you clone a cost model, the **Generate Controlled Cost Lines** option is enabled in the new model and the **Generate GL Expense Lines** option is inactivated in the new model irrespective of whether the options were inactivated or enabled in the base model. These options aren't editable and don't appear on the default view of the Cost Model View page.
-   When you create a cost model, the default values are set. The default value for the **Generate Controlled Cost Lines** option is **true** and the default value for the **Generate GL Expense Lines** option is **false**. These options aren't editable and don't appear on the default view of the Cost Model View page.
-   For existing cost models, the existing values remain the same. If the **Generate Controlled Cost Lines** option is inactivated, it remains inactive. If the **Generate GL Expense Lines** option is enabled, it remains enabled. You can change the values for these options to default values.

To view the sub-bucket information and view reports on the relationship between the two segments, do the following:

-   If you require the sub-bucket information of the generated lines, select the **Include sub-Bucket Info** option on the Cost Model View page.

    The generated controlled cost lines are sufficient to plot single-dimension charts with the buckets.

-   [Define a breakdown relationship](../task/t_CreateBreakdownRelationship.md) explicitly to view reports on the relationship between the two segments.

    The engine then generates the additional breakdown allocation lines in the Cost Allocation Breakdown Aggregate \[itfm\_allocation\_breakdown\] table, which help to plot a two-dimension chart between segments. For example, IT Shared Service contribution to Business Unit.


**Parent Topic:**[Create a cost model from Cost Model form](../task/t_CreateACostModel.md)

