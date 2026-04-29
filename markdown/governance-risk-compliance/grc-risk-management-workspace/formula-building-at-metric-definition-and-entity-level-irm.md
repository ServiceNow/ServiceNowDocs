---
title: Formula building in a calculated metric definition
description: In a calculated metric definition, you can create formulas to perform calculations for any data that you may require.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Formula building in a calculated metric definition

In a calculated metric definition, you can create formulas to perform calculations for any data that you may require.

A formula consists of operands, operators, and functions. For example, to calculate total employee count from male and female employee metrics, the metrics act as operands, and the operator performs the calculation to produce the result. Examples of operators include addition \(+\), subtraction \(-\), multiplication \(\*\), and division \(/\).

When you build a formula in a calculated metric definition, you can choose to build it at either the metric definition level or at the entity level. Before you save the calculated metric definition form and create the score formula, you must specify the calculation level in the calculated metric definition form. The two levels are as follows:

-   **Metric definition**: If you select **Metric definition** in the **Calculation level** field, then the data across all child metric definitions or child metrics is used for calculation. When you select **Execute**, the formula is applied and the calculated metric definition data is generated. For more information, see [Configure the formula builder](../task/configure-formula-builder-irm.md). The following image shows how calculation occurs at the metric definition level: ![Calculation at the metric definition level.](../../metrics/image/formula-building-md-level.png)
-   **Entity**: If you select **Entity** in the **Calculation level** field and specify the calculation method using the formula builder, then the child metrics are created for the calculated metric definition. These metrics are created for each distinct entity that is associated with the metric definitions that have been used as operands in the formula. When you Execute the metric definition, the formula is applied and the metric data is generated. When you Aggregate the metric definition, the metric data is aggregated and the calculated metric data is generated. The following image shows how calculation occurs at the entity level:![Calculation at the entity level.](../../metrics/image/aggregation-entity-level.png)

-   **[Configure the formula builder](../task/configure-formula-builder-irm.md)**  
Specify the formula context, the tables, and the identifiers before you can build a formula.
-   **[Create a formula](../task/create-a-formula-irm.md)**  
Build your own formula using either entities or metric definitions.

**Parent Topic:**[Configuring metrics](configuring-irm-metrics.md)

