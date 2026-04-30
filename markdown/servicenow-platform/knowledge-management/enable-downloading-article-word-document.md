---
title: Enable downloading of the source Microsoft Word document for a knowledge article
description: Set the sn\_km\_word.glide.knowman.enable\_document\_download property to enable users to download the source Microsoft Word document of a knowledge article from the knowledge article view page in a portal or workspace.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Knowledge Management - Add-in for Microsoft Word, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable downloading of the source Microsoft Word document for a knowledge article

Set the **sn\_km\_word.glide.knowman.enable\_document\_download** property to enable users to download the source Microsoft Word document of a knowledge article from the knowledge article view page in a portal or workspace.

## Before you begin

Role required: admin

## About this task

When a knowledge article is created using Microsoft Word, users accessing the knowledge article view page in a portal or workspace can download the source Microsoft Word document when the **sn\_km\_word.glide.knowman.enable\_document\_download** property is set to true.

**Note:** After you enable the **sn\_km\_word.glide.knowman.enable\_document\_download** property, the Microsoft Word source document of a knowledge article also might appear in search results as an attachment to the article. Therefore, enabling this property might affect the search relevancy of a knowledge article.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Search for the **sn\_km\_word.glide.knowman.enable\_document\_download** property.

3.  In the **Value** field, enter `true`.

4.  Click **Update**.


