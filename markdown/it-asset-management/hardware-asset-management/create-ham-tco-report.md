---
title: Create a TCO report in Hardware Asset Workspace
description: Create your own Total Cost of Ownership \(TCO\) report to compare the actual or projected TCO of multiple assets or compare the actual or projected asset TCO with the benchmark cost of the hardware model.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the Total Cost of Ownership of assets, Use, Hardware Asset Management, IT Asset Management]
---

# Create a TCO report in Hardware Asset Workspace

Create your own Total Cost of Ownership \(TCO\) report to compare the actual or projected TCO of multiple assets or compare the actual or projected asset TCO with the benchmark cost of the hardware model.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset analytics**.

2.  In the Comparative reports section, select **New**.

3.  On the form, fill in the fields.

<table id="table_xgt_hj2_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the TCO report.

</td></tr><tr><td>

Type

</td><td>

Type of the TCO report.-   TCO comparison: Costs of multiple assets are compared.
-   TCO vs benchmark: Costs of assets are compared with the benchmark cost.


</td></tr><tr><td>

Report table

</td><td>

Table for Hardware Asset Management, Hardware \(alm\_hardware\).

</td></tr><tr><td>

Total cost type

</td><td>

-   Actual TCO: The TCO value of the selected asset.
    -   If both Actual TCO and Real time report check boxes are selected, the generated TCO report is real-time and offline based on the Real time report selection.
    -   If only Actual TCO is selected, the generated TCO report is offline.
-   Projected TCO: This value is referenced from the following formulas and the generated report is only offline.
    -   When useful life of the asset is equal to or greater than asset life, the Projected TCO \(at end of life\) is calculated by using the following formula:

        ```
Normalized TCO * Useful life
        ```

, where Normalized TCO \(TCO per month\) is

        ```
(Purchase cost / Useful life) + (Sum of operational cost / Asset life)
        ```

.

    -   When useful life of the asset is lower than asset life, the Projected TCO \(at end of life\) is calculated by using the following formula:

        ```
Normalized TCO * Asset life
        ```

, where Normalized TCO \(TCO per month\) is

        ```
(Purchase cost + Sum of operational cost) / Asset life
        ```

.

</td></tr><tr><td>

Description

</td><td>

A brief and meaningful description of the report.

</td></tr><tr><td>

Show benchmark

</td><td>

Option for indicating the benchmark cost in the report.This field appears only when **Type** is selected as **TCO comparison**.

</td></tr><tr><td>

Benchmark model

</td><td>

Asset model to indicate the benchmark cost.When TCO comparison is selected in the Type field, this field appears only when the **Show benchmark** check box is selected.

</td></tr><tr><td>

Real time report

</td><td>

Option for generating real-time data on the report.

</td></tr><tr><td>

Workspace

</td><td>

The workspace you’re working on.Default: HAM

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The TCO report is generated and displayed in the Comparative reports section of the Total Cost of Ownership dashboard.

-   **[Create a TCO report source](create-tco-report-source-ham.md)**  
Create a Total Cost of Ownership \(TCO\) report source for TCO reports.

**Parent Topic:**[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

