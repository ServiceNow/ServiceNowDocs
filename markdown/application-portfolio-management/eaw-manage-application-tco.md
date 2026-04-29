---
title: Exploring total cost of ownership \(TCO\) in Enterprise Architecture Workspace
description: The Application Total Cost of Ownership \(TCO\) plugin helps Enterprise Architects to evaluate the cost of business applications and leverage the application costs to prioritize the application portfolio and align with the organization's business strategy.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring total cost of ownership \(TCO\) in Enterprise Architecture Workspace

The Application Total Cost of Ownership \(TCO\) plugin helps Enterprise Architects to evaluate the cost of business applications and leverage the application costs to prioritize the application portfolio and align with the organization's business strategy.

## Application TCO indicators

The following indicators are added for Application TCO.

|Indicator name|Description|
|--------------|-----------|
|Portfolio TCO|This indicator collects the total cost for a business application for a fiscal period.|

You can view the assessment score of the Portfolio TCO indicator in the Application Rationalization List view.

## Tables installed with Application TCO

The following tables are installed with the Application TCO plugin:

|Table|Description|
|-----|-----------|
|Total Cost of Ownership - sn\_apm\_tco|Stores total cost of ownership details for all the business applications. You can see the details such as Cost type, Expense type, Cost, Fiscal period, Billing date, Vendor, Source, and Source cost type.|
|TCO Cost Type - sn\_apm\_tco\_cost\_type|Stores the TCO cost types within Enterprise Architecture Workspace for analysis and reporting.|
|TCO Source - sn\_apm\_tco\_source|Stores the name of the TCO source.|
|TCO Source Cost Type - sn\_apm\_tco\_source\_cost\_type|Stores the cost types used in the source.|

## Business rules added for Application TCO

The following business rules are added for Application TCO:

|Business rule|Table|Description|
|-------------|-----|-----------|
|Check for duplicate cost type|TCO cost type \[sn\_apm\_tco\_cost\_type\]|Checks for the duplicate name and expense type entry in the TCO cost type table.|
|Check for duplicate source name|TCO source \[sn\_apm\_tco\_source\]|Checks for the duplicate source name entry in the TCO source table.|
|Check for duplicate source cost type|TCO source cost type \[sn\_apm\_tco\_source\_cost\_type\]|Checks for the duplicate source and source cost type entry in the TCO source cost type table.|

## TCO dashboards

The **Portfolio TCO** tab in the **Dashboards** page displays the following dashboards for Application TCO:

-   Business Application TCO for current quarter and previous quarter
-   Business Application TCO trend for year
-   Business Application TCO by application category for current quarter and previous quarter.
-   Business Application TCO by application planned disposition for current quarter

For more details, see [Explore the Enterprise Architecture Workspace dashboard](../../../../use/dashboards/concept/eaw-workspace-dashboard.md).

## Application TCO insights

The Insights section in the Enterprise Architecture Workspace home page displays insights for your business applications.![TCO insights](../../image/eaw-image/TCO-insights.png)

-   **[Manage application total cost of ownership \(TCO\) in Enterprise Architecture Workspace](eaw-app-tco.md)**  
You can configure the application TCO source and cost type in the Enterprise Architecture Workspace.

**Parent Topic:**[Exploring Enterprise Architecture Workspace](../explore-eaw.md)

**Related topics**  


[Manage application total cost of ownership \(TCO\) in Enterprise Architecture Workspace](eaw-app-tco.md)

[Install the Application Total Cost of Ownership \(TCO\) plugin](../../task/eaw-task/eaw-install-app-tco.md)

