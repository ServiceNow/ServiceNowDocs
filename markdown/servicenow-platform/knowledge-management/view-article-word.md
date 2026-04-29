---
title: View a knowledge article in Microsoft Word
description: View a knowledge article in Microsoft Word, including the article number, short description, and article content.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Authoring a knowledge article in Microsoft Word, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a knowledge article in Microsoft Word

View a knowledge article in Microsoft Word, including the article number, short description, and article content.

## Before you begin

-   Ensure that the administrator has configured the Knowledge Management - Add-in for Microsoft Word. \(For more information, see [Configure Knowledge Management - Add-in for Microsoft Word](configure-km-add-in-word.md).\)

-   You must have logged in to your ServiceNow instance from the Word Online application. For more information, see [Log in to your ServiceNow instance for authoring knowledge articles in Microsoft Word](authenticate-article-word.md).

-   You must have read access to the knowledge article.
-   You must have signed in to your Office 365 account.

## Procedure

1.  From the Microsoft 365 app launcher, select the icon to launch the Microsoft Word app.

    For more information, see [Use the Office 365 app launcher](https://support.microsoft.com/en-us/office/use-the-office-365-app-launcher-0c183e98-a718-4592-9f58-4b47a4074d0b).

2.  In the New section, click **New blank document**, or open any existing Microsoft Word document.

3.  On the Home tab of the Word document, click the Knowledge icon \(![Knowledge icon](../image/word-addin.png)\).

4.  Access the article in the Knowledge Management pane of the Word document.

    -   In the Knowledge Management pane, in the **Search** box, enter the knowledge article number or description.
    -   In the Knowledge Management pane, click a knowledge base to view a list of knowledge articles within the knowledge base. All knowledge bases and associated knowledge articles for which you have contribute or read access appear in the Knowledge Management pane
5.  In the Knowledge Management pane, click the link to the knowledge article that you want to view.

    **Tip:** To go back to the previous view in the Knowledge Management pane, click the left caret icon \(![Left caret icon](../image/word-back.png)\). To go back to the landing screen, click the home icon \(![Home icon](../image/word-home.png)\).


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

Automatically generated knowledge article number.

</td></tr><tr><td>

Knowledge base

</td><td>

Knowledge base in which the knowledge article is stored. You can associate a knowledge article with one knowledge base only.

</td></tr><tr><td>

Category

</td><td>

Category for the knowledge article. This value helps users find the article within a selected category. You can select only categories available within the selected knowledge base. Articles without a category appear in the \(empty\) category.

</td></tr><tr><td>

Ownership Group

</td><td>

Ownership group for the knowledge article. An ownership group consists of a group of members and a manager who are responsible for approvals and feedback tasks. Ownership groups can publish, edit, and retire knowledge articles that they are associated with.**Note:** This field is available only if the **glide.knowman.ownership\_group.enabled** property is enabled. If no ownership group is assigned and approvals are required to publish a knowledge article, it is automatically submitted for approval to the knowledge administrator and knowledge manager. For more information, see [Ownership groups](../concept/enable-ownership-group.md).

</td></tr><tr><td>

Workflow

</td><td>

Publishing workflow state of the knowledge article, such as **Draft**, **In Review**, or **Published**. For a new article, the workflow state is set to **Draft**.

</td></tr><tr><td>

Short description

</td><td>

Title of the knowledge article. This title appears when browsing and searching for knowledge article, and at the top of the article.You can enter up to 100 characters in this field.

</td></tr><tr><td>

Document URL

</td><td>

URL of the article for accessing the online version in Microsoft Word. The URL is automatically generated for Word documents created in Microsoft SharePoint and Microsoft OneDrive with business accounts only. For other applications and account types, you must manually enter the URL in the **Document URL** field.

 **Note:** Avoid copy-pasting the browser URL, because it might not always work. Depending on the collaboration tool for your Word document use the URL generated specifically for sharing with other users.

When manually entering the URL:

-   For Microsoft SharePoint, use the URL generated by the Word Online application for specific users you want to have access to the document.
-   For Box, use the Box Shared Link. For more information, see [Creating Shared Links](https://support.box.com/hc/en-us/articles/360043697094-Creating-Shared-Links).

</td></tr><tr><td>

Version

</td><td>

Automatically generated article version number. This number is incremented when changes are made to a published article. **Note:** This field is available if the article versioning feature has been enabled.

</td></tr><tr><td>

Valid to

</td><td>

The date this knowledge article expires. Articles do not appear in search results after the **Valid to** date or if the **Valid to** date is blank. The default value of the **Valid to** field is derived from the **Article Validity** field configured for the knowledge base \(see [Create a knowledge base](create-a-knowledgebase.md)\). The **Valid to** date starts from the date the article was created until the number of days specified in the **Article Validity** field. If the **Article Validity** field is blank, the default date in the **Valid to** field for the knowledge article is set to January 1, 2100.

 An article author or editor can select whether to keep or change the default **Valid to** date.

 On the first day of each month, the application sends an email notification to a list of authorized recipients to remind them about articles that are about to expire in the next month. The recipient can then extend the **Valid to** date to continue using the article. For more information, see [Managing email notifications in Knowledge Management](../concept/email-notifications-km.md).

 **Note:** If the system date format or user preferences are set to use the `yy` year format, you might face issues when the **Valid to** date is set to the default date. Contact your system administrator or modify the user preferences to use a date format with the `yyyy` year format. For more information, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Personalize the system date format](https://www.servicenow.com/docs/access?context=t_PersonalizeTheSystemDateFormat&version=australia&pubname=australia-platform-administration&ft:locale=en-US) topics.

</td></tr><tr><td>

Scheduled publish date

</td><td>

Future date when the knowledge article will be published automatically. For more information, see [Schedule a knowledge article for publishing in Microsoft Word](schedule-article-publishing-word.md).

</td></tr></tbody>
</table>**Related topics**  


[Create a knowledge article in Microsoft Word](create-article-word.md)

[Edit a knowledge article in Microsoft Word](edit-article-word.md)

