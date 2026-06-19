---
title: Insert a table of contents in knowledge articles
description: Insert a hierarchical table of contents \(toc\) based on the headings in your knowledge article.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/knowledge-management/insert-toc-html-editor.html
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Editing functions for knowledge articles in the HTML editor, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Insert a table of contents in knowledge articles

Insert a hierarchical table of contents \(toc\) based on the headings in your knowledge article.

## Before you begin

Open the knowledge article in which you want to use the HTML editor.

**Note:** If your article uses a custom template, you may need to create the table of contents manually using the anchor option in the HTML Toolbar and editing the source code.

Role required: none

## About this task

You can also use the HTML editor when creating or editing a knowledge article using the Knowledge Management application in the ServiceNow AI Platform interface or in Agent Workspace. To create or edit a knowledge article in the ServiceNow AI Platform interface, see [Create a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/knowledge-management/create-knowledge-article.md) or [Edit a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/knowledge-management/edit-knowledge-article.md). To create or edit a knowledge article in Agent Workspace, see [Create a knowledge article in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown) or [Edit a knowledge article in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown).

You can generate a table of contents only if your article uses heading levels from Heading 1 to Heading 3 and is a standard article.

**Note:** Use Format select to set heading levels in the article. You can also configure the HTML toolbar using TinyMCE attributes. For more information, see Customize TinyMCE attributes. \[Omitted image "km-h1.png"\] Alt text: HTML toolbar

## Procedure

1.  In the Article body section, place the cursor where you want to insert the table of contents.

2.  Select the table of contents icon \(\[Omitted image "toc.png"\] Alt text: Table of Contents icon\) on the HTML toolbar.

    If you do not see the table of contents icon on the toolbar, add it using steps available in Customize TinyMCE attributes.

3.  Update an existing table of contents by selecting it and then selecting the update icon \(\[Omitted image "toc-update.png"\] Alt text: Update icon\) on the HTML toolbar.

4.  The TOC font defaults to Verdana 8pt, but for those comfortable working in source code, you can edit the default by selecting the source code icon in the HTML Toolbar and changing the font size manually.

    In the following example, the font size is set to 12pt.

    ```
    <div id="mce_14" class="mce-toc" style="font-size: 12pt;">
    <h2>Table of Contents</h2>
    <ul>
    <li><a href="#mcetoc_1jommnuho99">KB Article</a>
    <ul>
    <li><a href="#mcetoc_1jommnuho9a">First section</a></li>
    <li><a href="#mcetoc_1jommnuhp9b">Second Section</a></li>
    <li><a href="#mcetoc_1jommnuhp9c">Third Section</a></li>
    <li><a href="#mcetoc_1jommnuhp9d">Fourth Section</a></li>
    </ul>
    </li>
    </ul>
    </div>
    ```


## Result

The HTML editor searches for the headings in your content including their levels \(such as Heading 2 or Heading 3\). It then automatically generates a table of contents that contains links to the heading levels from Heading 1 to Heading 3 only. The links to heading levels are indented to show the heading hierarchy.

**Note:** To add any additional links, use the anchor option in the HTML Toolbar.

