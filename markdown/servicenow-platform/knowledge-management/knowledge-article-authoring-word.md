---
title: Authoring a knowledge article in Microsoft Word
description: Author and access knowledge articles in Microsoft Word by deploying the Knowledge Management - Add-in for Microsoft Word.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Authoring a knowledge article in Microsoft Word

Author and access knowledge articles in Microsoft Word by deploying the Knowledge Management - Add-in for Microsoft Word.

User with contribute access to a knowledge base can open, create, edit, publish, and search for knowledge articles from within the Knowledge Management pane in Microsoft Word. A user with read access to a knowledge base can view the article in Microsoft Word. The Knowledge Management - Add-in for Microsoft Word is available in the online version of Microsoft Word only.

The Knowledge Management - Add-in for Microsoft Word works with applications that are integrated with the online version of Microsoft Word such as Microsoft SharePoint and Microsoft OneDrive.

Consider the following points when using the Knowledge Management - Add-in for Microsoft Word to maintain knowledge articles:

-   The URL is automatically generated for Word documents created in Microsoft SharePoint and Microsoft OneDrive with business accounts only.

    For other applications, account types and custom SharePoint URLs, you must manually enter the URL in the **Document URL** field on the Knowledge form in Microsoft Word. For more information, see [Create a knowledge article in Microsoft Word](../task/create-article-word.md).

-   The conversion time of a knowledge article from a Microsoft Word document depends on the document size.
-   Headers and footers corresponding to pages in the Microsoft Word document appear as is in the knowledge article. You can remove headers and footers in the Microsoft word document before creating or updating the knowledge article.

**Note:** As an admin, you must create a Restricted Caller Access Privileges record for the Microsoft Word add-in to publish a knowledge article content in scoped knowledge bases. For more information, see Restricted caller access privilege settings.

## Activation information

Activate the Knowledge Management - Add-in for Microsoft Word plugin \(com.snc.knowledge.ms\_word\) to access knowledge articles from within the Microsoft Word online application. For more information, see [Activate Knowledge Management - Add-in for Microsoft Word](../task/activate-km-word-add-in.md).

**Related topics**  


[View a knowledge article in Microsoft Word](../task/view-article-word.md)

[Create a knowledge article in Microsoft Word](../task/create-article-word.md)

[Edit a knowledge article in Microsoft Word](../task/edit-article-word.md)

[Publish a knowledge article in Microsoft Word](../task/publish-article-word.md)

[Configure Knowledge Management - Add-in for Microsoft Word](../task/configure-km-add-in-word.md)

