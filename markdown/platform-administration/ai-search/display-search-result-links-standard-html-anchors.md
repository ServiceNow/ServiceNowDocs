---
title: Display search result links as standard HTML anchors
description: Increase search flexibility by configuring AI Search to display search result links as standard HTML anchors. You can open these search result links in new browser tabs using your browser's right-click or long-press functionality.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/display-search-result-links-standard-html-anchors.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Display search result links as standard HTML anchors

Increase search flexibility by configuring AI Search to display search result links as standard HTML anchors. You can open these search result links in new browser tabs using your browser's right-click or long-press functionality.

## Before you begin

Role required: admin

## About this task

When AI Search displays search results, it defaults to rendering result titles as links that trigger navigation scripts when you select them. These links aren't standard HTML anchor elements, so you can't open search results in new browser tabs by right-clicking or long-pressing them.

Administrators can override this default behavior and configure AI Search to display search result titles as standard HTML `a` \(anchor\) elements with `href` \(hypertext reference\) attributes. After making this change, you can right-click or long-press search result titles to open results in new tabs in your web browser.

This configuration setting affects how search result title links are displayed in portal search and in global/workspace search.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the navigation filter, enter `sys_properties.list`.

    3.  Press Enter.

2.  Edit the record for the **glide.search.disable\_result\_href** system property.

3.  On the System Property form, change **Value** from **true** to **false**.

4.  Select **Update**.


## Result

Portal search and global/workspace search display search result title links as standard HTML anchor elements with `href` attributes. You can right-click or long-press a search result title to open it in a new tab in your web browser.

**Parent Topic:**[Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/defining-search-app-cfgs-ais.md)

