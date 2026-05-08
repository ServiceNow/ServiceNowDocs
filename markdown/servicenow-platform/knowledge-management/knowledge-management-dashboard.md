---
title: Knowledge Management dashboard
description: The Knowledge Management dashboard helps knowledge content owners and managers to determine the usage and quality of their knowledge content. It helps confirm that the proper processes and procedures are being followed for content creation.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Knowledge Management Platform Analytics Solutions, Analytics and Reporting Solutions for Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management dashboard

The Knowledge Management dashboard helps knowledge content owners and managers to determine the usage and quality of their knowledge content. It helps confirm that the proper processes and procedures are being followed for content creation.

**Note:**

-   This documentation refers to the Performance Analytics Content Pack for Knowledge Management v2, introduced in London. It doesn’t refer to the older, deprecated version.
-   To enable the solution for Knowledge Management, an admin can navigate to **Performance Analytics** &gt; **Guided Setup**. Select Get Started then scroll to the section for Knowledge Management. The guided setup takes you through the entire setup and configuration process.
-   To access the Knowledge Management dashboard, navigate to **All** &gt; **Self-Service** &gt; **Dashboard**. In the **Search dashboard** field, search for the Knowledge Management dashboard.

![Tab showing user activity, click rank, and click through rate for any user and authenticated user activities](../../../product/knowledge-management/image/kmdash-content-usage.png "Knowledge Management dashboard- Content Usage tab")

![Tab showing time to publish of articles](../../../product/knowledge-management/image/kmdash-content-gov.png "Knowledge Management dashboard - Content Governance tab")

![The Content Quality view shows the quality index, the percentage of flagged articles, the monthly average rating, and other quality reports](../../../product/knowledge-management/image/kmdash-content-quality.png "Knowledge Management dashboard-Content Quality tab")

|End user and goal|Required role|Benefits|
|-----------------|-------------|--------|
|Knowledge Manager: must identify areas of concern and direct resources optimally.|knowledge\_manager|Can review the velocity of content publication and see what content customers are searching for, to direct the efforts of content owners more efficiently.|
|Knowledge Administrator: needs clear visibility into the usage and quality of knowledge content.|knowledge\_admin|Can plan and direct content creation.|
|Content creator: must see the usage of content they own and areas for improvement|pa\_viewer|Can see what content in their subject area that customers are looking for.|

## CSM Knowledge Management dashboard indicators

The CSM Knowledge Management dashboard provides three views, into content usage, content governance, and content quality.

The Knowledge Management dashboard presents the following key performance indicators:

-   **% of Knowledge Articles Published**

    A daily calculation using the formula `[[Number of knowledge articles published]] / [[Number of knowledge articles active]]`

-   **Monthly Average Article Rating**

    A monthly calculation of the sum of all article ratings for the month divided by the number of knowledge articles rated for the month.

-   **Average select Rank**

    A monthly calculation using the formula `[[Sum of knowledge search ranks]] / Number of knowledge searches with rank]]`

-   **Select Through Rate**

    A monthly calculation using the formula `Number of knowledge searches with rank]] / [[Number of knowledge searches]]`

-   **Average Time to Publish**

    The average time to publish is recalculated daily, as a number of days. The goal of the indicator is for scores to minimize.

-   **Number of Active Users Who Performed Searches- Monthly**

    The number of authenticated users who performed at least one search of the knowledge base in the preceding month. The goal is for the number to maximize.

-   **Number of Active Users Who Viewed Articles- Monthly**

    The number of authenticated users who viewed at least one knowledge article in the preceding month. The goal is for the number to maximize.

-   **Number of Knowledge Searches with Rank- Monthly**

    The number of knowledge searches in a month where the Highest select Rank has a value higher than zero. The goal is for the number to maximize.

-   **Number of Knowledge Searches- Monthly**

    The number of knowledge searches in a month. The goal is for the number to maximize.

-   **Number of Knowledge Articles Rated- Monthly**

    The number of knowledge feedback records created in a month, excluding records where the Rating field is empty. The goal is for the number to maximize.

-   **Number of Knowledge Articles Published**

    A daily count of the total number of knowledge articles that have entered the Published state. The goal is for the number to maximize.

-   **Number of Knowledge Articles Active**

    A daily count of the number of active knowledge articles with up-to-date workflows. The goal is for the number to maximize.

-   **Sum of Knowledge Article Rating- Monthly**

    The monthly sum of all knowledge article ratings. This indicator is used only to calculate the average monthly article rating.

-   **Sum of Knowledge Search Ranks- Monthly**

    The sum of feedback rankings of knowledge searches made in a month, excluding empty Highest select Rank values. The goal is for the number to maximize.

-   **Average select Rank for Unauthenticated Users**

    A monthly calculation of the average select rank for the unauthenticated user activity. The score is calculated according to the formula `[[Sum of Knowledge Search Ranks by Unauthenticated Users- Monthly]]/[[Number of Knowledge Searches by Unauthenticated user with Rank- Monthly]]`. A lower value is better.

-   **Select Through Rate for Unauthenticated Users**

    A monthly calculation of the percentage of select through rate for the unauthenticated user activity. The score is calculated according to the formula `[[Number of Knowledge Searches by Unauthenticated user with Rank- Monthly]]/[[Number of Knowledge Searches by Unauthenticated user- Monthly]] * 100`. A higher value is better.

-   **Number of Knowledge Searches by Unauthenticated Users- Monthly**

    A monthly count of the knowledge searches by unauthenticated users.

-   **Number of Article Views by Unauthenticated Users- Monthly**

    A monthly count of the knowledge articles viewed by unauthenticated users.

-   **Sum of Knowledge Search Ranks by Unauthenticated Users- Monthly**

    A monthly sum of the knowledge search ranks for the unauthenticated user activity.

-   **Number of Knowledge Searches with Rank for Unauthenticated Users- Monthly**

    A monthly count of the knowledge searches with select rank for the unauthenticated user activity.


## Breakdowns

The following breakdowns apply to the indicators on the dashboard:

-   Time to Publish Groups
-   Knowledge Base
-   Knowledge Category

## Data visualizations

The dashboards include the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Articles with Inactive Authors|Column![Column icon](../../performance-analytics/image/column-icon.png)|Active = true and Author.Active = False|
|Invalid Articles|Column![Column icon](../../performance-analytics/image/column-icon.png)|Active = true and Workflow is one of Draft, Review, Published, or Pending Retirement and Valid to is before today and latest = true|
|Articles Created Over 1 Year|Column![Column icon](../../performance-analytics/image/column-icon.png)|Active = true and Created = before 1 year ago|
|Articles not Published|Column![Column icon](../../performance-analytics/image/column-icon.png)|Active = true and Workflow is Draft or Review|

**Parent Topic:**[Knowledge Management Platform Analytics Solutions](knowledge-content-pack.md)

**Related topics**  


[bundle-par.dashboards-landing-page]

