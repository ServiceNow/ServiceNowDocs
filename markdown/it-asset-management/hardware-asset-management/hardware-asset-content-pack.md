---
title: Analytics and Reporting Solutions for Hardware Asset Management
description: This Platform Analytics Solution contains preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.View the key metrics on your hardware and consumable models and assets for the entire asset life cycle in the Hardware Asset dashboard.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Explore, Hardware Asset Management, IT Asset Management]
---

# Analytics and Reporting Solutions for Hardware Asset Management

This Platform Analytics Solution contains preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

## Enabling the Performance Analytics Solution

Use the Performance Analytics widgets on the dashboard to visualize data over time, analyze your business processes, and identify areas of improvement. With solutions, you can get value from Performance Analytics for your application with minimal setup.

**Note:** Solutions include some dashboards that are inactive by default. You can activate these dashboards to make them visible to end users according to your business needs.

For unlimited access to all features of this Platform Analytics Solution, purchase a Performance Analytics subscription. For more information, see [Activating your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

To use this Analytics and Reporting Solution, you must be entitled to use Performance Analytics with Hardware Asset Management. For more information about entitlements to Performance Analytics, see [Activating your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

This Out-of-the-box Performance Analytics Solution is available from the ServiceNow Store. To enable this solution, an admin navigates to **System Applications** &gt; **Search ServiceNow Store**. When the landing page for the ServiceNow Store opens, search for Hardware Asset Management. When you have found the Solution, follow the instructions in the Store. The ServiceNow Store has its own documentation.

## Domain separation and 'Run As' user

In some solutions, System Administrator is the **Run As** user for data collection jobs in the Platform Analytics Solutions. In other solutions, the **Run As** user for data collection jobs is left blank. Verify that the **Run As** user exists on the instance, and that this user has the appropriate level of access. An inappropriate **Run As** user can cause errors or limit the data that is collected. This setting only has an effect if domain separation is enabled.

## Performance Analytics dashboards for Hardware Asset Management

**Important:** You can access the Core UI Performance Analytics dashboards only if you have upgraded from prior releases to Xanadu. Beginning with the Xanadu release, the Core UI Performance Analytics dashboards aren't available to new users of Hardware Asset Management.

The Performance Analytics dashboards available for Hardware Asset Management are the following:

-   Hardware Asset Dashboard
-   Hardware Normalization Dashboard
-   My Assets
-   Procurement Overview
-   Asset Contract Overview
-   Asset Overview

Beginning with the Xanadu release, note the following points about the Core UI Performance Analytics dashboards:

-   The Procurement Overview and Asset Contract overview module links are redirected to [Hardware Asset Workspace](../../../product/hardware-asset-management/concept/using-ham-workspace.md).
-   The following Next Experience Platform Analytics dashboard versions of the Asset Overview and My Assets Core UI Performance Analytics dashboards are available:
    -   Analytics Overview: You can access this dashboard by navigating to **Asset** &gt; **Analytics Overview**.
    -   My Assets Analytics: You can access this dashboard by navigating to **Self-Service** &gt; **My Assets Analytics**.

**Note:** After upgrading to Xanadu, you can view both the Core UI Performance Analytics dashboards and the Next Experience Platform Analytics dashboards for Hardware Asset Management. While migrating the Core UI Performance Analytics dashboards to the Next Experience Platform Analytics dashboards, auto-migration is disabled by default to avoid duplicate dashboards.

**Related topics**  


[Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

## Hardware Asset dashboard

View the key metrics on your hardware and consumable models and assets for the entire asset life cycle in the Hardware Asset dashboard.

**Important:** You can access the Hardware Asset dashboard only if you have upgraded from prior releases to Xanadu. Beginning with the Xanadu release, the Hardware Asset Dashboard isn't available to new users of Hardware Asset Management.

Access the Hardware Asset dashboard by navigating to **Asset** &gt; **Hardware Asset Dashboard**.

The results in all the tabs in the Hardware Asset dashboard are updated in real time. Only the reports that display data in the **Lifecycle Overview** sections is updated daily based on scheduled jobs. You can save charts in PNG or JPEG formats for sharing or viewing them locally.

### End user and roles

|End user and goal|Required role|Benefits|
|-----------------|-------------|--------|
|Asset Manager must see patterns in the data all through the asset life cycle.|asset|View reports that provide critical insights on assets such as procurement needs, inventory, and end of life status. You can also view the normalization status and life-cycle overview for hardware and consumable models.|

### Asset Health tab

This tab gives you an overview of hardware and consumable models that are missing purchase information, undiscovered over a period one month of missing, scheduled for retirement, or reported with most incidents. Use Location and Model Category filters to view asset health reports of particular location and model respectively.

|Report|Source table|Description|
|------|------------|-----------|
|Incomplete Assets|Asset \[alm\_asset\]|Asset models without purchase order number, purchase order line, or receiving line.|
|Eligible for Refresh Assets|Hardware \[alm\_hardware\]|Asset nearing end of life and which are eligible for refresh.|
|Asset incident Frequency|Incident \[incident\]|Assets that have been reported with frequent incidents.|
|Active Assets - Not Discovered|Asset \[alm\_asset\]|Assets that aren’t discovered at all or not discovered within one month.|

![Asset Health tab on the Hardware Dashboard.](../../../product/hardware-asset-management/image/asset-health.jpg "Asset Health tab")

### Model Management tab

This tab gives you an overview of hardware and consumable models that are reaching their end of life. You can also view the normalization status, life-cycle overview, and information on the content service library. You can effectively manage your models by viewing their end of life status on a monthly, quarterly, or yearly basis.

<table id="table_cc2_2cl_blb"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hardware Models up for End of Life

</td><td>

Hardware Model Lifecycle \[cmdb\_hardware\_model\_lifecycle\]

</td><td>

The beginning phase of the end of life for hardware models. Shows the count of hardware models whose start date of the end of life phase is either the current month, quarter, or year. **Note:** Only hardware model life cycle records that are active, model status is in production, and life cycle type is Publisher appear in **This month**, **This quarter**, or **This year**.

</td></tr><tr><td>

Normalization Status

</td><td>

Hardware Product Model \[cmdb\_hardware\_product\_model\]

</td><td>

Normalization status of all the hardware models. View the count of hardware models that were normalized and those models that didn't get normalized.

 You can further drill down to view the status of the normalized models: Manually Normalized, Manufacturer Normalized, or Partially Normalized.

 You can drill down to view the status of non-normalized models too: New and Match Not Found.

</td></tr><tr><td>

Lifecycle Overview

</td><td>

Hardware Model Lifecycle \[cmdb\_hardware\_model\_lifecycle\]

</td><td>

The count of hardware models that are present in each life cycle stage: General availability, end of support, end of extended support, and end of sale.

</td></tr><tr><td>

Consumable Models up for End of Life

</td><td>

Consumable Model Lifecycle \[cmdb\_consumable \_model\_lifecycle\]

</td><td>

The beginning phase of the end of life for consumable models. Shows the count of hardware models whose start date of the end of life phase is either the current month, quarter, or year. **Note:** Only consumable model life cycle records that are currently active, model status is in production, and life cycle type is Publisher appear in **This month**, **This quarter**, or **This year**.

</td></tr><tr><td>

Normalization Status

</td><td>

Consumable Product model \[cmdb\_consumable\_product\_model\]

</td><td>

Normalization status of all the consumable models. You can view the count of consumable models that were normalized and those that didn't get normalized.

 You can further drill down to see the status of the normalized models: Manually Normalized, Manufacturer Normalized, or Partially Normalized.

 You can drill down to view the status of non-normalized models too: New and Match Not Found.

</td></tr><tr><td>

Lifecycle Overview

</td><td>

Consumable Model Lifecycle \[cmdb\_consumable\_model\_lifecycle\]

</td><td>

The consumable models that are present in each life-cycle stage: General availability, end of support, end of extended support, and end of sale.

</td></tr><tr><td>

Product Model Status

</td><td>

Product Model \[cmdb\_ model\]

</td><td>

Current count of hardware, consumable, and software models based on the status of the models. Drill down on a model to view the status of that model. For example, click hardware models on the chart to see the status of all the hardware models: In Production, Retired, or sold.

</td></tr><tr><td>

Hardware Model Content Service Download

</td><td>

CDS table \[cds\_client\_schedule\]

</td><td>

The days since the content service library was last downloaded on your instance and the days remaining for the next download to take place.

</td></tr></tbody>
</table>![Model Management tab on the Hardware Dashboard.](../image/model-management.png "Model Management tab")

### Procurement tab

This tab gives you a view of the purchase orders for hardware assets that are pending delivery worldwide. You can also view purchase orders that haven’t yet been sourced and information relating to cost of purchase orders per vendor. You can filter the results in this tab by location and year.

<table id="table_tf3_xfl_blb"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase orders pending delivery

</td><td>

Purchase Order \[proc\_po\]

</td><td>

Purchase orders which aren’t yet received or canceled. Only purchase orders that have a status of ordered or pending delivery are displayed.**Note:** The asset, procurement\_user, inventory\_admin, or contract\_manager role can only access the Purchase Order \[proc\_po\] reports.

</td></tr><tr><td>

Expenditure by Vendor

</td><td>

Purchase Order \[proc\_po\]

</td><td>

The cost that you’ve paid to each of your vendors for procuring the inventory. Only purchase orders that have a status of ordered, pending delivery, or received are displayed.**Note:** The asset, procurement\_user, inventory\_admin, or contract\_manager role can only access the Purchase Order \[proc\_po\] reports.

</td></tr><tr><td>

Orders by Vendor

</td><td>

Purchase Order \[proc\_po\]

</td><td>

Purchase orders that are ordered, pending delivery, or received.**Note:** The asset, procurement\_user, inventory\_admin, or contract\_manager role can only access the Purchase Order \[proc\_po\] reports.

</td></tr><tr><td>

Requests that Require Sourcing

</td><td>

Request \[sc\_request\]

</td><td>

Requests that haven’t yet been addressed. Requests for which either a purchase order or a transfer order hasn’t been initiated.

</td></tr></tbody>
</table>![Procurement tab on the Hardware Dashboard.](../image/procurement-dashboard.png "Procurement tab")

### Inventory tab

This tab shows data regarding your open stock orders. You can also view information about active stock rules, open transfer orders, and requests sourced through stock. You can filter the results in this tab by location and stockroom.

<table id="table_ow5_jhl_blb"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hardware Requests fulfilled from Stock \(YTD\)

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Requests sourced through stock in the current year.**Note:** The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports.

</td></tr><tr><td>

Open Stock Orders

</td><td>

Requested Item \[sc\_req\_item\]

</td><td>

All the stock orders which haven’t yet been fulfilled. The open stock orders can be viewed as numerical data geographically.

</td></tr><tr><td>

Active Stock Rules

</td><td>

Stock Rule \[alm\_stock\_rule\]

</td><td>

Count of active stock rules grouped by model category. If a model of an item that has an active stock rule falls below the threshold value, a new order is placed.

</td></tr><tr><td>

Open Transfer Orders

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Transfer orders not yet delivered or canceled.**Note:** The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports.

</td></tr><tr><td>

Open Audit Assets

</td><td>

Asset Audits \[sn\_hamp\_asset\_audit\]

</td><td>

Audits that are currently new or in progress.**Note:** The asset or inventory\_user role can only access the Asset Audits \[sn\_hamp\_asset\_audit\] reports.

</td></tr><tr><td>

New Hardware Assets Found by Audits

</td><td>

Asset \[alm\_asset\]

</td><td>

The distribution of categories the assets belong to for audits conducted in the last year.

</td></tr><tr><td>

Loaner Asset Order Status

</td><td>

Loaner Asset Order \[sn\_hamp\_loaner\_asset\_order\]

</td><td>

Number of Loaner Asset Orders that are new, deployed, and the ones that are overdue for return.

</td></tr><tr><td>

Open RMA Request Lines

</td><td>

RMA Request Line \[sn\_hamp\_rma\_request\_line\]

</td><td>

List of all the open RMA request lines.**Note:** The asset, itil, or inventory\_user role can only access the RMA Request Line \[sn\_hamp\_rma\_request\_line\] reports.

</td></tr></tbody>
</table>![Inventory tab on the Hardware Dashboard.](../image/inventory-dashboard.png "Inventory tab")

### End of Life tab

View this tab to monitor your assets that are approaching their end of life stage and the disposal status of your assets. You can filter the results in this tab by location, stockroom, and model category. The Model category filter doesn’t apply to **Hardware Asset Disposal Status**.

<table id="table_k5x_yfs_blb"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hardware Nearing End of Warranty

</td><td>

Asset \[alm\_asset\]

</td><td>

Hardware and consumable assets whose warranty expiration date falls in the current month, quarter, or year.**Note:** Only assets that are in the following states appear.

-   in stock
-   in transit
-   in use
-   in maintenance
-   consumed

</td></tr><tr><td>

Hardware Asset Disposal Status

</td><td>

Hardware Disposal Order \[hamp\_hardware\_disposal\]

</td><td>

Status of requests created for hardware assets disposal. The count of new requests appears in **New**. The count of all hardware disposal requests that are currently in scheduling, transit, and confirmation stages are listed under **In progress**.**Pending Documentation** shows all the disposal requests that are in the Documentation stage.

</td></tr><tr><td>

Hardware Assets Disposed \(YTD\)

</td><td>

Asset \[alm\_asset\]

</td><td>

Hardware and consumable assets, based on model category that have been disposed in the current year.

</td></tr><tr><td>

End of Life Method \(YTD\)

</td><td>

Asset \[alm\_asset\]

</td><td>

Count of hardware and consumable assets that are retired, based on their substates. A hardware asset in a retired state has many substates \(disposed, none, sold, vendor credit, and pending disposal\).

</td></tr><tr><td>

Lease Contract Expiration

</td><td>

Contract \[ast\_contract\]

</td><td>

Hardware and consumable assets whose lease expiration date falls in the current month, quarter, or year. It shows only the active contracts.

</td></tr><tr><td>

Hardware Asset Refresh Order

</td><td>

Requested Item \[sc\_req\_item\]

</td><td>

A list of Hardware Asset Refresh ordered.

</td></tr></tbody>
</table>![End of Life tab on the Hardware Dashboard.](../image/endoflife-dashboard.png "End of Life tab")

