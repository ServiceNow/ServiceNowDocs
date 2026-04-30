---
title: Pipeline project creation rule for high-value sourcing requests
description: By default, the Pipeline project creation rule decision table is used to create pipeline projects automatically in Sourcing Pipeline Management.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sourcing Pipeline Management, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Pipeline project creation rule for high-value sourcing requests

By default, the Pipeline project creation rule decision table is used to create pipeline projects automatically in Sourcing Pipeline Management.

**Note:** You must have the `sn_spend_pipeline.pipeline_management_admin` role to update the Pipeline project creation rule decision table configuration.

The `sn_spend_pipeline.pipeline_management_admin` role contains the `decision_table_admin` role, which enables you to create, read, edit, and delete decision table inputs, columns, and values. For more information about configuring decision tables, see [Configuring decision tables](https://www.servicenow.com/docs/access?context=configuring-decision-builder&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

![Pipeline project creation rule.](../image/pipeline-decision-table.png)

When a shopper requests pricing for items over $250,000 through Shopping Hub or via Employee Center using the default "I need a product" record producer, specific decision inputs are triggered. If the shopper enters a budget greater than $250,000, the system automatically evaluates these decision inputs to apply the rule conditions:

-   Sourcing request \[sn\_shop\_sourcing\_activity\]
-   Purchase line \[sn\_shop\_purchase\_line\]

The Pipeline project creation rule is applied to the **Budget** field in the Sourcing Request \(SR\). This rule determines whether a pipeline project should be created for the SR based on the following conditions:

-   If the amount exceeds $250,000 USD, a pipeline project is created.
-   If the amount is $250,000 USD or less, a pipeline project isn’t created.

**Note:** The **Budget** field controls the creation of pipeline projects based on the entered amount. If the currency is different from the USD, it's converted to USD before the rule conditions are applied.

**Parent Topic:**[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

