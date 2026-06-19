---
title: Article Optimization with Reading Ease scan
description: The Reading Ease scan runs as part of Article Optimization. The scan is triggered each time you save an article or when the scheduled job runs, or both. When the scan detects readability issues with a knowledge article, review and resolve the findings to improve the readability of the article that scored below the acceptable threshold.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/ai-platform-capabilities/kc-reading-ease-scan.html
release: australia
product: AI Platform Capabilities
classification: ai-platform-capabilities
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 2
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article Optimization with Reading Ease scan

The Reading Ease scan runs as part of **Article Optimization**. The scan is triggered each time you save an article or when the scheduled job runs, or both. When the scan detects readability issues with a knowledge article, review and resolve the findings to improve the readability of the article that scored below the acceptable threshold.

## Before you begin

Verify that **Article Optimization** is activated for your instance.

Role required: agent

## About this task

The Reading Ease scan evaluates the readability of your Knowledge Center articles and provides recommendations in the **Article Optimization** panel.

The configuration and prompt for running the scan follow default settings.

The scan detects articles that score below 60 on the Flesch-Kincaid reading ease scale, and generates a findings card with up to three recommendations at a time. Each finding identifies a specific passage and suggests a rewrite to improve readability.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** &gt; **Lists**.

2.  Select the type of article from the **List** menu \(Unpublished, Published, Retired, and so on\).

3.  Select an existing article from the article list.

4.  Select **Edit** to open the article in the **Article Editor** window.

5.  Select the **Article Optimization** icon to view the list of issues identified in the article, along with the suggestions to fix them.

6.  If the scan detects a reading ease issue, the **Article too complex for audience** card appears along with the details.

    The scan identifies and displays the top three changes with the maximum impact on improving the score.

7.  To open the recommendation detail for a finding, select the **Review** option from the over flow menu available next to the it.

    The modal displays the original text and the recommended replacement text. The recommendation identifies how to improve the passage based on the finding category, such as sentence structure, vocabulary simplification, or active voice.

8.  For each finding, choose one of the following actions:

    -   **Update** — Applies the recommended text change to the article.
    -   **Ignore** — Dismisses the individual finding without making changes.
9.  To act on all findings at once, select **Review all** or **Ignore all** from the findings card.

    When you select **Review all**, all findings appear in the same modal. You can review each finding individually by selecting it, and then select **Update all** to apply all recommended changes at once.

10. Select **Save** to save the article with the applied changes.

    Saving the article triggers the reading ease scan to run again. If the article still scores below 60, a new findings card appears with additional recommendations. Continue reviewing and resolving findings until the article passes the readability threshold.


## Result

The article meets the readability threshold and no further reading ease findings are generated. Most articles reach a passing score after one or two review cycles.

**Parent Topic:**[Using Now Assist in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/using-now-assist-in-km.md)

