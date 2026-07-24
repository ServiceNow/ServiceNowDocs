---
title: View a knowledge article in Microsoft Word
description: View a knowledge article in Microsoft Word, including the article number, short description, and article content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-management/view-article-word.html
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Authoring a knowledge article in Microsoft Word, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a knowledge article in Microsoft Word

View a knowledge article in Microsoft Word, including the article number, short description, and article content.

## Before you begin

-   Ensure that the administrator has configured the Knowledge Management - Add-in for Microsoft Word. \(For more information, see [Configure Knowledge Management - Add-in for Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/configure-km-add-in-word.md).\)

-   You must have logged in to your ServiceNow instance from the Word Online application. For more information, see [Log in to your ServiceNow instance for authoring knowledge articles in Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/authenticate-article-word.md).

-   You must have read access to the knowledge article.
-   You must have signed in to your Office 365 account.

## Procedure

1.  From the Microsoft 365 app launcher, select the icon to launch the Microsoft Word app.

    For more information, see [Use the Office 365 app launcher](https://support.microsoft.com/en-us/office/use-the-office-365-app-launcher-0c183e98-a718-4592-9f58-4b47a4074d0b).

2.  In the New section, click **New blank document**, or open any existing Microsoft Word document.

3.  On the Home tab of the Word document, click the Knowledge icon .

4.  Access the article in the Knowledge Management pane of the Word document.

    -   In the Knowledge Management pane, in the **Search** box, enter the knowledge article number or description.
    -   In the Knowledge Management pane, click a knowledge base to view a list of knowledge articles within the knowledge base. All knowledge bases and associated knowledge articles for which you have contribute or read access appear in the Knowledge Management pane
5.  In the Knowledge Management pane, click the link to the knowledge article that you want to view.

    **Tip:** To go back to the previous view in the Knowledge Management pane, click the left caret icon . To go back to the landing screen, click the home icon .


## Result

If a knowledge article was created from the Knowledge Management application in the ServiceNow AI Platform interface, the article content appears in the Document pane and the article details appear in the Knowledge Management pane of the Microsoft Word document.

If a knowledge article was created using another Word document, the document opens in a new browser tab with the content in the Document pane and the article details in the Knowledge Management pane of that document.

**Note:** If the article uses a template, the article opens in the ServiceNow AI Platform interface in a new browser tab. You can’t edit articles with templates in Microsoft Word.

The following article details appear in the Knowledge Management pane.

<table id="table_ldf_vkf_klb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number automatically assigned to the knowledge article.

</td></tr><tr><td>

Knowledge base

</td><td>

Knowledge base that stores the knowledge article and the article category.

</td></tr><tr><td>

Category

</td><td>

Category for the knowledge article. Articles without a category appear in the \(empty\) category.

</td></tr><tr><td>

Ownership Group

</td><td>

Ownership group for the knowledge article. An ownership group consists of a group of members and a manager who are responsible for approvals and feedback tasks. Ownership groups can publish, edit, and retire knowledge articles that they are associated with.**Note:** This field is available only if the **glide.knowman.ownership\_group.enabled** property is enabled. If no ownership group is assigned and approvals are required to publish a knowledge article, it is automatically submitted for approval to the knowledge administrator and knowledge manager. For more information, see [Ownership groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/enable-ownership-group.md).

</td></tr><tr><td>

Workflow

</td><td>

Publishing workflow state of the knowledge article, such as **Draft**, **In Review**, or **Published**.

</td></tr><tr><td>

Version

</td><td>

Version of the knowledge article. This field appears when the article versioning feature is enabled.

</td></tr><tr><td>

Short description

</td><td>

Title of the knowledge article.

</td></tr><tr><td>

Document URL

</td><td>

URL to access the document in the Word Online application.

</td></tr><tr><td>

Scheduled publish date

</td><td>

Future date when the knowledge article will be published automatically. For more information, see [Schedule a knowledge article for publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/schedule-article-publishing.md).

</td></tr><tr><td>

Valid to

</td><td>

Date this knowledge article expires.

</td></tr></tbody>
</table>**Related topics**  


[Create a knowledge article in Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/create-article-word.md)

[Edit a knowledge article in Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/edit-article-word.md)

