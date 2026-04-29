---
title: Article optimization with article length scan
description: The article length scan is a script‑based, non‑AI scan that runs in the background while authors work on articles. When the scan detects a length issue, an article length card appears in the Article Optimization panel.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article optimization with article length scan

The article length scan is a script‑based, non‑AI scan that runs in the background while authors work on articles. When the scan detects a length issue, an article length card appears in the Article Optimization panel.

## Before you begin

Role required: admin

## About this task

Use Article Length Scan results under Article Optimization for articles to optimize your knowledge center articles.

The configuration and script for running the scan follow default settings.

The scan evaluates articles against two length‑based criteria:

-   **Minimum length for search engine optimization:** Articles with fewer than 300 words are less likely to be prioritized by search engines and might not surface effectively in search results.
-   **Maximum length for AI search:** AI search can’t index articles that exceed 10,000 AI tokens. Because token counts vary by model and tokenization method, the scan uses 10,000 words as a practical indicator for this upper limit.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** &gt; **Lists**.

2.  Select the type of article from the **List** menu \(Unpublished, Published, Retired, and so on\).

3.  Select an existing article from the article list.

4.  Select **Edit** to open the article in the **Article Editor** window.

5.  Select the **Article Optimization** icon to view the list of issues identified in the article, along with the suggestions to fix them.

    ![Article Length Card displayed in the Article Optimization panel](../image/article-length-scan-card.png)

6.  If the scan detects an article length issue, the Article Length card is displayed with the details.

    The scan detects two possible scenarios and the messages are displayed accordingly:

    -   If the article length is below 300 words, it’s flagged as too short for effective search engine optimization.
    -   If the article length exceeds 10,000 words, which is the maximum length that AI search can index, it doesn't appear in AI‑powered search results.
7.  Review the feedback card and make the necessary changes within the article area.

    Key characteristics of this card:

    -   The article length card is only for information and doesn’t include any buttons or actions. You can’t resolve the findings directly from the card and involves adding or reducing content within the article itself.
    -   The card uses a dynamic description, which changes based on whether the article is below 300 words or above 10,000 words. These descriptions are configurable through the scan script.
8.  Select **Save** to save the changes made to the article.

    Once the article length is brought within the acceptable range and saved, the card is automatically removed.


