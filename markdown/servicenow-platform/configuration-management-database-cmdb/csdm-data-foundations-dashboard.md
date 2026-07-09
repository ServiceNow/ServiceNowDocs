---
title: CSDM Data Foundations dashboard
description: The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/csdm-data-foundations-dashboard.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-01-22"
reading_time_minutes: 3
breadcrumb: [CSDM and CMDB Data Foundations Dashboards, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM Data Foundations dashboard

The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.

## Access the dashboard

Use either of the following methods to open the dashboard:

Navigate to **All** &gt; **Configuration**, and then select **CSDM Data Foundations Dashboard**.

1.  In CMDB Workspace, navigate to **Workspaces** &gt; **CMDB Workspace**.
2.  Select **Management** in the CMDB Workspace menu bar.
3.  Select **CSDM Data Foundations Dashboard** in the Optimize section of the Management tools.

Select the change dashboard icon \(\[Omitted image "ChangeDashboard.png"\] Alt text: Change dashboard.\) to toggle between the CSDM and CMDB dashboards.

## Example

The reports on each tab display the data metrics that are appropriate for the maturity of your organization's CSDM implementation stage \(foundation, crawl, walk, run, and fly\). A label on each report identifies the metric being displayed.

In this example, a report on the **Run** tab indicates that several business service offerings don't have the required relationships to service instances . With this knowledge, Service owners can add the relationships to ensure that customer service agents get complete information on the upstream impacts of applications that are down.

\[Omitted image "csdm-data-foundations-dashboard-run.png"\] Alt text: Run tab on the Data Foundations dashboard.

## Tabs on the dashboard

-   The Foundation domain involves tables that contain base data that is referenced from or to objects in the other CSDM domains. Foundation data is required before you can use ServiceNow products or add data to the CMDB. See ['Foundation' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-foundation-tab.md).
-   In the Crawl stage, you work on base-system CMDB tables that are associated with IT Service Management \(ITSM\). See ['Crawl' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-crawl-tab.md).
-   In the Walk stage, you identify and populate the network infrastructure CIs and applications that your organization's technical teams support. See ['Walk' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-walk-tab.md).
-   In the Run stage, you set up the relationship between a technology and the business that sells and/or consumes the technology. See ['Run' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-run-tab.md).
-   When you reach the Fly stage, you've accomplished all or most of the process of implementing the CSDM framework. The fly stage completes the process. See ['Fly' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-fly-tab.md).

## Managing performance of data collection

For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/csdm-cmdb-foundations-dashboards.md).

-   **[Auto-generate product models for logical CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-auto-create-prod-model-for-ci.md)**  
Use the CSDM Product Model Assignment job to auto-generate a product model record \(application model, service model, or software model\) for each logical CI that is not yet associated with a product model. Product models are ideal for associating CIs that are parts of a single digital product.

**Parent Topic:**[Managing the CSDM framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-using.md)

**Related topics**  


[Configure the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/common-service-data-model-csdm/csdm-foundations-dashboard.md)

[Monitor system foundations in the CSDM and the CMDB Data Foundations Dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/csdm-cmdb-foundations-dashboards.md)

