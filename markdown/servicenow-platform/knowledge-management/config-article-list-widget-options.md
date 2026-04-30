---
title: Configure article list widget instance options
description: Configure widget instance options for the article lists on the Knowledge Management Service Portal homepage.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure article list widget instance options

Configure widget instance options for the article lists on the Knowledge Management Service Portal homepage.

## Before you begin

Role required: sp\_admin or admin

## About this task

The homepage uses the Article List widget to display different lists of articles, including Featured, Most Useful, and Most Viewed.

## Procedure

1.  Navigate to the Knowledge Management Service Portal homepage.

2.  Control + right-click one of the article list headers.

3.  Click **Instance Options**.

4.  Configure the desired settings for the article list widget.

    |Instance option|Description|
    |---------------|-----------|
    |Title|The title of the article list.|
    |Bootstrap color|The color of the widget.|
    |Glyph|An icon that appears in the widget.|
    |CSS|Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://www.servicenow.com/docs/access?context=scss-primer&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).|
    |Table|The table that stores the list articles.|
    |Display Field|The title displayed for each article in the list. By default, this is the article short description.|
    |Secondary Fields|Additional information displayed for each article in the list below the title. By default, this information includes the author, view count, the date that the article was last modified, and the article rating.|
    |Max number of records to show|The maximum number of articles to include in the list.|
    |Show even when empty|Enable this check box to display the article list even if it does not contain any articles.|
    |Show Secondary Fields Label|Enable this check box to display the field labels for the additional information displayed for each article.|
    |Knowledge Base|To restrict the articles that appear in this list to a specific knowledge base, select the knowledge base from the knowledge base list.|

5.  Click **Save**.


