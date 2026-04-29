---
title: Software Asset Analytics dashboard
description: View true-up costs and license, compliance, and removal summaries trend charts on the Software Asset Analytics dashboard integrated with Performance Analytics.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Platform Analytics Solution for Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Software Asset Analytics dashboard

View true-up costs and license, compliance, and removal summaries trend charts on the Software Asset Analytics dashboard integrated with Performance Analytics.

**Note:** The Software Asset Analytics dashboard is no longer available for new Australia users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Australia without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Australia.

-   If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Australia but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard.
-   If you activated the Software Asset Workspace \(sn\_sam\_workspace\) store application after upgrading to Australia, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

The Software Asset Analytics dashboard tab is accessed by navigating to **Software Asset** &gt; **Overview**. Select an element within a report to see more information, or add and move widgets as needed.

The Overview, License Summary, and Compliance Summary tabs are updated whenever a new reconciliation result is available. Results are updated daily for the **Removal Summary** tab. You can save charts in PNG or JPG formats.

The graphs show important statistics about the software that is being tracked. In the **Overview** and **Optimization**, you can filter by publisher and product to narrow the results.

**Note:** If you are not seeing data in the Overview dashboard, verify the **glide.cms.enable.responsive\_grid\_layout** system property is set to true.

## Overview

![Software Asset Analytics dashboard](../image/dashboard-analytic-overview.png "Software Asset Analytics dashboard")

<table id="table_vgl_c3y_tz"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

True-up Cost

</td><td>

Product Results

</td><td>

Cost to be compliant based on the average prices in entitlements for the rights.

</td></tr><tr><td>

Publishers out of Compliance

</td><td>

Product Results

</td><td>

Number of publishers that have at least one software model out of compliance.Select the report to view the results in the [Software license usage](sam-license-workbench.md).

</td></tr><tr><td>

Products out of Compliance

</td><td>

Product Results

</td><td>

Number of products that have at least one software model out of compliance.Select the report to view the results in the [Software license usage](sam-license-workbench.md).

</td></tr><tr><td>

Potential Savings

</td><td>

Product Results

</td><td>

Cost saved if removal candidates are reclaimed.

</td></tr><tr><td>

True-up Cost Breakdown

</td><td>

Product Results

</td><td>

Cost to be compliant based on the average prices in entitlements for the rights by publisher.

</td></tr><tr><td>

Software Spend Breakdown

</td><td>

License Metric Results

</td><td>

Total software cost of all entitlements not retired by publisher.

</td></tr><tr><td>

End of Life Products

</td><td>

Product Lifecycle \[sam\_sw\_product\_lifecycle\]

</td><td>

Heat map of software product lifecycles that are reaching their end of life cycle. Select to drill-down to the software installations.

</td></tr></tbody>
</table>## License Summary

![License Summary tab shows information pertaining to licenses](../image/SAMDashLicSumNew.png "License Summary tab")

<table id="table_y3q_r3y_tz"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overall Product Compliance

</td><td>

Product Result\[samp\_product\_result\]

</td><td>

Total percent of compliant products.

</td></tr><tr><td>

Percent Spend Not in Use

</td><td>

Product Result and License Metric Results\[samp\_product\_result\] and \[samp\_license\_metric\_result\]

</td><td>

Percent of software spend that is not in use \(over-licensed amount and potential savings\).

</td></tr><tr><td>

Expiring Maintenance Entitlements

</td><td>

Software Entitlement\[alm\_license\]

</td><td>

End date of the total sum of all entitlements that are going to expire within 6 months.

 The total sum of entitlements includes:

-   Perpetual
-   Maintenance
-   Perpetual + Maintenance
-   Upgrade
-   SA
-   Perpetual +SA
-   Step-up

 Select the report to view details about the specific entitlements that are going to expire.

**Note:** Maintenance and SA entitlements are not displayed as the Perpetual entitlements associated with them are displayed.

</td></tr><tr><td>

Software Spend

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Total software cost of all entitlements that are not retired.

</td></tr><tr><td>

Week over Week Cost Summary

</td><td>

Product Result and License Metric Results\[samp\_product\_result\] and \[samp\_license\_metric\_result\]

</td><td>

True-up cost, potential savings, and over-licensed amount for a series of weeks.

</td></tr><tr><td>

Month Over Month Software Spend

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Total software spend in a series of months.

</td></tr><tr><td>

Potential Savings by Optimizing Licenses

</td><td>

Potential Savings by Optimizing Licenses\[samp\_license\_optimization\_summary\]

</td><td>

Potential cost savings for licenses on your physical hosts and clusters that are based on recommended license optimizations.

 **Note:** This report is available only for Microsoft Windows Server and on-premise Red Hat Enterprise Linux \(RHEL\) licenses.

 Select the report to view details about the recommended license optimizations and associated cost savings for each host or cluster. License optimizations include the recommended license, recommended rights, and recommended spend.

</td></tr><tr><td>

Overall Publisher Compliance

</td><td>

Product Result\[samp\_product\_result\]

</td><td>

Percentage of products that are compliant by publisher.

</td></tr><tr><td>

Spend In Use by Publisher

</td><td>

Product Result and License Metric Results\[samp\_product\_result\] and \[samp\_license\_metric\_result\]

</td><td>

Spend in use by publisher = \[\[Total spend\] — \[Over-licensed amount\] — \[Potential savings\]\] / Total spend.

</td></tr><tr><td>

Software Spend by Publisher

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Total software spend by publisher.

</td></tr></tbody>
</table>## Compliance Summary

Compliance summary consists of time-series data using Performance Analytics to show the compliance trends over time. The source for compliance analysis data is the Product Result \[samp\_product\_result\] table.

![Compliance Summary tab](../image/dashboard-analytics-compliance-summary.png "Compliance Summary tab")

|Report|Description|
|------|-----------|
|True-up Cost|Cost to be compliant based on the average prices for entitlements for the rights.|
|Publishers out of compliance|Number of publishers that have at least one software model out of compliance.|
|Products out of compliance|Number of products that have at least one software model out of compliance.|
|Potential savings|Cost saved if removal candidates are reclaimed.|
|Breakdowns|Shows the detailed list of results based on the widget selected. Breakdowns include Publisher, Product, and Scorecard.|
|Records|Shows the detailed list of product results based on the widget selected.|

|Report|Description|
|------|-----------|
|Over-licensed amount|Cost of licenses owned but not being used.|
|Publishers over-licensed|Number of publishers that have at least one software right not being used.|
|Products over-licensed|Number of products that have at least one software right not being used.|
|Breakdowns|Shows the detailed list of results based on the widget selected. Breakdowns include Publisher, Product, and Scorecard.|
|Records|Shows the detailed list of product results based on the widget selected.|

## Removal Summary

The source for removal summary data is the Reclamation Candidate \[samp\_sw\_reclamation\_candidate\] table.

![Removal Summary tab](../image/removal-summary-tab.png)

<table id="table_ixc_kkc_fbb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reclamation Candidates

</td><td>

Total number of active removal candidates with a low usage justification.Select the report to show the filtered list of records.

</td></tr><tr><td>

Restricted Installs Being Removed

</td><td>

Total number of active removal candidates with a restricted software justification.Select the report to show the filtered list of records.

</td></tr><tr><td>

Unlicensed Installs Being Removed

</td><td>

Total number of active removal candidates with an unlicensed justification.Select the report to show the filtered list of records.

</td></tr><tr><td>

Unallocated Installs Being Removed

</td><td>

Total number of active removal candidates with an unallocated justification.Select the report to show the filtered list of records.

</td></tr><tr><td>

Candidates Requiring Attention

</td><td>

Number of removal candidates in the attention required state.Select the report to show the filtered list of records.

</td></tr><tr><td>

Candidates Not Updated in 30 Days

</td><td>

Number of removal candidates that have an updated date value older than 30 days.Select the report to show the filtered list of records.

</td></tr><tr><td>

Actual Savings Year-to-date

</td><td>

Sum of potential savings in a given month of closed complete removal candidates.

</td></tr><tr><td>

Removal Candidates Breakdown

</td><td>

Active removal candidates in various breakdowns \(State, Publisher, Product, Justification, and Last Updated\).

</td></tr></tbody>
</table>**Parent Topic:**[Platform Analytics Solution for Software Asset Management classic](../../../use/dashboards/application-content-packs/software-asset-mgmt-content-pack.md)

