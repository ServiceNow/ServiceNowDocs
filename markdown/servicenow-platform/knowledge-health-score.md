---
title: Knowledge Health score
description: The Knowledge Health Score measures the quality of knowledge articles and your knowledge bases using weighted scan metrics, so you can identify and resolve content gaps that affect discovery and user trust.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-health-score.html
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Exploring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Health score

The Knowledge Health Score measures the quality of knowledge articles and your knowledge bases using weighted scan metrics, so you can identify and resolve content gaps that affect discovery and user trust.

## Benefits

**Governance at the knowledge level**- the roll-up score gives leadership insights about knowledge quality in the home page.

**Visibility into content quality at scale**- instead of manually auditing hundreds of articles and KB-level scores give an immediate signal of where quality is degrading.

**In-context feedback**- The right-side panel shows exactly which parameters are pulling the score down while the author is already in edit mode.

## Prerequisites

You must enable [Enable article health score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-healthscore-calculation.md) property and [Enable article optimization recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/enable-ao-recommendations.md) skill to view knowledge health score.

## How the Knowledge Health Score is calculated

Each knowledge article is scanned against six quality parameters and assigned an article health score from 0 to 100. Knowledge Base scores are the average of all article scores within that Knowledge Base, and the score is the average of all Knowledge Base scores. See [Article health score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/healthscore-metrics.md) for the full parameter breakdown and weighted calculation.

## Score aggregation across levels

Article scores aggregate upward through two additional levels:

-   **Article Health Score**

    The article health score is a numeric value from 0 to 100 that represents the quality of a single knowledge article. It is calculated by scanning the article against six quality parameters and computing a weighted average of the results.

-   **Knowledge Base level**

    The average of all article health scores within a Knowledge Base selected by the user.

-   **Aggregated score**

    The average of all Knowledge Base scores across the Knowledge Base. This is the score displayed on the Knowledge Management homepage gauge by default.


A change to a single article score propagates upward: improving an article raises its Knowledge Base score, which in turn affects the average score appearing in the home page.

## Knowledge Base health

The Knowledge Base health view provides a filtered, drill-down view of health scores across the knowledge bases you have access to. Use this view to identify which knowledge bases and articles need attention and to navigate directly to articles that require fixes.

The view contains three sections:

-   **Needs Attention**

    Displays a health score indicator for the selected Knowledge Base and a set of issue cards, one for each scan parameter. Each card shows the parameter name and the number of articles affected by that finding. Select a card to filter the Articles list to only the articles affected by that parameter. The section updates dynamically when you change the Knowledge Base filter.

-   **Knowledge bases**

    Lists the knowledge bases you have access to.

    |Column|Description|
    |------|-----------|
    |Knowledge Base|Name of the Knowledge Base.|
    |Description|Brief description of the Knowledge Base.|
    |Owner|User responsible for the Knowledge Base.|
    |Health score|Aggregate health score for the Knowledge Base.|

-   **Articles**

    Lists knowledge articles across the selected Knowledge Base.

    |Column|Description|
    |------|-----------|
    |Article|Title of the knowledge article.|
    |Short description|Brief description of the article.|
    |View count|Number of times the article has been viewed.|
    |Knowledge base|Knowledge base the article belongs to.|
    |Health score|Health score for the individual article.|

    Select an article to open it and navigate to the edit view to improve its health score.


**Related topics**  


[Enable article optimization recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/enable-ao-recommendations.md)

[Enable article health score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-healthscore-calculation.md)

[View the Knowledge Health Score dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-knowledge-health-base.md)

