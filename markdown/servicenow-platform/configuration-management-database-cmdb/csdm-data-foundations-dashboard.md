---
title: CSDM Data Foundations dashboard
description: The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CSDM and CMDB Data Foundations Dashboards, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM Data Foundations dashboard

The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.

## Access the dashboard

Use either of the following methods to open the dashboard:

Navigate to **All** &gt; **Configuration**, and then select **CSDM Data Foundations Dashboard**.

1.  In CMDB Workspace, navigate to **Workspaces** &gt; **Service Graph Workspace** or**Workspaces** &gt; **CMDB Workspace**.
2.  Select **Management** in the workspace menu bar.
3.  Select **CSDM Data Foundations Dashboard** in the Optimize section of the Management tools.

Select the change dashboard icon \(![Change dashboard.](../../configuration-management/image/ChangeDashboard.png)\) to toggle between the CSDM and CMDB dashboards.

## Example

The reports on each tab display the data metrics that are appropriate for the maturity of your organization's CSDM implementation stage \(foundation, crawl, walk, run, and fly\). A label on each report identifies the metric being displayed.

In this example, a report on the **Run** tab indicates that several business service offerings don't have the required relationships to service instances . With this knowledge, Service owners can add the relationships to confirm that customer service agents get complete information on the impact of applications that are down.

![Run tab on the Data Foundations dashboard.](../image/csdm-data-foundations-dashboard-run.png)

## Tabs on the dashboard

-   Tables in the Foundation domain contain base data that is referenced from or to objects in the other CSDM domains. Before you can use ServiceNow products, you must populate foundational data. See ['Foundation' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-foundation-tab.md).
-   In the Crawl stage, you work on base-system CMDB tables that are associated with IT Service Management \(ITSM\). See ['Crawl' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-crawl-tab.md).
-   In the Walk stage, you identify and populate the network infrastructure CIs and applications that your organization's technical teams support. See ['Walk' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-walk-tab.md).
-   In the Run stage, you set up the relationship between a technology and the business that sells and consumes the technology. See ['Run' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-run-tab.md).
-   When you reach the Fly stage, you have accomplished all or most of the process of implementing the CSDM framework. The fly stage completes the process. See ['Fly' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-fly-tab.md).

## Managing performance of data collection

For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md#section-manage-performance).

**Parent Topic:**[Access CSDM features](csdm-content-frame-using.md)

**Related topics**  


[Configure the CSDM Data Foundations dashboard](../task/csdm-foundations-dashboard.md)

[Monitor health in CSDM and CMDB Data Foundations Dashboards](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md)

