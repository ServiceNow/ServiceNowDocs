---
title: Configure knowledge base tile widget instance options
description: Configure widget instance options for the knowledge base tile widgets on the Knowledge Management Service Portal homepage.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure knowledge base tile widget instance options

Configure widget instance options for the knowledge base tile widgets on the Knowledge Management Service Portal homepage.

## Before you begin

Role required: sp\_admin or admin

## About this task

The homepage uses the Knowledge Bases Browse widget to display knowledge base tiles.

## Procedure

1.  Navigate to the Knowledge Management Service Portal homepage.

2.  Control + right-click a knowledge base tile.

3.  Click **Instance Options**.

4.  Configure the desired settings for the knowledge base tile widgets.

    |Instance option|Description|
    |---------------|-----------|
    |Title|The title that appears above the knowledge base tiles. The default is **Explore our Knowledge Bases**.|
    |Bootstrap color|The color of the widget.|
    |CSS|Custom configurations that determine the look and feel of the elements in the widget. For more information, see Service Portal SCSS Primer.|
    |Order By|The order in which the knowledge base tiles appear on the homepage. Use any field on the Knowledge table. If this field is empty, tiles are displayed in alphabetical order. Other available options include article\_count.|
    |Reverse Order|Enable this check box to display knowledge base tiles in the reverse order.|
    |Post Question Label|The label on the button used to post a question. The default is **Ask a Question**.|
    |Create Article Label|The label on the button used to create an article. The default is **Create Article**.|
    |Post Question URL|The parameters that appear in the URL when posting a question.|
    |Create Article URL|The parameters that appear in the URL when creating an article.|

5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

