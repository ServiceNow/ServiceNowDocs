---
title: Configure the home page widget instance options
description: Configure widget instance options for the widgets used to display popular articles on the Knowledge Management Service Portal homepage.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the home page widget instance options

Configure widget instance options for the widgets used to display popular articles on the Knowledge Management Service Portal homepage.

## Before you begin

Role required: sp\_admin or admin

## About this task

The homepage displays links to the featured, most viewed, and most useful articles using several widgets. The featured articles are displayed based on the keywords associated with the articles. For information on displaying articles in the Featured content section, see [Pin a knowledge article](t_PinAnArticle.md). Most viewed and most useful articles are displayed based on the highest view and use count of the articles.

## Procedure

1.  Navigate to the Knowledge Management Service Portal homepage.

2.  Control + right-click one of the widgets.

3.  Click **Instance Options**.

4.  Configure the desired settings for the widget.

    |Instance option|Description|
    |---------------|-----------|
    |Title|The title of the widget.|
    |Bootstrap color|The color of the widget.|
    |Glyph|An icon that appears in the widget.|
    |CSS|Custom configurations that determine the look and feel of the elements in the widget. For more information, see Service Portal SCSS Primer.|
    |Table|The table that contains the **Source Field** used to provide the featured, most viewed, and most useful articles widget options. The default table is Knowledge \(kb\_knowledge\).|
    |Display Field|The title displayed for each article in the list. By default, this is the article short description.|
    |Secondary Fields|Additional information displayed for each article in the list below the title. By default, this information includes the author, view count, the date that the article was last modified, and the article rating.|
    |Max number of records to show|The maximum number of articles to include in the list.|
    |Show even when empty|Enable this check box to display the widget even if there are no articles in the list.|
    |Show Secondary Fields Label|Enable this check box to display the field labels for the additional information displayed for each article.|
    |Knowledge Base|To restrict the articles that appear in this list to a specific knowledge base, select the knowledge base from the knowledge base list.|

5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

