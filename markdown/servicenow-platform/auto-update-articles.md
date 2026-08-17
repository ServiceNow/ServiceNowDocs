---
title: Auto-fix article optimization issues
description: Resolve multiple H1 tag and title relevancy issues found by article optimization scans. Select the articles to fix, and Knowledge Center creates and publishes a new version of each article.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/auto-update-articles.html
release: australia
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 3
keywords: [auto-fix, article optimization, Knowledge Center, H1 tag, title relevancy]
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Auto-fix article optimization issues

Resolve multiple H1 tag and title relevancy issues found by article optimization scans. Select the articles to fix, and Knowledge Center creates and publishes a new version of each article.

## Before you begin

Role required: knowledge manager or knowledge admin.

The article optimization skill must be enabled.

The `sn_km_center.ao_auto_update.enabled` system property must be active. This property is active by default and enables the auto-fix feature.

The **AO auto publish enabled** flag must be enabled on the knowledge base. If this flag is not enabled, all findings for the knowledge base go to manual review and none are fixed automatically.

## About this task

Auto-fix applies to two scan types only: multiple H1 tags and title relevancy. Multiple H1 tag findings use a script-based scan and return a scripted update. Title relevancy findings use an AI model that returns a recommendation and a confidence score. Only findings that meet the configured confidence score threshold are available for auto-fix. All other findings, including article length, image alt tags, and bad links, go to manual review.

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center**.

2.  On the Knowledge Center homepage, select **View top issues** to open the Article Optimization dashboard.

    The **Overview** tab opens by default.

3.  From the **Select a knowledge base** list, select a knowledge base.

    The dashboard shows only the issues found in the selected knowledge base.

4.  Review the summary cards.

    The summary cards show **Issues found**, **Articles with issues**, **Articles ready to auto-fix**, and **Articles needing review** across all scan types.

5.  Under **Issues by type**, select a scan type card that supports auto-fix.

    Only **Multiple H1 tags** and **Title relevancy** support auto-fix. Each card shows the number of articles ready to auto-fix and the number of articles needing review.

6.  In the article list, use the **Show** toggle to display **Articles ready to auto-fix** or **Articles needing review**.

7.  Select the articles to fix, then select **Auto-fix**.

    -   To fix every article for the scan type, select **Auto-fix all articles** on the scan type card, or select **Select all list items** and then select **Auto-fix articles**.
    -   To fix specific articles, select their check boxes, then select **Auto-fix articles** at the top of the list.
    -   To fix a single article, select **Auto-fix** in its row.
    The auto-fix control label shows the count of selected articles, for example **Auto-fix 20 articles**.


## Result

Auto-fix creates a new version of each selected article, applies the update, and publishes it. Publishing follows the existing approval workflow for the knowledge base. If instant publishing is configured, the article publishes immediately. If an approval is required, the article follows the approval rules before publishing.

## What to do next

To ignore a finding that is not correct, select one or more articles and select **Ignore articles**. The ignored findings no longer appear in the list.

Scan types other than multiple H1 tags and title relevancy are available for manual review only. To fix these issues, open an article and review it from the article optimization panel, or open the article from the **Articles** tab list view.

Completed runs appear on the **History** tab. After a run completes, you have five days to revert it. When you revert, the article returns to its previous version, with its content and state as-is. The `sn_km_gen_ai.ai_operation.revert_ttl_days` system property sets this limit, and the default is five days. You can't revert an article if you checked it out and created a new draft after the system published it.

**Related topics**  


[View article optimization analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-article-optimization.md)

[Enable system properties for Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-system-properties-for-KC.md)

[Identify and resolve duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/identify-duplicate-articles.md)

