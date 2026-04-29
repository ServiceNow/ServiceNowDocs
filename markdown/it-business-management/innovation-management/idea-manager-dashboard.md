---
title: Analyzing idea metrics using Idea Manager dashboard
description: Review, analyze, and manage your ideas effectively by using the Idea Dashboard manager.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Analyzing idea metrics using Idea Manager dashboard

Review, analyze, and manage your ideas effectively by using the Idea Dashboard manager.

The Idea Manager dashboard provides summary of idea metrics and trends such as ideas in different states, age of ideas, categories, and ideas converted to different work entities.

**Note:** Starting with version 2.0.0, the Idea Manager dashboard is available in the Next experience UI Framework which can be accessed from Analytics Idea Manager. The Ideas pane in **Analysis** tab is not supported in the Next experience.

## Idea Manager dashboard in Next experience UI

The Idea Manager dashboard provides comprehensive reports to the idea manager and users with read-only roles for ppm \(sn\_ppm\_read\). The dashboard uses Performance Analytics to provide a trend of historical data as well as regular reports. It provides you an overview of ideas, number of ideas converted into work entities, and trends based on categories, idea submitters, and votes. It helps you to review and analyze ideas and enables you to take required actions for managing your ideas effectively.

![Animated tour of the Idea Manager Dashboard in Next experience UI](../image/idea-manager-dashboard.gif)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Idea Manager - Needs visibility into ideas in different states, number of ideas created, and age of ideas.|idea\_manager|
|Read only roles for PPM - Needs visibility into ideas in different states, number of ideas created, and age of ideas.|sn\_ppm\_read|

## Use case

The dashboard displays ideas related to Project Portfolio Management.

Only ideas associated with categories are displayed in the dashboard. Ideas marked for deletion are not displayed. By default, the dashboard displays one-year data. Use the interactive date filter to view monthly, quarterly, or yearly data.

You can drill down within an idea indicator data for further analysis by navigating to Idea Portal from the dashboard. For example, to view individual records of Open ideas in the Idea Portal, click the **Open ideas** indicator value to open the Analytics Hub. In the Analytics Hub, click **Show Records** to view the list of open ideas, open an idea in the form view, and then click the **Idea Portal** related link to view the idea record in the Idea Portal.

## Indicators

The Summary and Analysis tabs in the dashboard contain the following indicators. The data for ideas is collected from the \[idea\] table.

-   **Open Ideas**

    Count of the ideas that are in Submitted, Need more information, or Under Review state for the current month.

-   **Average Age of Open Ideas**

    The average age of ideas that are in Submitted, Need more information, or Under Review state since their creation, in days, as calculated by the formula `[[PPM:Total Age of Open Ideas]]/[[PPM:Open Ideas]]/24`.

-   **Ideas Converted**

    Count of ideas converted into different work entities such as demand, project, story, or epic based on other plugins.

-   **% of Ideas Converted**

    The percentage of ideas converted into different work entities such as demand, project, story, or epic based on other plugins, as calculated by the formula `[[PPM:Ideas Converted]/[PPM:Active Ideas]] *100`.

-   **Ideas**

    Count of ideas that are in different states. You can view the count of ideas, in different states, created in week, month, quarter, and year.

-   **Active Ideas**

    Count of ideas in Submitted, Need more information, Under review, in backlog, planned and in development state. This indicator is not displayed in dashboard but is used in formula.

-   **Total Age of Open Ideas**

    Total number of days an idea is in state Submitted, Need more information, and Under review before conversion to a work entity. This indicator is not displayed in dashboard but is used in formula.


## Breakdowns

-   PPM - Idea Category
-   PPM - Idea State

## Data visualizations

The dashboard includes the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Ideas by state|Pie chart ![Pie chart](../../performance-analytics/image/donut-icon.png)|Breakdown of the number of ideas in each of the different states.|
|Ideas converted|Pie chart ![Pie chart](../../performance-analytics/image/donut-icon.png)|Breakdown of the number of ideas converted into work entities such as demand and project.|
|Top 10 ideas by votes|Horizontal bar chart ![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)|Top 10 ideas based on the total number of up-votes.|
|Top 10 idea creators|Horizontal bar chart ![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)|Top 10 users based on the number of ideas submitted.|
|Ideas trended by categories|Line chart ![Line chart](../../../reuse/reporting/image/line-multiple.svg)|Trend of the total number of ideas submitted under various categories. The trend is displayed on a monthly basis.|
|Top 10 categories by ideas|Horizontal bar chart ![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)|Top 10 categories based on the number of ideas submitted under each category.|

**Parent Topic:**[Innovation Management](../../../product/innovation-management/concept/innovation-management-landing.md)

