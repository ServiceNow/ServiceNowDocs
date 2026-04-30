---
title: Configure article helpful widget instance options
description: Configure the Knowledge Article Helpful widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure article helpful widget instance options

Configure the Knowledge Article Helpful widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal.

## Before you begin

Role required: sp\_admin or admin

## About this task

The article view page uses the Knowledge Article Helpful widget to allow users to provide feedback on the helpfulness of the article, display a confirmation message after a feedback is provided, and display the percentage of users who found the article to be useful. Use the widget instance options to customize these actions.

## Procedure

1.  Navigate to the Knowledge Management article view page in the Knowledge Management Service Portal.

2.  Control + right-click **Helpful?**

3.  Click **Instance Options**.

4.  Configure the desired settings for the Knowledge Article Helpful widget.

    |Instance option|Description|
    |---------------|-----------|
    |Bootstrap color|The color of the widget header.|
    |CSS|Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://www.servicenow.com/docs/access?context=scss-primer&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).|
    |Show helpful percentage information|Check box to enable the display of percentage of users who found this article to be helpful.|
    |Helpful Action Label|Label for marking this article as helpful or not.|
    |Feedback Message|Text that displays when the user marks the article as helpful or not.|

5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

