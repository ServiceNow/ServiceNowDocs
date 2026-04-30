---
title: Software Asset Management dashboard
description: View true-up costs, optimization results, and compliance trend charts on the Software Asset Management dashboard.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Platform Analytics Solution for Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Software Asset Management dashboard

View true-up costs, optimization results, and compliance trend charts on the Software Asset Management dashboard.

**Note:** The Software Asset Management dashboard is no longer available for new Zurich users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Zurich without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Zurich.

-   If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Zurich but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard.
-   If you activated the Software Asset Workspace \(sn\_sam\_workspace\) store application after upgrading to Zurich, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

The Software Asset Management dashboard tab is accessed by navigating to **Software Asset** &gt; **Overview** and selecting **Software Asset Management** from the dashboard list. Select an element within a report to see more information, or add and move widgets as needed.

Results are updated daily, or whenever a new reconciliation result is available, and can be refreshed by selecting the **Refresh** icon for each result. You can also save charts in PNG or JPG formats.

The graphs show important statistics about the software being tracked. In the Overview and Optimization tabs, you can filter by publisher, product, department, and country to narrow the results.

## Overview

The source for overview data is the Product Result \[samp\_product\_result\] table.

![Software Asset Management dashboard](../image/dashboard-sam-overview.png "Overview tab")

<table id="table_vgl_c3y_tz"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total True-up Cost

</td><td>

Cost to be compliant based on the average prices in entitlements for the rights.

</td></tr><tr><td>

Publishers out of Compliance

</td><td>

Number of publishers that have at least one software model out of compliance.Select the report to show the filtered list of records.

</td></tr><tr><td>

Products out of Compliance

</td><td>

Number of products that have at least one software model out of compliance.Select the report to show the filtered list of records.

</td></tr><tr><td>

Potential Savings

</td><td>

Cost saved if removal candidates are reclaimed.

</td></tr><tr><td>

Top 10 Products by True-up Cost

</td><td>

Top 10 products graphed in order of true-up cost.

</td></tr><tr><td>

Top 10 Products by Potential Savings

</td><td>

Top 10 products graphed in order of potential savings.

</td></tr></tbody>
</table>## Optimization

The source for optimization data is the Reclamation Candidate \[samp\_sw\_reclamation\_candidate\] table.

![Optimization tab in the Software Asset Management dashboard](../image/dashboard-sam-optimization.png "Optimization tab")

<table id="table_y3q_r3y_tz"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reclamations Requiring Attention

</td><td>

State is Attention Required

</td></tr><tr><td>

Potential Savings

</td><td>

-   Created on This Year OR Active is true

OR

-   Closed on This Year AND Opened on Last Year

</td></tr><tr><td>

Actual Savings YTD

</td><td>

Closed on This Year AND State is Closed Complete

</td></tr><tr><td>

All Active Reclamations by State

</td><td>

Active is true

</td></tr><tr><td>

Top 10 Active Reclamations Breakdown

</td><td>

Active is true

</td></tr><tr><td>

Actual Savings per Month

</td><td>

State is Closed Complete AND Closed in Last 12 Months

</td></tr></tbody>
</table>[Removal candidate](../task/t_AddAReclCandidate.md) state color key:

|Color|State|
|-----|-----|
|Red|Attention Required|
|Green|Ready|
|Yellow|Awaiting Use|
|Orange|Awaiting Approval|
|Purple|Awaiting Revocation|
|Blue|Closed Complete|

## Compliance Analysis

Compliance analysis consists of time-series data using Performance Analytics to show the compliance trends over time. The for compliance analysis data is the Product Result \[samp\_product\_result\] table.

![Compliance Analysis tab in the Software Asset Management dashboard](../image/SAMCompliance.png "Compliance Analysis tab")

|Report|Description|
|------|-----------|
|True-up Cost|Cost to be compliant based on the average prices for entitlements for the rights.|
|Publishers out of compliance|Number of publishers that have at least one software model out of compliance.|
|Products out of compliance|Number of products that have at least one software model out of compliance.|
|Potential savings|Cost saved if removal candidates are reclaimed.|
|Breakdowns|Shows the detailed list of results based on the widget selected.|
|Records|Shows the detailed list of product results based on the widget selected.|

|Report|Description|
|------|-----------|
|Over-licensed amount|Cost of licenses owned but not being used.|
|Publishers over-licensed|Number of publishers that have at least one software right not being used.|
|Products over-licensed|Number of products that have at least one software right not being used.|
|Breakdowns|Shows the detailed list of results based on the widget selected.|
|Records|Shows the detailed list of product results based on the widget selected.|

**Parent Topic:**[Platform Analytics Solution for Software Asset Management classic](../../../use/dashboards/application-content-packs/software-asset-mgmt-content-pack.md)

