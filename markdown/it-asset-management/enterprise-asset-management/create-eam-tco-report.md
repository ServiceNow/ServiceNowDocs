---
title: Create a TCO report in Enterprise Asset Workspace
description: Create a TCO report to compare the actual or projected TCO of assets or to compare the actual or projected asset TCO with the benchmark cost of the enterprise model.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Total Cost of Ownership for enterprise assets, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a TCO report in Enterprise Asset Workspace

Create a TCO report to compare the actual or projected TCO of assets or to compare the actual or projected asset TCO with the benchmark cost of the enterprise model.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Asset analytics** &gt; **Asset TCO**.

2.  Select **New**on the right side of the page.

<table id="choicetable_xfs_scj_hzb"><thead><tr><th align="left" id="d134192e71">

Field

</th><th align="left" id="d134192e74">

Description

</th></tr></thead><tbody><tr><td id="d134192e80">

**Name**

</td><td>

Name of the report.

</td></tr><tr><td id="d134192e89">

**Type**

</td><td>

The type of report. Choose from the following options:-   TCO comparison: Evaluates cost of multiple group of assets with each other.
-   TCO vs benchmark: Evaluates how efficiently an asset or group of assets is managed in relation to industry or market standards.


</td></tr><tr><td id="d134192e106">

**Report Table**

</td><td>

The table this report is based on. This is a read-only field with the value **Enterprise asset**.

</td></tr><tr><td id="d134192e121">

**Total cost type**

</td><td>

The total cost type of the report. -   Actual TCO: The TCO value of the selected asset.
    -   If both Actual TCO and Real time report check boxes are selected, the generated TCO report is real-time based on the Real time report selection.
    -   If only Actual TCO is selected, the generated TCO report is offline.
-   Projected TCO: This value is referenced from the following formulas and the generated report is only offline.
    -   When useful life of the asset is equal to or greater than asset life, the Projected TCO \(at end of life\) is calculated by using the following formula: `Normalized TCO * Useful life`, where Normalized TCO \(TCO per month\) is `(Purchase cost / Useful life) + (Sum of operational cost / Asset life)`.
    -   When useful life of the asset is lower than asset life, the Projected TCO \(at end of life\) is calculated by using the following formula:`Normalized TCO * Asset life`, where Normalized TCO \(TCO per month\) is `(Purchase cost + Sum of operational cost) / Asset life)`.


</td></tr><tr><td id="d134192e167">

**Description**

</td><td>

Description of the report.

</td></tr><tr><td id="d134192e176">

**Show benchmark**

</td><td>

Shows the benchmark threshold on the TCO comparison report.

 This field appears only if you select TCO comparison as your report type.

</td></tr><tr><td id="d134192e191">

**Benchmark model**

</td><td>

The enterprise model for the benchmark threshold.

</td></tr><tr><td id="d134192e203">

**Real time report**

</td><td>

When selected, generates real-time data on the report. You can deselect this check box to make it an offline report.

</td></tr><tr><td id="d134192e212">

**Workspace**

</td><td>

The workspace that you are currently logged into. By default, the value for this field is **EAM**. This is a read-only field.

</td></tr></tbody>
</table>3.  Select **Save**.

    The report is created and the TCO report sources related list appears. You can now add the report sources.


**Parent Topic:**[Configuring Total Cost of Ownership for enterprise assets](../concept/confifure-eam-asset-tco.md)

