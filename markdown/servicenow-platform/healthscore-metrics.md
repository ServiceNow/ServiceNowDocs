---
title: Article health score
description: Track and improve the quality of your knowledge articles using the article health score. Scan results highlight specific issues to fix, and improvements automatically roll up to your Knowledge Base and instance scores.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/healthscore-metrics.html
release: australia
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 3
breadcrumb: [Knowledge Health Score, Exploring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article health score

Track and improve the quality of your knowledge articles using the article health score. Scan results highlight specific issues to fix, and improvements automatically roll up to your Knowledge Base and instance scores.

## Improving the article health score

When an article has a low health score, the scan parameters identify specific findings you can act on. The improvement process follows three steps:

1.  **Review the findings**. Open the article health score panel from the article's edit view. The panel lists each scan parameter, its individual score, and its contribution to the overall article score. Parameters with low scores have findings that need attention.
2.  **Fix the recommendations**. In the article optimization window you can see the articles and their scores, further you can edit the article to fix the recommendation. Each finding includes a recommendation, for example, adding missing alt text to an image, removing a duplicate H1 heading, or updating a broken link. Apply the recommended changes and save the article.
3.  **Check the updated score**. After saving, switch to the **Health score** tab in the right-side panel to see the recalculated score. The score updates to reflect the improvements made. For more information, see [View the Knowledge Health Score dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-knowledge-health-base.md)

Repeat this process for the parameters with the lowest scores first as these have the highest impact on the overall article score and, by extension, the knowledge base and instance scores.

## Scan parameters

The following parameters are evaluated for every article:

-   **Image alt tags**

    Checks whether images in the article have alternative text. Missing alt text reduces accessibility and affects search indexing.

-   **Multiple H1 tags**

    Detects articles that contain more than one H1 heading. Multiple H1 tags can confuse search engines and indicate poor content structure.

-   **Bad links**

    Identifies broken or unresolvable links within the article. Bad links degrade the reader experience and reduce article trust.

-   **Article length**

    Evaluates whether the article meets the minimum length threshold for adequate content coverage. Articles that are too short may not resolve the reader's issue. Similarly, if articles are too long it might not get retrieved well by AI systems.

-   **Title relevancy**

    Measures how closely the article body aligns with its title. Low relevancy scores indicate a mismatch between what the title promises and what the article delivers.

-   **Article readability**

    Assesses the reading ease of the article based on sentence complexity and vocabulary. Higher readability scores indicate content that is easier to understand for a broader audience.


## How the Knowledge Health Score is calculated

Each article is evaluated against six scan parameters. Every parameter carries a weight that represents its proportional contribution to the overall article score. The article health score is the sum of each parameter's score multiplied by its weight.

To show how a single parameter score feeds into the total, consider the Bad links scan.

For example, an article contains 10 links. The scan detects 4 broken links, leaving 6 good links. The Bad links score is round \(6 / 10 × 100\) = 60. This score of 60 is then multiplied by the Bad links weight of 0.17, contributing 10.2 to the overall article health score. This 10.2 is one of six such contributions, one from each scan parameter as in the following table. When all six are added together \(13.6 + 11.2 + 10.2 + 13.6 + 15.3 + 12.8\), the total is 76.7, which rounds to an article health score of 77.

|Scan parameter|Weight|Parameter score|Contribution to article score|
|--------------|------|---------------|-----------------------------|
|Image alt tags|0.17 \(17%\)|80|13.6|
|Multiple H1 tags|0.16 \(16%\)|70|11.2|
|Bad links|0.17 \(17%\)|60|10.2|
|Article length|0.17 \(17%\)|80|13.6|
|Title relevancy|0.17 \(17%\)|90|15.3|
|Article readability|0.16 \(16%\)|80|12.8|
|**Total**|**1.00 \(100%\)**|—|**76.7 ≈ 77**|

**Note:** Weights are fixed in the current release. The ability to configure custom weights will be available in a future release.

**Related topics**  


[Enable article health score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-healthscore-calculation.md)

[View the Knowledge Health Score dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-knowledge-health-base.md)

