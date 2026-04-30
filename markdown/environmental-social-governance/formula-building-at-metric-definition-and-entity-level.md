---
title: Formula building in a calculated metric definition
description: When building a formula in a calculated metric definition, you can determine the granularity of results needed.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Formula building in a calculated metric definition

When building a formula in a calculated metric definition, you can determine the granularity of results needed.

A formula consists of operands, operators, and functions. For example, if you want to calculate the total employee count from two metric definitions, for example, the number of male employees and of female employees, the selected metric definitions are the operands and the operator is the symbol or function that performs a specific operation on the operands to obtain a result. Examples of operators include addition \(+\), subtraction \(-\), multiplication \(\*\), and division \(/\).

You can set default values for operands in the Calculated Metric Definition Settings \[sn\_grc\_metric\_definition\_setting\] table so metric calculations continue smoothly even when data is missing or undefined. When a formula encounters an empty operand, the system automatically applies the configured default value from this table. You can activate the shipped default record or create custom entries with preferred values for specific operands. This setup enhances the reliability and flexibility of metric logic, reduces manual intervention, and supports consistent results across varying data conditions.

The calculation level, either Metric definition or Entity, determines the granularity of results, and is set in the **Calculation level** field.

-   **Metric definition**: Use this level to produces a single aggregated result from the data across all child metric definitions or child metrics. After building your formula, selecting **Execute** applies the formula and the calculated metric definition data is generated. For more information, see [Configure the formula builder](../task/configure-formula-builder.md).

    The following image shows how calculation occurs at the metric definition level. ![Calculation at the metric definition level.](../image/formula-building-md-level.png)

-   **Entity**: Use this level to generate separate results for each distinct entity associated with the metric definitions used as formula operands. After building and saving your formula, child metrics are automatically created for each entity.

    Selecting **Execute** applies the formula and the metric data is generated. When you select **Aggregate**, the metric data is aggregated and the calculated metric data is generated.

    The following image shows how calculation occurs at the entity level.![Calculation at the entity level.](../image/aggregation-entity-level.png)


-   **[General guidelines for formula building](../../esg-management-reporting/concept/Formula-building-general-guidelines.md)**  
While building a custom formula in a calculated metric definition, keep these general guidelines in mind to easily create your formulas.
-   **[Configure the formula builder](../task/configure-formula-builder.md)**  
Specify the formula context, the tables, and the identifiers before you can build a formula.
-   **[Import a formula into a calculated metric definition](../task/import-a-formula-into-a-cmd.md)**  
Directly import any formula that is stored in Microsoft Excel spreadsheets into a calculated metric definition. This import helps in quickly building your formula for performing calculations.
-   **[Create a formula](../task/create-a-formula.md)**  
Build your own formula using either entities or metric definitions.
-   **[Set default values for CMD formula operands](activate-default-values-for-cmd-calculations.md)**  
Set default values for formula operands so CMD calculations continue when operand data is missing or undefined.

**Parent Topic:**[Configuring GRC: Metrics](configuring-grc-metrics.md)

