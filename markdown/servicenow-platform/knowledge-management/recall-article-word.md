---
title: Recall an article that is being reviewed in Microsoft Word
description: Recall a knowledge article that is being reviewed and created using Microsoft Word to stop the approval process.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Microsoft Word, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Recall an article that is being reviewed in Microsoft Word

Recall a knowledge article that is being reviewed and created using Microsoft Word to stop the approval process.

## Before you begin

-   You must have contribute access to the knowledge base that stores the knowledge article you want to recall.
-   You must have logged in to your ServiceNow instance from the Word Online application. For more information, see [Log in to your ServiceNow instance for authoring knowledge articles in Microsoft Word](authenticate-article-word.md).

-   You must have signed in to your Office 365 account.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated. For more information, see [Activate the Knowledge Management Advanced plugin](activate-knowledge-advanced-plugin.md).
-   The article versioning feature is enabled. For more information, see [Article versioning](../concept/article-versioning.md).
-   The Knowledge Management - Add-in for Microsoft Word is enabled. \(For more information, see [Configure Knowledge Management - Add-in for Microsoft Word](configure-km-add-in-word.md).\)

## About this task

The author of a knowledge article, knowledge administrators, and system administrators can recall an article. If an ownership group is assigned to a knowledge article, the ownership group manager and ownership group members can also recall the knowledge article.

If a version of a knowledge article is in the Review state, you can recall only the corresponding version to make additional changes. Recalling the article results in a minor version increment.

## Procedure

1.  From the Microsoft 365 app launcher, select the icon to launch the Microsoft Word app.

    For more information, see [Use the Office 365 app launcher](https://support.microsoft.com/en-us/office/use-the-office-365-app-launcher-0c183e98-a718-4592-9f58-4b47a4074d0b).

2.  In the New section, click **New blank document**, or open any existing Microsoft Word document.

3.  On the Home tab of the Word document, click the Knowledge icon \(![Knowledge icon](../image/word-addin.png)\).

4.  In the Knowledge Management pane of the Word document, in the **Search** box, enter the knowledge article title or description.

5.  Click the link to the article in Review state that you want to recall.

6.  On the Knowledge form, click **Recall**.


## Result

The article opens in edit mode and the state of the article is changed to Draft. The version number of the article increments by 0.01.

