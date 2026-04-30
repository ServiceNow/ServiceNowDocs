---
title: Microsoft dashboards in Software Asset Management classic
description: View installations, cost, and compliance for Microsoft software such as SQL Server in the Software Asset Management classic application. View subscription use, cost, and compliance for Microsoft 365.SARAH: One is an analytics dashboard. Do you think we should combine?
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Microsoft dashboards in Software Asset Management classic

View installations, cost, and compliance for Microsoft software such as SQL Server in the Software Asset Management classic application. View subscription use, cost, and compliance for Microsoft 365.

**Note:** The add-on Microsoft publisher pack \(com.snc.samp.microsoft\) plugin must be installed to view the dashboards.

Dashboards are updated whenever a new reconciliation result is available. You can save charts in PNG or JPG format.

## Software Publisher Analytics dashboard for Microsoft

Access the Software Publisher Analytics dashboard for Microsoft by navigating to **Software Asset** &gt; **Publisher Overview**.

![Software Publisher Analytics dashboard for Microsoft.](../image/publisher-dashboard-microsoft.png)

<table id="table_vgl_c3y_tz"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Products out of Compliance

</td><td>

Product Results

</td><td>

Number of products that have at least one software model out of compliance.Select the report to view the results in the [License Workbench](../concept/sam-license-workbench.md).

</td></tr><tr><td>

True-up Cost

</td><td>

Product Results

</td><td>

Cost to be compliant based on the average prices for entitlements for the rights.

</td></tr><tr><td>

Over-Licensed Amount

</td><td>

Product Results

</td><td>

Cost of licenses owned but not being used.

</td></tr><tr><td>

Reclamations Requiring Attention

</td><td>

Reclamation Candidates

</td><td>

State is Attention Required.

</td></tr><tr><td>

Potential Savings

</td><td>

Reclamation Candidates

</td><td>

Cost saved if removal candidates are reclaimed.

</td></tr><tr><td>

Actual Savings Year-to-date

</td><td>

Reclamation Candidates

</td><td>

Closed this Year and the State is set to Closed Complete.

</td></tr><tr><td>

Products by True-up Cost

</td><td>

Product Results

</td><td>

Greatest true-up costs by product.

</td></tr><tr><td>

Products by Potential Savings

</td><td>

Reclamation Candidates

</td><td>

Greatest potential savings by product.

</td></tr><tr><td>

Microsoft Software Lifecycle Report

</td><td>

Software Lifecycle Report

</td><td>

Number of products in each software lifecycle phase, including End of Extended Support, End of Life, and End of Support.

</td></tr><tr><td>

Microsoft Products Across Hybrid Environments

</td><td>

Software Installations

</td><td>

Distribution of Microsoft products across on-premise and cloud environments.

</td></tr><tr><td>

License Types on Microsoft Azure

</td><td>

Software Installations

</td><td>

License types used on Microsoft Azure.

</td></tr><tr><td>

License Types on AWS

</td><td>

Software Installations

</td><td>

License types used on AWS.

</td></tr><tr><td>

SQL Server Install Breakdown

</td><td>

Software Installations

</td><td>

Total software installations per SQL Server.

</td></tr><tr><td>

SQL Server Active Right Breakdown

</td><td>

Software Entitlements

</td><td>

Number of total active rights per SQL Server.

</td></tr></tbody>
</table>## Office 365 &amp; Adobe Cloud dashboard

Only Microsoft 365 software products that are recognized as subscription software are shown. [Microsoft Office 365 integration](../task/set-up-microsoft-office-365.md) must be set up to view compliance information.

![Office 365 & Adobe Cloud dashboard.](../image/publisher-dashboard-o365.png)

<table id="table_kgm_wsc_fbb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of Assigned Subscriptions

</td><td>

Software Subscriptions

</td><td>

Aggregate sum of the number of subscriptions that are used \(for example, user accounts active\).

</td></tr><tr><td>

Percentage of Unused Subscriptions

</td><td>

Software Subscriptions

</td><td>

Ratio of rights available to rights owned.

</td></tr><tr><td>

Total Number of Purchased Subscriptions

</td><td>

License Metric Results

</td><td>

Total number of rights owned.

</td></tr><tr><td>

Current Subscription Spend

</td><td>

License Metric Results

</td><td>

Aggregate sum of the total cost for subscription rights.

</td></tr><tr><td>

Software Models Out of Compliance

</td><td>

Software Model Results

</td><td>

Number of software models out of compliance.Select the report view the results in the [License Workbench](../concept/sam-license-workbench.md).

</td></tr><tr><td>

True-up cost

</td><td>

Software Model Results

</td><td>

Sum of true-up costs on the latest software model results.

</td></tr><tr><td>

Subscriptions Consumption Trend

</td><td>

Software SubscriptionsLicense Metric Results

</td><td>

Trend assigned, active, and available subscriptions.

</td></tr><tr><td>

Assigned Subscription Breakdown

</td><td>

Software Subscriptions

</td><td>

Breakdown of assigned subscriptions by software model.

</td></tr><tr><td>

Available Subscription Breakdown

</td><td>

License Metric Results

</td><td>

Breakdown of total active rights by software model.

</td></tr><tr><td>

Subscription Spend Breakdown

</td><td>

License Metric Results

</td><td>

Breakdown of subscription total cost by product/version/edition \(software model\).

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management publisher pack for Microsoft](../concept/microsoft-publisher-pack.md)

