---
title: Article health score
description: Track and improve the quality of your knowledge articles using the article health score. Scan results highlight specific issues to fix, and improvements automatically roll up to your Knowledge Base and instance scores.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/healthscore-metrics.html
release: australia
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 4
breadcrumb: [Knowledge Health Score, Exploring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article health score

Track and improve the quality of your knowledge articles using the article health score. Scan results highlight specific issues to fix, and improvements automatically roll up to your Knowledge Base and instance scores.

## Improving the article health score

When an article has a low health score, the scan parameters identify specific findings you can act on. The improvement process follows three steps:

1.  **Review the findings**. Open the article health score panel from the article's edit view. The panel lists each scan parameter, its individual score, and its contribution to the overall article score. Parameters with low scores have findings that need attention.
2.  **Fix the recommendations**. In the article optimization window, you can see the articles and their scores. Further, you can edit the article to fix the recommendation. Each finding includes a recommendation, for example, adding missing alt text to an image, removing a duplicate H1 heading, or updating a broken link. Apply the recommended changes and save the article.
3.  **Check the updated score**. After saving, switch to the **Health score** tab in the right-side panel to see the recalculated score. The score updates to reflect the improvements made. For more information, see [View the Knowledge Health Score dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/view-knowledge-health-base.md)

Repeat this process for the parameters with the lowest scores first. The articles with the lowest scores have the highest impact on the overall article score and, therefore, the knowledge base and instance scores.

## Scan parameters

The following parameters are evaluated for every article:

-   **Image alt tags**

    Checks whether images in the article have alternative text. Missing alt text reduces accessibility and affects search indexing.

-   **Multiple H1 tags**

    Detects articles that contain more than one H1 heading. Multiple H1 tags can confuse search engines and indicate poor content structure.

-   **Bad links**

    Identifies broken or unresolvable links within the article. Bad links degrade the reader experience and reduce article trust.

-   **Stale and expiring articles**

    Flags if an article is stale \(not been updated in a significant period with potential obsolete details\) or, has expired or, nearing the end of its validity.

-   **Article length**

    Evaluates whether the article meets the minimum length threshold for adequate content coverage. Articles that are too short may not resolve the reader's issue. Similarly, if articles are too long it might not get retrieved well by AI systems.

-   **Title relevancy**

    Measures how closely the article body aligns with its title. Low relevancy scores indicate a mismatch between what the title promises and what the article delivers.

-   **Article readability**

    Assesses the reading ease of the article based on sentence complexity and vocabulary. Higher readability scores indicate content that is easier to understand for a broader audience.


## How the Knowledge Health Score is calculated

The Article health score is an aggregate of the Article optimization score and the Duplicate score, in the ratio of 80% and 20%, respectively. This is the default ratio that can be customized in the health score configuration section of the Knowledge Center.

## Article optimization score

Each article is evaluated against seven scan parameters. Every parameter carries a weight that represents its proportional contribution to the overall article score.

To show how a single parameter score feeds into the total, consider the Bad links scan.

For example, an article contains 10 links. The scan detects 4 broken links, leaving 6 good links. The Bad links score is round \(6 / 10 × 100\) = 60. This score of 60 is then multiplied by the Bad links weight of 0.15. This is one of seven such contributions, one from each scan parameter as in the following table. When all seven are added together \(11.2 + 10.5 + 9.0 + 8.4 + 11.2 + 12.6 + 11.2\), the total is 74.1, which rounds to an article optimization score of 74. The article optimization score contributes to 80% of the aggregate article health score.

|Scan parameter|Weight|Parameter score|Contribution to article optimization score|
|--------------|------|---------------|------------------------------------------|
|Image alt tags|0.14 \(14%\)|80|11.2|
|Multiple H1 tags|0.15 \(15%\)|70|10.5|
|Bad links|0.15 \(15%\)|60|9.0|
|Stale or expiring article|0.14 \(14%\)|60|8.4|
|Article length|0.14 \(14%\)|80|11.2|
|Title relevancy|0.14 \(14%\)|90|12.6|
|Article readability|0.14 \(14%\)|80|11.2|
|**Total**|**1.00 \(100%\)**|—|**74.1 ≈ 74**|

## Duplicate score

When multiple articles cover the same topic, merging them helps users find a single, reliable answer. Presence of potential duplicate articles identified during a scan results in a reduced score \(on a scale of 100\). The duplicate score contributes to 20% of the aggregate article health score. For example, if the duplicate score for an article is 50, \(20/100 x 50\) = 10 is the number considered for calculating the overall score.

The final Article health score would be a sum of 80% of the Article optimization score and 20% of the Duplicate score. Applying this to the above example, the Article health score will be \(80/100\) x 74 + \(20/100\) x 50 = 69.2, that rounds off to 69.

**Note:** Weights are fixed in the default configuration. Alternatively, you can customize these weights in Health score configuration. For more information, see [Health score configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/kc-health-score-configuration.md).

**Related topics**  


[Enable article health score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/enable-healthscore-calculation.md)

[View the Knowledge Health Score dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/view-knowledge-health-base.md)

