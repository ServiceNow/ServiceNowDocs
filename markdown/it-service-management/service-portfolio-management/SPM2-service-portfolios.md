---
title: Service Portfolio Management portfolios
description: A service portfolio presents an overall top-level view of your currently available services, possible future services, and services that existed in the past. Evaluate the impact that services have on your business and manage them in a single portfolio or multiple portfolios with unique taxonomy structures, owners, and market scope.
locale: en-US
release: xanadu
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Service Portfolio Management portfolios

A service portfolio presents an overall top-level view of your currently available services, possible future services, and services that existed in the past. Evaluate the impact that services have on your business and manage them in a single portfolio or multiple portfolios with unique taxonomy structures, owners, and market scope.

## Portfolio overview

Gain valuable knowledge about your service portfolios, including an overall performance score and estimated spend. This knowledge helps you budget for your services and make informed decisions about adding new services and retiring services that no longer benefit your business.

Think of a service portfolio as a container that holds a hierarchical organization of definable nodes, services, and service offerings. Taxonomy in Service Portfolio Management refers to the classification of your portfolio layers and associated services \(legacy portfolios use layers; see the **Note**\). Typically, taxonomy is structured from a general, high-level perspective to a specific level, such as a service offering. With this dynamic taxonomy structure, you can organize your service portfolios in various ways.

## Standard and legacy portfolio structures

Prior to the Utah release, Service Portfolio Management provided one portfolio structure. With the Utah release and after, existing customers can move from the legacy structure to the improved standard structure by opting in via a system property.

As an existing customer, opting in to the standard portfolio structure upgrades all your service portfolios. Your existing portfolios remain intact, but performance metrics, scores, and weights are no longer available. With the improved standard service portfolios, you can use key performance indicator \(KPI\) groups in Digital Portfolio Management \(DPM\) to report on services, nodes, and portfolio performance.

The standard portfolio structure provides new features and capabilities for your service portfolios so that you can:

-   Create portfolio structures that have multiple different depths in the same portfolio.
-   Update your portfolio structure over time to add or remove depth in areas of the portfolio, as needed.
-   Work in your existing portfolio in the new structure, even though "layers" are removed.

The portfolio\_admin can navigate to **All** &gt; **Service Portfolio Management** &gt; **Administration** &gt; **Upgrade to Standard Portfolio** to access the system property \[standard\_portfolio\_construct.turn\_on\]. Only existing customers see this menu path. New customers get the standard portfolio structure by default so this menu path isn't available.

**Important:** After you upgrade to the standard portfolio:

-   You can't revert to the legacy portfolio structure.
-   You don't have access to the performance score in Service Owner Workspace because weights and performance metrics are no longer available.

<table id="table_m4b_kxr_fwb"><thead><tr><th>

Opt in to the standard service portfolios

</th><th>

Don't opt in — keep legacy service portfolios

</th></tr></thead><tbody><tr><td>

-   Use node-to-node relationships to create service portfolios with different levels of depth in a single portfolio \(no more layers\).
-   Report on services, nodes, and portfolio performance using KPI groups in DPM.

</td><td>

-   Layered records are required, so you assign nodes to a layer and then reference the parent/child node.
-   Report using portfolio performance metrics, scores, and weights from Service Owner Workspace \(and not KPI groups from DPM\).

</td></tr></tbody>
</table>When you opt in, a dialog box provides these important aspects and considerations. Select the check box if you want to opt in or not \(Yes or No\).

**Important:** The Service Offering Metric Data \[service\_offering\_metric\_data\] table along with the following four indicators have been deprecated in the Utah release:

-   Average SLA Achievement \[ServiceOffering.MetricData.SLA.Daily\]
-   Average Customer Satisfaction \[ServiceOffering.MetricData.CSAT.Daily\]
-   Average Availability \[ServiceOffering.MetricData.Availability.Daily\]
-   Average Request Activity \[ServiceOffering.MetricData.Activity.Daily\]

Therefore, if you have the Vendor Management Workspace application integrated with Service Portfolio Management, and if you are upgrading to the Service Portfolio Management standard portfolio, the metric data from the legacy indicators are no longer available. For information on vendor scores, see [Vendor KPI Groups in Vendor Management Workspace reference](../../vendor-management-workspace/reference/vendor-manager-workspace-default-wep.md).

## Portfolio administration

As a portfolio\_admin user, you can create a single service portfolio or multiple portfolios. If your organization has multiple businesses, you can define multiple portfolios to segregate them by business location, by vendor, or by Chief Information Officer \(CIO\). You can also:

-   Add and remove services from portfolios.
-   Determine how the services in a portfolio are categorized.
-   Update portfolio taxonomy.
-   Update portfolio details.
-   Update services and service offerings \(the service\_editor role also has access\).
-   Reparent services \(the service\_editor role also has access\).

**Parent Topic:**[Exploring Service Portfolio Management](c_ServicePortfolioManagementv2.md)

