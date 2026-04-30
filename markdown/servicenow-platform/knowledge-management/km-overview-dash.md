---
title: Knowledge Management Overview dashboard
description: The Knowledge Management Overview dashboard provides an overview of various usage metrics associated with knowledge articles. You can view and track knowledge usage and views and direct the efforts of content owners more efficiently.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Knowledge Management Platform Analytics Solutions, Analytics and Reporting Solutions for Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management Overview dashboard

The Knowledge Management Overview dashboard provides an overview of various usage metrics associated with knowledge articles. You can view and track knowledge usage and views and direct the efforts of content owners more efficiently.

**Note:**

If you’re upgrading from a previous release, you must activate the Knowledge Overview \(com.sn\_knowledge\_overview\) plugin to enable the Knowledge Management Overview dashboard. You must also update the navigation path. For more information, see [Update the navigation path for the Knowledge Management Overview dashboard](km-overview-dash-path.md).

Enable the responsive dashboard to optimize analytics by setting the **glide.cms.enable.responsive\_grid\_layout** system property to true.

To access the Knowledge Management Overview dashboard, navigate to **All** &gt; **Self-Service** &gt; **Dashboards**. Search for the Knowledge Management Overview dashboard. The dashboard by default opens with the **Article Lifecycle** tab displayed.

![Knowledge Management Overview dashboard tabs](../image/KMdashboard_overview.gif "Knowledge Management Overview dashboard")

## End user and roles

|End user and goal|Required role|Benefits|
|-----------------|-------------|--------|
|Knowledge Manager: Identify areas of concern and direct resources optimally.|knowledge\_manager|Can review the velocity of content publication and see what content customers are searching for.|
|Knowledge Administrator: Has clear visibility into the usage and quality of knowledge content.|knowledge\_admin|Can plan and direct content creation.|

## Reports

The Knowledge Management Overview dashboard includes various reports.

|Title|Type|Description|
|-----|----|-----------|
|Article life cycle|
|Articles created in the last 30 days|Single score \(![Single score icon](../image/icon-single-score-report-p.png)\)|Total number of articles created in the last 30 days.|
|Number of articles in review|Single score \(![Single score icon](../image/icon-single-score-report-p.png)\)|The total number of articles in review state.|
|Articles by workflow state|Pie \(![Pie icon](../image/pie.png)\)|Displays articles by their workflow state.|
|Articles in review for more than 30 days|Horizontal bar \(![Horizontal bar icon](../image/icon-horizontal-bar-report-p.png)\)|Shows the articles that have been in the review state for more than 30 days.|
|Articles created in the last 30 days|Pivot table \(![Pivot table icon](../image/pivot-table-icon.png)\)|Shows the articles created in the last 30 days and the knowledge bases and workflows associated with the articles.|
|Articles updated in the last 30 days|Pivot table \(![Pivot table icon](../image/pivot-table-icon.png)\)|Shows the articles updated in the last 30 days and the knowledge bases and workflows associated with the articles.|
|Articles expiring in the next 90 days|Pivot table \(![Pivot table icon](../image/pivot-table-icon.png)\)|Shows the articles expiring in the next 90 days and the Shows the articles.|
|Articles in Draft state|Horizontal bar \(![Horizontal bar icon](../image/icon-horizontal-bar-report-p.png)\)|Shows the articles in the draft state.|
|Article Feedback|
|Articles flagged in the last 30 days|Single score \(![Single score icon](../image/icon-single-score-report-p.png)\)|Total number of articles flagged in the last 30 days.|
|Articles marked Not Helpful in the last 30 days|Single score \(![Single score icon](../image/icon-single-score-report-p.png)\)|The total number of articles marked as not helpful in the last 30 days.|
|Comments added in the last 30 days|Single score \(![Single score icon](../image/icon-single-score-report-p.png)\)|Total number of articles that have received comments in the last 30 days.|
|Article ratings in the last 30 days|Pivot table \(![Pivot table icon](../image/pivot-table-icon.png)\)|Displays the ratings for articles that are in different workflow states. It also shows the average rating of articles from different knowledge bases.|
|Average article rating|Single score \(![Singe score icon](../image/icon-single-score-report-p.png)\)|Shows the average rating of articles that have been rated.|
|Article Usage|
|Knowledge use|Vertical bar \(![Vertical bar icon](../image/icon-bar-report-p.png)\)|Shows the count of articles used as attachments.|
|Article views|Vertical bar \(![Vertical bar icon](../image/icon-bar-report-p.png)\)|Shows the count of articles viewed by the knowledge base.|
|Knowledge use trended by month|Line \(![Line icon](../image/icon-line-report.png)\)|Shows the count of articles used as attachments trended by month.|
|Article view count trend by month|Line \(![Line icon](../image/icon-line-report.png)\)|Shows the count of viewed articles trended by month.|
|Author Metrics|
|Monthly knowledge usage by author|Trend \(![Trend icon](../image/icon-trend-report.png)\)|Shows the count of articles used as attachments trended by month with respect to the author.|
|Monthly knowledge views by author|Trend \(![Trend icon](../image/icon-trend-report.png)\)|Shows the count of viewed articles trended by month per author.|
|Articles created by author|Trend \(![Trend icon](../image/icon-trend-report.png)\)|Shows articles created according to knowledge author trended by month.|

