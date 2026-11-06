---
title: Display search suggestion links as standard HTML anchors
description: Increase search flexibility by configuring AI Search to display search suggestion links as standard HTML anchors. You can open these search suggestion links in new browser tabs using your browser's right-click or long-press functionality.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/display-search-suggestion-links-standard-html-anchors.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Auto-complete suggestions, Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Display search suggestion links as standard HTML anchors

Increase search flexibility by configuring AI Search to display search suggestion links as standard HTML anchors. You can open these search suggestion links in new browser tabs using your browser's right-click or long-press functionality.

## Before you begin

Role required: admin

## About this task

When AI Search displays search suggestions for your search, it defaults to rendering suggestions as links that trigger navigation scripts when you select them. These links aren't standard HTML anchor elements, so you can't open search suggestions in new browser tabs by right-clicking or long-pressing them.

Administrators can override this default behavior and configure AI Search to display search suggestions as standard HTML `a` \(anchor\) elements with `href` \(hypertext reference\) attributes. After making this change, you can right-click or long-press search suggestions to open them in new tabs in your web browser.

This configuration setting affects how search suggestion links are displayed in portal search and in global/workspace search.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the navigation filter, enter `sys_properties.list`.

    3.  Press Enter.

2.  Edit the record for the **glide.search.disable\_suggestion\_href** system property.

3.  On the System Property form, change **Value** from **true** to **false**.

4.  Select **Update**.


## Result

Portal search and global/workspace search display search suggestion links as standard HTML anchor elements with `href` attributes. You can right-click or long-press a search suggestion to open it in a new tab in your web browser.

**Parent Topic:**[Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/auto-complete-ais.md)

