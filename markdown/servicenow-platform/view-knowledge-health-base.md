---
title: View the Knowledge Health Score dashboard
description: View the instance-level health score gauge on the Knowledge Management homepage and navigate to the knowledge base health view to identify content that needs attention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/view-knowledge-health-base.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
keywords: [knowledge health score, knowledge management dashboard, knowledge base health, health score gauge]
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View the Knowledge Health Score dashboard

View the instance-level health score gauge on the Knowledge Management homepage and navigate to the knowledge base health view to identify content that needs attention.

## Before you begin

Role required: admin

You must enable [Enable article health score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-healthscore-calculation.md) property and [Enable article optimization recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/enable-ao-recommendations.md) skill to view knowledge health score.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center**.

2.  Locate the **Knowledge Health Score** gauge on the homepage.

    **Note:** The gauge displays the instance-level health score by default, which is an aggregate of all Knowledge Base scores across your instance. To check the health score for a specific Knowledge Base, apply a filter to narrow the view.

3.  Select **View Knowledge Base Health** to open the knowledge base health view.

4.  In the filter bar, select the Knowledge Base you want to review.

    The **Needs Attention** section and the **Articles** list update to reflect the selected Knowledge Base. You can only view knowledge bases you have access to.

5.  You can also select a card in the **Needs Attention** section to filter the **Articles** list to only the articles affected by that parameter.

6.  Select an article from the **Articles** list to open it and navigate to the edit view to improve its health score.

7.  Follow the recommendation displayed for each article to improve its health score.

    For more information, see [Review and optimize articles using Article Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-review-and-optimize-articles.md) and [Generate and edit articles using the article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-edit-knowledge-article.md).

8.  After editing the article, select **Save**.

    **Note:** After you save the article, all Article Optimization scans run automatically. After the scans complete, the health score updates. Refresh the page after 5 to 7 seconds to see the updated score. Acting on these recommendations improves the article health score, which raises the overall knowledge base health score.


## Result

The Knowledge Base health view displays the health scores for the selected Knowledge Base, the finding cards with affected article counts, and the list of articles with their individual health scores.

**Related topics**  


[Enable article health score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-healthscore-calculation.md)

[Enable article optimization recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/enable-ao-recommendations.md)

[View article optimization analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-article-optimization.md)

[Generate and edit articles using the article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-edit-knowledge-article.md)

[Review and optimize articles using Article Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-review-and-optimize-articles.md)

