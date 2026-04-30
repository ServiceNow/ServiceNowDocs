---
title: Create an article version by importing a Word document
description: Import a Word document to a knowledge article to create a new version.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an article version by importing a Word document

Import a Word document to a knowledge article to create a new version.

## Before you begin

-   Ensure that the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is installed.
-   You can only upload new versions to articles that are in **Draft** or **Published** state.
-   You cannot upload new versions to articles that are created using an article template or if the article type is **Wiki**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles**.

2.  Click an article.

3.  Click the **Upload New Version** related link.

    **Note:** Any text written in TinyMCE is overwritten once the file is imported.

4.  Add the file you want to import.

5.  Select the **Copy Attachments** check box to copy all attachments to the knowledge article.

    **Note:** If the article is published, the attachments are added to a new article version. If the article is in draft, the attachments are added to the existing knowledge article. The draft article does not appear in the knowledge base \(KB\) for users until it is reviewed and published.

6.  Click **Import**.

    A draft version is created and sent to approvers to approve or reject. Once the article is approved, it is displayed in the **Article Versions** related list.


**Parent Topic:**[Creating and maintaining articles](../../../creating-and-maintaining-articles.md)

