---
title: Review stale and expiring articles
description: The article optimization scan identifies stale and expiring articles. The scan provides information on knowledge base articles that need review or have reached their expiration date. Select the articles and update or retire them to maintain accurate and current information in the knowledge base.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/kc-review-stale-expiring-articles.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Review stale and expiring articles

The article optimization scan identifies stale and expiring articles. The scan provides information on knowledge base articles that need review or have reached their expiration date. Select the articles and update or retire them to maintain accurate and current information in the knowledge base.

## Before you begin

Role required: knowledge manager, knowledge admin, or knowledge.

The article optimization skill must be enabled.

## About this task

The Knowledge Center Article Optimization scan identifies articles in three states:

-   **Stale article:** An article that was published or last updated before a system-defined number of days \(default: 365 days\). Stale articles may contain outdated information and need review.
-   **Expiring article:** An article approaching its expiration date. The notification alerts you a specified number of days before the article's Valid To date expires \(default: 30 days before expiration\). Expiring articles remain current but will become unavailable soon.
-   **Expired article:** An article that has passed its Valid To date. Expired articles are no longer valid and should be retired or deleted from the knowledge base.

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center** &gt; **List**.

2.  Navigate to an article in your Knowledge Center from the Expiring Articles list and select **Edit**.

3.  Locate the **Stale or expiring article** notification card in **Article Optimization** panel.

4.  Review the article content to determine if it remains accurate and current.

    Check for outdated information, broken links, deprecated processes, or information that no longer applies to your organization. Stale articles have not been updated in a significant time period and may contain obsolete details.

5.  Take one of the following actions based on your review:

    -   Update the article- if the content is mostly accurate but needs corrections or additions, select **Checkout** and update the article text and save your changes.
    -   Extend the expiration date- if the article is current but approaching expiration, extend the **Valid To** date to keep the article available.
    -   Retire or remove the article- if the article is no longer relevant, select **Retire** or **Delete** \(from more actions ellipsis\), to retire or remove it from your knowledge base.
6.  Select **Save** to apply your changes.


**Related topics**  


[Configure stale and expiring articles notification settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/kc-configure-stale-and-expiring-settings.md)

