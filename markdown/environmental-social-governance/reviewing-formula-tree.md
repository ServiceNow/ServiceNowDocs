---
title: Reviewing calculation details with formula trees
description: Calculated metric definitions provide a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using GRC: Metrics to provide data, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Reviewing calculation details with formula trees

Calculated metric definitions provide a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.

Formula trees enhance transparency in calculated metric values by displaying a detailed breakdown of the calculation for a selected calculated metric data record. They display the values of the operands and how they’re combined to produce the final result. You can view the details of complex calculations and verify their accuracy, and provide that information to auditors.

**Note:** The **Calculation level** field determines whether formula trees are available for different data. For generated Calculated metric data, the field is set to Metric Definition, and for generated metrics, the field is set to Entity. For more information on formula building, see [Formula building in a calculated metric definition](formula-building-at-metric-definition-and-entity-level.md).

To access the formula tree for a calculated metric data record, open the record and select **Show formula tree**.

![Sample formula tree.](../image/metric-formula-tree-view.png "Example of a formula tree")

A formula tree displays the values of operands by applying the level of precision provided in the CMD. For example, if the CMD specifies a precision of two decimal places, the formula tree displays all operand values with two decimal places even if the actual values have more or fewer decimal places.

If an empty page is displayed, the formula tree or formula operands are currently empty and being updated asynchronously.

If an error page is displayed, errors in the formula operands must be corrected.

**Note:** If a value is missing for any operand in a CMD formula, you can define a default value for that operand in the Calculated Metric Definition Settings \[sn\_grc\_metric\_definition\_setting\] table. The system will automatically retrieve and apply the specified default value so the formula executes without interruption. You can customize these default values or add new records as needed. For more information, see [Set default values for CMD formula operands](activate-default-values-for-cmd-calculations.md).

To learn more about formula trees, see [View the calculation breakdown in a formula tree](../task/view-formula-tree.md).

-   **[View the calculation breakdown in a formula tree](../task/view-formula-tree.md)**  
View a structured and visual representation of the entire calculation chain in Operational Sustainability Workspace, including all operands and operations. This view is helpful for auditing data and debugging.

**Parent Topic:**[Using GRC: Metrics to provide data](using-grc-metrics.md)

