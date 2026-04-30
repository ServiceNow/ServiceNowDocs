---
title: Configure the supplier emissions by model table
description: Configure your supplier emission data collection to capture emissions by specific models of assets to report and calculate Scope 3 emissions accurately.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the Scope 3 dashboard, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Configure the supplier emissions by model table

Configure your supplier emission data collection to capture emissions by specific models of assets to report and calculate Scope 3 emissions accurately.

## Before you begin

Role required: sn\_esg.admin and sn\_esg.program\_manager

## About this task

The data that is configured in the supplier emissions by model table is used in the automated metric definition for supplier data collection. Ensure that data is populated in supplier emissions by model table before the first run date of the metric definition.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Scope 3 configurations** &gt; **Supplier emissions by model**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_vzv_rg3_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Model of your hardware for which you want to collect data.

</td></tr><tr><td>

Supplier emission factor

</td><td>

Measure used to quantify the amount of greenhouse gas \(GHG\) emissions produced per unit of a product or service provided by a supplier.

</td></tr><tr><td>

Supplier emission factor year

</td><td>

Specific year for which the emission factors provided by a supplier are applicable. Because the emission factors can vary every year, select a specific year in this field.

</td></tr><tr><td>

Supplier

</td><td>

Name of the supplier.

</td></tr><tr><td>

Supplier emission factor unit

</td><td>

Unit of measurement used to quantify the emissions per unit of activity, material, or energy consumed. The units supported are as follows.-   **KgCO2e/$**: If you select this unit, then the calculation happens by multiplying the sum of cost by the dollar.
-   **KgCO2e/unit**: If you select this unit, then the calculation happens by multiplying the units by the emission factors.


</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Configuring the Scope 3 dashboard](../concept/configuring-the-scope-3-dashboard.md)

