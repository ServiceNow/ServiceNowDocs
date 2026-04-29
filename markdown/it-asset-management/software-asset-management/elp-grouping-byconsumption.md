---
title: Effective License Position \(ELP\) report for grouping by consumption
description: Get a comprehensive overview of your software license position across various organizational levels by generating an ELP report.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software reconciliation for compliance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Effective License Position \(ELP\) report for grouping by consumption

Get a comprehensive overview of your software license position across various organizational levels by generating an ELP report.

## Overview of ELP report

An ELP report groups your data on the latest reconciliation results, and shows the consumption cost by department, cost center, or other groups within your organization, without rerunning the reconciliation process.

The ELP report creates a record every time the report is run for every combination of publisher, product, group, subgroup, version, and edition. For each combination, the report calculates the average cost and totals the number of required licenses. The results are presented in a structured, list view for easy analysis and reporting.

All the ELP data reports you have generated can be found in the ELP Grouping subtab, in the License Usage view.

A grouping result is only deleted if you rerun the reconciliation process with grouping for the same publisher and product.

For details on generating an ELP report, see [Generate an Effective License Position \(ELP\) report](../task/generate-elp-report-sam.md).

## Use case scenario of an ELP report

Organization, SampleXYZ, runs the ELP report with the following parameters:

-   Publisher: Microsoft
-   Product: Office
-   Group: Cost Center

Once the report is generated, a record is created for a unique combination of publisher, product, edition, version, license metric, group, and optional subgroup. Open the record to view the cost breakdown for each company group along with a detailed breakdown of the costs for each license metric, edition, and version of software models.

![ELP grouping report](../image/elpgrouping-report.png)

**Parent Topic:**[Software reconciliation for compliance](c_SAMReconciliation.md)

