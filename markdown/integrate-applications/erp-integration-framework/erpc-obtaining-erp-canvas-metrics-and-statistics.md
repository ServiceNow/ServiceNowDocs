---
title: Obtaining Zero Copy Connector for ERP metrics and statistics
description: Use the Zero Copy Connector for ERP home page dashboard to obtain statistics about transactions and information to help you troubleshoot.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, metrics, statistic, kpi, dashboard, log]
breadcrumb: [Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Obtaining Zero Copy Connector for ERP metrics and statistics

Use the Zero Copy Connector for ERP home page dashboard to obtain statistics about transactions and information to help you troubleshoot.

View statistics, metrics, and debug information for Zero Copy Connector for ERP on the dashboard. Open links to related Zero Copy Connector for ERP properties, logs, events, and editors.

You must have the sn\_erp\_mining.erp\_admin or sn\_erp\_mining.erp\_user role to view the dashboard.

To view the dashboard, navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**..

Select areas or items in the charts, graphs, and lists on the dashboard to view the underlying records. For example, select a section of a donut chart to see a list of the records for that section.

![Donut chart with one section selected.](../image/erpc-home-page-records.png)

## Dashboard tabs

The **Recent overview** tab contains information obtained in the last 24 hours.

The **Historical overview** tab contains all information.

![Zero Copy Connector for ERP dashboard with recent overview tab open.](../image/erpc-home-page-dashboard.png)

|Title|Type|Description|
|-----|----|-----------|
|Asynchronous transactions by status|Donut|Background jobs, such as extractions, organized by status \(for example, Started, Success, or Error\).|
|Synchronous transactions by status|Donut|User-initiated jobs, such as remote lookup, organized by status \(for example, Started, Success, or Error\).|
|Top 10 slowest asynchronous transactions|Bar|Asynchronous transactions ordered by slowest response time.|
|Top 10 slowest synchronous transactions|Bar|Synchronous transactions ordered by slowest response time.|
|Asynchronous transactions by entity type|Bar|Asynchronous transactions organized by entity type \(for example, read\).|
|Synchronous transactions by entity type|Bar|Synchronous transactions organized by entity type \(for example, read\).|
|Users grouped by role \(available on the **Recent overview** tab for users with the sn\_erp\_mining.erp\_admin role\)|Donut|Users that have initiated a job, organized by role.|

**Parent Topic:**[Configuring Zero Copy Connector for ERP](erp-integration-configuration-overview.md)

