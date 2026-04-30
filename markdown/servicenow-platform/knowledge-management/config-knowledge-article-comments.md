---
title: Configure article comments instance options
description: Configure the Knowledge Article Comments widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure article comments instance options

Configure the Knowledge Article Comments widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal.

## Before you begin

Role required: sp\_admin or admin

## About this task

The article view page uses the Knowledge Article Comments widget to allow users to rate an article, add a comment, or view existing comments for the article. Use the widget instance options to customize these actions.

## Procedure

1.  Navigate to the Knowledge Management article view page in the Knowledge Management Service Portal.

2.  Control + right-click the comments section.

3.  Click **Instance Options**.

4.  Configure the desired settings for the Knowledge Article Comments widget.

<table id="table_ndg_fcd_hmb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Bootstrap color

</td><td>

The color of the widget header.

</td></tr><tr><td>

CSS

</td><td>

Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://www.servicenow.com/docs/access?context=scss-primer&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td colspan="2">

Other Options

</td></tr><tr><td>

Show User Comments

</td><td>

Displays the field for users to enter comments.Available options:

 -   Yes - displays the field that enables users to enter comments for the article.
-   No - hides the field that enables users to enter comments for the article.
-   Use system property - display or hide the comments field using article view properties.


</td></tr><tr><td>

Add Comment Label

</td><td>

Label for the field to add comments.

</td></tr><tr><td>

Maximum number of attachments that can be attached to a comment

</td><td>

Maximum number of attachments that can be attached to a comment included for a knowledge article.

</td></tr><tr><td>

Maximum attachment file size in MB that can be attached to a comment

</td><td>

Maximum attachment file size in MB that can be attached to a comment included for a knowledge article.

</td></tr></tbody>
</table>5.  Click **Save**.


