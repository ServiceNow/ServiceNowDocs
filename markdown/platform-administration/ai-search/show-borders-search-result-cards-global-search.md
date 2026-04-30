---
title: Show borders between search result cards in global search
description: Display borders between search result cards on the global search results page.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 1
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Show borders between search result cards in global search

Display borders between search result cards on the global search results page.

## Before you begin

You must be using Next Experience UI.

Role required: ui\_builder\_admin or admin

## About this task

By default, AI Search displays no borders between search result cards on the global search results page. You can enable display of borders between search result cards on the global search results page by configuring the search result wrapper component for the Unified Navigation app in UI Builder.

## Procedure

1.  Navigate to **All** &gt; **Next Experience Framework** &gt; **UI Builder**.

    UI Builder opens in a new browser tab.

2.  In the list of available experiences, open the **Unified Navigation App** record.

3.  In the Pages and variants listing, open the **Search Results** &gt; **search Default** record.

    UI Builder reloads and displays settings for the Search Results \(search Default\) page.

4.  In the Content pane, select the **Body \(Grid\)** &gt; **Search Result Wrapper 1** component.

    Properties, styles, and events for the selected component appear in the configuration panel.

5.  If a `Different application scope` informational message appears, select **Edit in original scope**.

    The system displays an informational message indicating that you are editing in the application scope.

6.  On the configuration panel's Config tab, select the **Show card border** option.

7.  Select **Save**.


## Result

AI Search displays borders between search result cards on the global search results page.

## What to do next

For details on showing borders between search results cards in portal search, see [Show borders between search result cards in portal search](show-borders-search-result-cards-portal-search.md).

**Parent Topic:**[Configuring AI Search](../concept/configuring-ais.md)

