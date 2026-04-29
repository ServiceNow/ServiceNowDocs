---
title: Configure search widget instance options
description: Configure widget instance options for the search widgets on the Knowledge Management Service Portal homepage and search results page.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure search widget instance options

Configure widget instance options for the search widgets on the Knowledge Management Service Portal homepage and search results page.

## Before you begin

Role required: sp\_admin or admin

## About this task

The homepage uses the Knowledge Homepage Search widget and the search results page uses the Knowledge Search widget. Use the widget instance options to customize the search feature for these pages.

## Procedure

1.  Navigate to the Knowledge Management Service Portal homepage or search results page.

2.  Control + right-click the search bar.

3.  Click **Instance Options**.

4.  Configure the search widgets settings.

    |Instance option|Page\(s\)|Description|
    |---------------|---------|-----------|
    |Title|Knowledge Management Service Portal homepage|The title of the search widget. The default for the homepage is Welcome to Knowledge.|
    |Search Placeholder|Knowledge Management Service Portal homepage|Default text that appears in the search bar.|
    |Bootstrap color|Search result page|The color of the search widget.|
    |Bootstrap size|Search result page|The size of the search widget.|
    |Allow Empty Search|Search result page|Allow empty knowledge base searches. The default for the homepage uses the system property. The default for the search results page is Yes.|
    |Allow Instant Search On Keypress|Search result page|Enables instant search results as you type a search term. The default for the search results page uses the system property.|
    |Wait time \(ms\) between searches, if instant search is enabled|Search result page|The time, in milliseconds, to wait between searches if the instant search feature is enabled. The default wait time is 500 ms.|
    |Alternate URL Parameters for Search|Search result page|Alternate parameters that appear in the search results URL. By default these parameters include keyword and query.|
    |Alternate URL Parameters for Language|Search result page|Alternate parameters that appear in the URL denoting the selected language.|
    |Minimum Number of Characters for Search|Both|The minimum number of characters required to generate a search.|
    |Glyph|Both|An icon that appears in the search bar.|
    |CSS|Both|Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://www.servicenow.com/docs/access?context=scss-primer&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).|

5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

