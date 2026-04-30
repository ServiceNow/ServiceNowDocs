---
title: Insert a table of contents in knowledge articles
description: Insert a hierarchical table of contents \(toc\) based on the headings in your knowledge article.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Editing functions for knowledge articles in the HTML editor, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Insert a table of contents in knowledge articles

Insert a hierarchical table of contents \(toc\) based on the headings in your knowledge article.

## Before you begin

Open the knowledge article in which you want to use the HTML editor.

Role required: none

## About this task

You can also use the HTML editor when creating or editing a knowledge article using the Knowledge Management application in the ServiceNow AI Platform interface or in Agent Workspace. To create or edit a knowledge article in the ServiceNow AI Platform interface, see [Create a knowledge article](create-knowledge-article.md) or [Edit a knowledge article](edit-knowledge-article.md). To create or edit a knowledge article in Agent Workspace, see [Create a knowledge article in Agent Workspace](create-article-workspace-1.md) or [Edit a knowledge article in Agent Workspace](edit-article-workspace-1.md).

You can generate a table of contents only if your article uses heading levels from Heading 1 to Heading 3 and is a standard article.

**Note:** Use Format select to set heading levels in the article. You can also configure the HTML toolbar using TinyMCE attributes. For more information, see [Customize TinyMCE attributes](https://www.servicenow.com/docs/access?context=tinymce&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). ![HTML toolbar](../image/km-h1.png)

## Procedure

1.  In the Article body section, place the cursor where you want to insert the table of contents.

2.  Click the table of contents icon \(![Table of Contents icon](../image/toc.png)\) on the HTML toolbar.

    If you do not see the table of contents icon on the toolbar, add it using steps available in [Customize TinyMCE attributes](https://www.servicenow.com/docs/access?context=tinymce&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  Update an existing table of contents by selecting it and then clicking the update icon \(![Update icon](../image/toc-update.png)\) on the HTML toolbar.


## Result

The HTML editor searches for the headings in your content including their levels \(such as Heading 2 or Heading 3\). It then automatically generates a table of contents that contains links to the heading levels from Heading 1 to Heading 3 only. The links to heading levels are indented to show the heading hierarchy.

