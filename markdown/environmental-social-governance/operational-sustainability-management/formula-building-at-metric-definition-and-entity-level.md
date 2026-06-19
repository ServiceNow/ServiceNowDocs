---
title: Formula building in a calculated metric definition
description: In a calculated metric definition, you can build formulas using operands, operators, and functions to perform calculations on metric data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/operational-sustainability-management/formula-building-at-metric-definition-and-entity-level.html
release: australia
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Formula building in a calculated metric definition

In a calculated metric definition, you can build formulas using operands, operators, and functions to perform calculations on metric data.

A formula consists of operands, operators, and functions. For example, to calculate the total employee count from two metric definitions \(number of male employees and number of female employees\), the metric definitions are the operands, and the operator is the symbol or function that performs a specific operation on the operands to produce a result. Examples of operators include addition \(+\), subtraction \(-\), multiplication \(\*\), and division \(/\).

## Default values for formula operands

You can set default values for operands in the Calculated Metric Definition Settings table. When a formula encounters an operand with no value, the system applies the configured default value from this table and completes the calculation. You can activate the shipped default record or create a custom entry with preferred values for specific operands.

## Formula versions

Each time you save an edited formula on a calculated metric definition that has been executed, a new formula version is created. Formula versions are listed in the **Versions** related list on the calculated metric definition. Each version has an Applicable from date and an Applicable to date. The Applicable to date is empty for the currently active version and is set to the day before the new version's Applicable from date when a newer version is saved.

You can edit a formula at any time, including after the calculated metric definition has been executed. For more information, see [Edit a calculated metric definition formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/edit-a-calculated-metric-definition-formula.md).

## Formula calculation levels

When you build a formula in a calculated metric definition, you can build it at either the metric definition level or the entity level. Before you save the calculated metric definition and build the formula for metric definition score calculation, you must specify the calculation level in the Calculation level field. The two levels are as follows:

-   **Metric definition**: If you select **Metric definition** in the **Calculation level** field, the data across all child metric definitions or child metrics is used for calculation. When you select **Execute**, the formula is applied and the calculated metric definition data is generated. For more information, see [Configure the formula builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/configure-formula-builder.md).
-   **Entity**: If you select **Entity** in the **Calculation level** field and specify the calculation method using the formula builder, child metrics are created for the calculated metric definition. These metrics are created for each distinct entity associated with the metric definitions used as operands in the formula. When you select **Execute**, the formula is applied and the metric data is generated. When you select Aggregate, the metric data is aggregated and the calculated metric data is generated.

**Important:**

Ad hoc metric data from child metrics is not included in CMD formula calculations at either level. Only data from scheduled child metric tasks feeds into the CMD score. For more information, see [Ad hoc metric data task limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/ad-hoc-metric-data-task-limitations.md).

-   **[General guidelines for formula building](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/Formula-building-general-guidelines.md)**  
While building a custom formula in a calculated metric definition, keep these general guidelines in mind to easily create your formulas.
-   **[Configure the formula builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/configure-formula-builder.md)**  
Specify the formula context, the tables, and the identifiers before you can build a formula.
-   **[Import a formula into a calculated metric definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/import-a-formula-into-a-cmd.md)**  
Directly import any formula that is stored in Microsoft Excel spreadsheets into a calculated metric definition. This import helps in quickly building your formula for performing calculations.
-   **[Create a formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/create-a-formula.md)**  
Build your own formula using either entities or metric definitions.
-   **[Edit a calculated metric definition formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/edit-a-calculated-metric-definition-formula.md)**  
Edit a formula in a calculated metric definition to update the calculation logic or apply changes to historical data.

**Parent Topic:**[Configuring GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/configuring-grc-metrics.md)

