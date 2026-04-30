---
title: View trending topics dashboard
description: Identify clusters of related records and visualize their volumes and sentiment trends over time using the trending topics dashboard and GenAI-generated insights.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-09-25"
reading_time_minutes: 3
keywords: [Trending Topics, GenAI Insights, Case Manager Dashboard, Customer Sentiment, Base system Insights]
breadcrumb: [Use, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# View trending topics dashboard

Identify clusters of related records and visualize their volumes and sentiment trends over time using the trending topics dashboard and GenAI-generated insights.

The trending topics dashboard provides visibility into emerging issues across cases. It includes interactive widgets, filters, and GenAI-generated insights to help identify trends, understand root causes, and improve efficiency.

## Widget Overview

|Function|Description|
|--------|-----------|
|Trending Topics Widget|The trending topics widget can be accessed from the CSM/FSM configurable workspace home page and provides an overview of current trends. You can access more detailed information by selecting **View dashboard** and navigate to the details page.|
|Data Scope|The widget displays topics that have at least one open case and a minimum of two total records.|
|Interactivity|When you select on a topic, the dashboard opens pre-filtered topic details for that specific topic.|
|Refresh button|Selecting the **Refresh** icon updates the data for the top 10 trends, ensuring you have the most current information at your fingertips.|

## In-depth View Page Structure

The in-depth view page is divided into two sections: **Data Visualizations** and **GenAI Insight Cards**.

![Dashboard showing trending topics with a table of top 10 trends and metrics, with colorful bar charts for GenAI generated insights on impacted accounts, products, assignment groups, and channels.](../image/trending-topics-dashboard.png "Trending topics dashboard")

## Data Visualizations – List View

Displays the top 10 trending topics with the following attributes:

-   Topic description
-   Total records
-   Total record change
-   Affected accounts
-   Number of agents
-   Customer sentiment

Filters include:

-   Region, Assignment Group, Account, Agent, Category, Product, Channel, Priority, State
-   Time period: Last 7 days, Last 6 months, Last 30 days, Last 3 months, Last 12 months, and Custom range

You can select a topic description link to further in-depth view into the trends over time based on the following filters:

-   Region, Assignment Group, Account, Agent, Category, Product, Channel, Priority, State.
-   Time period: Last 7 days, Last 6 months, Last 30 days, Last 3 months, Last 12 months, and Custom range

The dashboard provides several key features to analyze and understand record trends and case status.

Trend over time:

-   Record Trend Chart: Visualize the total records on a specific date.
-   Record Details Chart: Examine the case status of various cases on a particular date.

Trend Breakdown: Trend analysis can be segmented by multiple categories, including, Region, Assignment Group Account Agent Category Product Channel Priority State.

Affected regions trend insights: For each region, you can view:

-   Average trend score
-   Record count by trend bucket

This breakdown provides a detailed understanding of trends across different dimensions and regions.

## GenAI generated Insight Cards

Automatically generated insights give you information about general trends and include:

-   **Most impacted accounts** - Accounts impacted by the highest volume of records among the top 10 trends. Top insight for the top account with the highest number of cases are displayed.
-   **Most impacted products**- Products impacted by the highest volume of records among the top 10 trends. Top insight for the top product with the highest number of cases are displayed.
-   **Most impacted assignment groups** - Assignment groups impacted by the highest volume of records among the top 10 trend. Top insight for the top assignment group with the highest number of cases are displayed.
-   **Most impacted channels** - Channels impacted by the highest volume of records among the top 10 trends. Top insight for the top channel with the highest number of cases are displayed.

You can select **Related record** to open a new page with a list that shows the corresponding cases referenced in the graph and select the refresh icon ![Refresh data icon](../../workforce-optimization-for-customer-service-configurable/image/refresh-sync-new.png) to see the most recent update.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](now-assist-csm-using.md)

**Related topics**  


[Configure trending topics dashboard](../task/configure-trending-topics-dashboard.md)

