---
title: Publish a knowledge article in Microsoft Word
description: Use the Word Online application to publish a knowledge article originally created in Microsoft Word to make it available to users.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Microsoft Word, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Publish a knowledge article in Microsoft Word

Use the Word Online application to publish a knowledge article originally created in Microsoft Word to make it available to users.

## Before you begin

-   Ensure that the administrator has configured the Knowledge Management - Add-in for Microsoft Word. \(For more information, see [Configure Knowledge Management - Add-in for Microsoft Word](configure-km-add-in-word.md).\)

-   You must have logged in to your ServiceNow instance from the Word Online application. For more information, see [Log in to your ServiceNow instance for authoring knowledge articles in Microsoft Word](authenticate-article-word.md).

-   You must have contribute access to the knowledge base within which you want to publish the knowledge article.
-   You must have signed in to your Office 365 account.

## Procedure

1.  From the Microsoft 365 app launcher, select the icon to launch the Microsoft Word app.

    For more information, see [Use the Office 365 app launcher](https://support.microsoft.com/en-us/office/use-the-office-365-app-launcher-0c183e98-a718-4592-9f58-4b47a4074d0b).

2.  In the New section, click **New blank document**, or open any existing Microsoft Word document.

3.  On the Home tab of the Word document, click the Knowledge icon \(![Knowledge icon](../image/word-addin.png)\).

4.  Access the article in the Knowledge Management pane of the Word document.

    -   In the Knowledge Management pane, in the **Search** box, enter the knowledge article number or description.
    -   In the Knowledge Management pane, click the knowledge base to view a list of knowledge articles within the knowledge base.
5.  In the Knowledge Management pane, click the link to the knowledge article that you want to publish.

6.  On the Knowledge form, click **Publish**.


## Result

A knowledge article is published depending on the workflow setting of its knowledge base:

-   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it is scheduled to be published at a later date.
-   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it is scheduled to be published at a later date.

For more information, see [Schedule a knowledge article for publishing in Microsoft Word](schedule-article-publishing-word.md).

If the article versioning feature is enabled, the version of the article is incremented based on the [version number pattern](../concept/knowledge-article-version-numbers.md).

