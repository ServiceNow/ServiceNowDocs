---
title: Edit a knowledge article in Microsoft Word
description: Use Microsoft Word to edit a knowledge article originally created in Microsoft Word.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Authoring a knowledge article in Microsoft Word, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a knowledge article in Microsoft Word

Use Microsoft Word to edit a knowledge article originally created in Microsoft Word.

## Before you begin

-   Ensure that the administrator has configured the Knowledge Management - Add-in for Microsoft Word. \(For more information, see [Configure Knowledge Management - Add-in for Microsoft Word](configure-km-add-in-word.md).\)

-   You must have logged in to your ServiceNow instance from the Word Online application. For more information, see [Log in to your ServiceNow instance for authoring knowledge articles in Microsoft Word](authenticate-article-word.md).

-   You must have contribute access to the knowledge article.
-   You must have signed in to your Office 365 account.

## About this task

**Note:** You can’t edit a knowledge article that uses an article template in Word.

## Procedure

1.  From the Microsoft 365 app launcher, select the icon to launch the Microsoft Word app.

    For more information, see [Use the Office 365 app launcher](https://support.microsoft.com/en-us/office/use-the-office-365-app-launcher-0c183e98-a718-4592-9f58-4b47a4074d0b).

2.  In the New section, click **New blank document**, or open any existing Microsoft Word document.

3.  On the Home tab of the Word document, click the Knowledge icon \(![Knowledge icon](../image/word-addin.png)\).

4.  Access the article in the Knowledge Management pane of the Word document.

    -   In the Knowledge Management pane, in the **Search** box, enter the knowledge article number or description.
    -   In the Knowledge Management pane, click a knowledge base to view a list of knowledge articles within the knowledge base. All knowledge bases and associated knowledge articles for which you have contribute or read access appear in the Knowledge Management pane. However, you can edit knowledge articles for which you have contribute access.
5.  In the Knowledge Management pane, click the link to the knowledge article that you want to edit.

6.  If the Document pane of the Word document contains any content, retain or replace the content.

    -   To overwrite the existing content in the Word document with content from the article you selected, click **Replace**.
    -   To keep the existing content in the Word document, click **Retain**.
    **Note:** When you save the article, the Word document content will replace the article content.

7.  If the article versioning feature is enabled, click **Checkout** for a published knowledge article.

    You can edit only the latest version of a knowledge article.

8.  Edit the content of the article in Microsoft Word.

    -   Edit the article content online using Microsoft Word in your browser.
    -   Edit the article content using the Word Desktop app on your computer. In this case, after you complete editing the desktop version of the article content, you must return to the online version in your browser to save the article content in your ServiceNow instance.
    **Tip:** If multiple people with contribute access to the knowledge article need to co-author the same document, you can share the document URL. For more information, see [Document collaboration and co-authoring](https://support.office.com/en-us/article/document-collaboration-and-co-authoring-ee1509b4-1f6e-401e-b04a-782d26f564a4).

9.  In the Knowledge Management pane, click **Save**.

10. Publish the article by clicking **Publish** in the Knowledge Management pane.

    The knowledge article is published depending on the workflow setting of its knowledge base.

    -   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it is scheduled to be published at a later date.
    -   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it is scheduled to be published at a later date.
    For more information, see [Schedule a knowledge article for publishing in Microsoft Word](schedule-article-publishing-word.md).

    If the article versioning feature is enabled, the version number of the knowledge article increments to the next whole number \(for example, from 2.02 to 3.0\). For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md).


