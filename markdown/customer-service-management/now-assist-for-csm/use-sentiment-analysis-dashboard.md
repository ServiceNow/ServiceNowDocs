---
title: Use sentiment analysis dashboard
description: Visualize and interpret customer sentiment across cases using the sentiment analysis dashboard and GenAI insight cards.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-09-25"
reading_time_minutes: 3
keywords: [Sentiment Analysis, GenAI Insights, Case Manager Dashboard, Customer Experience, Base system Insights]
breadcrumb: [Use, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Use sentiment analysis dashboard

Visualize and interpret customer sentiment across cases using the sentiment analysis dashboard and GenAI insight cards.

The sentiment analysis dashboard provides a comprehensive view of customer sentiment across cases and accounts. It includes visualizations, filters, and GenAI-generated insights to help identify sentiment trends, root causes, and performance across channels and assignment groups.

## Entry Point Widget

The sentiment snapshot widget can be accessed from the CSM/FSM configurable workspace home page. It displays a preview of the dashboard of the sentiment trend over time, using the average sentiment score per day. You can access more detailed information by selecting **View dashboard** and navigate to the details page.

**Note:**

-   The sentiment analysis dashboard can only be managed by customer service managers. The sentiment analysis case skill must be activated so that future cases can pick up sentiment.
-   The entry point in Core UI to access the sentiment analysis dashboard is **Customer Service ** &gt; **Now Assist Dashboards** &gt; **Sentiment Analysis Dashboard**.

![Dashboard showing sentiment trend line chart, sentiment breakdown by channel, and multiple bar charts for negative and positive drivers, assignment groups, escalation impact, and case counts by channel.](../image/sentiment-trends-dashboard.png "Sentiment analysis dashboard")

## In-depth View Page – Data Visualizations

|Function|Description|
|--------|-----------|
|**Sentiment trend**|Displays the average sentiment score per day over time.|
|**Record details**|Displays the distribution of cases from very positive up to very negative.|
|**Sentiment breakdown**|Displays sentiment breakdown by Region, Assignment Group, Account, Agent, Category, Product, Channel, Priority, State, and also includes average sentiment and total records data.|
|**Bar Chart**|Displays sentiment split across categories in **Record details**.|
|**Chart Toggle**|Switches between line and bar chart views in **Sentiment trend** and **Record details**.|
|**Time Filters**|Supports Last 7 days, Last 30 days, Last 3 months, Last 6 months, and custom range filtering options.|

## GenAI generated Insight Cards

GenAI insights provide explanations for sentiment trends and root causes in different cases. These include:

-   **Negative sentiment drivers**: Displays factors that most frequently influence negative customer sentiment. The insight is across the date range and displays a reason why cases in these categories were showing that sentiment.
-   **Positive sentiment drivers**: Displays factors that most frequently influence positive customer sentiment. The insight is across the date range and displays a reason why cases in these categories were showing that sentiment.
-   **Top negative assignment groups**: Displays agent assignment groups with the highest levels of negative customer sentiment.
-   **Sentiment change after escalation**: Displays the comparison of customer sentiment before and after a case escalation.
-   **Number of cases by channel**: Displays the distribution of customer sentiment across different communication channels.

**Note:**

All five of these insights look into each case's short description and the last 10 days of comments and work notes to generate these insights.

You can select **Related records** to open a new page with a list that shows the corresponding cases referenced in the graph. You can select the refresh icon ![Reload data](../../workforce-optimization-for-customer-service-configurable/image/refresh-sync-new.png) to see the latest update.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](now-assist-csm-using.md)

**Related topics**  


[Exploring Now Assist for Customer Service Management \(CSM\)](now-assist-csm-exploring.md)

