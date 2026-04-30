---
title: Manage application total cost of ownership \(TCO\)
description: The Application Total Cost of Ownership \(TCO\) plugin helps Enterprise Architects to evaluate the cost of business applications and leverage the application costs to prioritize the application portfolio and align with the organization's business strategy.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Working with an application portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage application total cost of ownership \(TCO\)

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

For more details, see [Working with the Enterprise Architecture Workspace dashboard](../../../../use/dashboards/concept/eaw-workspace-dashboard.md).

## Application TCO insights

The Insights section in the Enterprise Architecture Workspace home page displays insights for your business applications.![TCO insights](../../image/eaw-image/TCO-insights.png)

-   **[Install the Application Total Cost of Ownership \(TCO\) plugin](../../task/eaw-task/eaw-install-app-tco.md)**  
Install the Application TCO store application that you purchased from the ServiceNow Store to make it available on your instance.
-   **[View all total cost of ownership records](../../task/eaw-task/eaw-view-all-tco-records.md)**  
View the list of all total cost of ownership \(TCO\) records in the Enterprise Architecture Workspace.
-   **[Add or edit a total cost of ownership record](../../task/eaw-task/eaw-create-new-tco.md)**  
Create a new entry for total cost of ownership \(TCO\) record to evaluate the cost of your business applications.

**Parent Topic:**[Working with an application portfolio](eaw-app-portfolio.md)

**Related topics**  


[Configure application total cost of ownership \(TCO\) in Enterprise Architecture Workspace](eaw-app-tco.md)

[Install the Application Total Cost of Ownership \(TCO\) plugin](../../task/eaw-task/eaw-install-app-tco.md)

