---
title: Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) licensing
description: The Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application supports a unit-based subscription licensing model in which you must pay a recurring fee for assets to use the application. You can determine the licensing requirements and costs for these assets based on their resource categories and corresponding subscription unit ratios.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-10-01"
reading_time_minutes: 2
breadcrumb: [Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\), Enterprise Asset Management, IT Asset Management]
---

# Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) licensing

The Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application supports a unit-based subscription licensing model in which you must pay a recurring fee for assets to use the application. You can determine the licensing requirements and costs for these assets based on their resource categories and corresponding subscription unit ratios.

Resource categories group specific types of assets together and enable them to use the features and workflows of an application. Each resource category is associated with a corresponding subscription unit ratio, which you can use to group the given assets against a standardized cost. You can use this information to determine the total licensing requirements and costs for assets within each resource category. For example, a ratio of 25:1 indicates that one subscription is required for every 25 assets within a given resource category. If one subscription costs $100 and you have 50 assets within that resource category, you must purchase two subscriptions for a total of $200.

The Enterprise Asset Management for DCNAM application supports the following resource categories.

**Note:** These resource categories are automatically enabled when you activate the Enterprise Asset Management for DCNAM application on your ServiceNow instance.

<table id="table_kxq_1h3_xgc"><thead><tr><th>

Resource category

</th><th>

Subscription unit ratio

</th><th>

Supported asset model categories

</th></tr></thead><tbody><tr><td>

Critical environment asset

</td><td>

10:1

</td><td>

This resource category supports assets that are associated with the following model categories:-   Automatic Transfer Switch
-   AV Displays
-   AV Equipment
-   Cameras
-   Circuit Breaker
-   Electrical
-   Facility General
-   Fuel Tank
-   Fuse Alarm Panel
-   HVAC
-   Inverter
-   Maintenance Bypass Panel
-   Plumbing
-   Power Generator
-   Power Panel
-   Rectifier
-   Remote Power Panel
-   Security
-   Service Industry Equipment
-   Structure
-   Switchgear
-   Transformer
-   UPS
-   Facilities

</td></tr><tr><td>

Linear asset

</td><td>

2:1

</td><td>

N/A

</td></tr><tr><td>

Linear asset segment

</td><td>

4:1

</td><td>

N/A

</td></tr></tbody>
</table>**Note:** These resource categories support serialized assets only. You are not charged for any consumable assets.

You can view subscription consumption information for the Enterprise Asset Management for DCNAM application by using the ITAM Licensing Resource Counts \[itam\_licensing\_resource\_counts\] table. For more details, see [View your subscription consumption for the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application](../task/view-subscription-consumption-eam-dcnam.md).

**Parent Topic:**[Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](eam-dcnam.md)

