---
title: Formula building in a calculated metric definition
description: In a calculated metric definition, you can create formulas to perform calculations for any data that you may require.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Formula building in a calculated metric definition

In a calculated metric definition, you can create formulas to perform calculations for any data that you may require.

A formula consists of operands, operators, and functions. For example, if you want to calculate the total employee count from two metric definitions namely number of male employees and number of female employees, then the selected metric definitions are the operands and the operator is the symbol or function that performs a specific operation on the operands to obtain a result. Examples of operators include addition \(+\), subtraction \(-\), multiplication \(\*\), and division \(/\).

You can set default values for operands in the Calculated Metric Definition Settings table to ensure metric calculations continue smoothly even when data is missing or undefined. When a formula encounters an empty operand, the system automatically applies the configured default value from this table, allowing the calculation to proceed without interruption. Users can activate the shipped default record or create custom entries with preferred values for specific operands. This setup enhances the reliability and flexibility of metric logic, reduces manual intervention, and supports consistent results across varying data conditions.

When you build a formula in a calculated metric definition, you can choose to build it at either the metric definition level or at the entity level. Before you save the calculated metric definition form and build the formula for metric definition score calculation, you must specify the calculation level in the calculated metric definition form. The two levels are as follows:

-   **Metric definition**: If you select **Metric definition** in the **Calculation level** field, then the data across all child metric definitions or child metrics is used for calculation. When you select **Execute**, the formula is applied and the calculated metric definition data is generated. For more information, see [Configure the formula builder](../task/configure-formula-builder.md). The following image shows how calculation occurs at the metric definition level: ![Calculation at the metric definition level.](../image/formula-building-md-level.png)
-   **Entity**: If you select **Entity** in the **Calculation level** field and specify the calculation method using the formula builder, then the child metrics are created for the calculated metric definition. These metrics are created for each distinct entity that is associated with the metric definitions that have been used as operands in the formula. When you Execute the metric definition, the formula is applied and the metric data is generated. When you Aggregate the metric definition, the metric data is aggregated and the calculated metric data is generated. The following image shows how calculation occurs at the entity level:![Calculation at the entity level.](../image/aggregation-entity-level.png)

**Important:**

Ad hoc metric data from child metrics is not included in CMD formula calculations at either level. Only data from scheduled child metric tasks feeds into the CMD score. For more information, see [Ad hoc metric data task limitations](../reference/ad-hoc-metric-data-task-limitations.md).

-   **[General guidelines for formula building](../../esg-management-reporting/concept/Formula-building-general-guidelines.md)**  
While building a custom formula in a calculated metric definition, keep these general guidelines in mind to easily create your formulas.
-   **[Configure the formula builder](../task/configure-formula-builder.md)**  
Specify the formula context, the tables, and the identifiers before you can build a formula.
-   **[Import a formula into a calculated metric definition](../task/import-a-formula-into-a-cmd.md)**  
Directly import any formula that is stored in Microsoft Excel spreadsheets into a calculated metric definition. This import helps in quickly building your formula for performing calculations.
-   **[Create a formula](../task/create-a-formula.md)**  
Build your own formula using either entities or metric definitions.

**Parent Topic:**[Configuring GRC: Metrics](configuring-grc-metrics.md)

