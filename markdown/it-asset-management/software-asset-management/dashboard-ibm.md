---
title: Software Publisher Analytics dashboard for IBM in Software Asset Management classic
description: View compliance analysis results related to IBM on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Publisher Analytics dashboard for IBM in Software Asset Management classic

View compliance analysis results related to IBM on the Software Publisher Analytics dashboard in the Software Asset Management classic application.

Access the Software Publisher Analytics dashboard by navigating to **All** &gt; **Software Asset** &gt; **Publisher Overview**.

**Note:** The add-on IBM publisher pack \(com.sn\_samp\_ibm\) plugin must be installed to view the IBM dashboard tab.

[IBM License Metric Tool \(ILMT\) integration](../concept/setting-up-ibm-ilmt.md#) must be set up to view compliance information.

Results are updated whenever a new reconciliation result is available. You can save charts in PNG or JPG format.

## IBM dashboard

You can manage IBM software using the IBM publisher pack.

![Software Publisher Analytics dashboard for IBM.](../image/publisher-dashboard-ibm.png)

<table id="table_v4y_d5c_fbb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Products out of Compliance

</td><td>

Product Results\[samp\_product\_result\]

</td><td>

Number of products that have at least one software model out of compliance.Select the report to view the results in the [License Workbench](../concept/sam-license-workbench.md).

</td></tr><tr><td>

True-up Cost

</td><td>

Product Results\[samp\_product\_result\]

</td><td>

Cost to be compliant based on the average prices for entitlements for the rights.

</td></tr><tr><td>

% of Total Excess Spend Not In Use

</td><td>

Software Entitlements\[alm\_license\]

</td><td>

Sum of the over-licensed amount over the total of licensed amount.

</td></tr><tr><td>

PVU Subcapacity Consumption Trend

</td><td>

IBM Peak Consumption\[samp\_ilmt\_sw\_install\]

</td><td>

Comparison of the aggregate peak consumption for all products over time.

</td></tr><tr><td>

IBM Software Lifecycle Report

</td><td>

Software Lifecycle Report\[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Number of products in each software lifecycle phase, including End of Extended Support, End of Life, and End of Support.

</td></tr><tr><td>

PVU Subcapacity Breakdown of Top 10 Products

</td><td>

IBM Peak Consumption\[samp\_ilmt\_sw\_install\]

</td><td>

Peak PVU utilization for the top 10 IBM products.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management publisher pack for IBM](../concept/ibm-publisher-pack.md)

