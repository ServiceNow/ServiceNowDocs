---
title: Schedule a knowledge article for publishing in Microsoft Word
description: Set a specific time and day for the draft version of a knowledge article created in Microsoft Word to be published automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-management/schedule-article-publishing-word.html
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Microsoft Word, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Schedule a knowledge article for publishing in Microsoft Word

Set a specific time and day for the draft version of a knowledge article created in Microsoft Word to be published automatically.

## Before you begin

-   You must have contribute access to the knowledge base that stores the knowledge article you want to schedule for publishing.
-   You must have logged in to your ServiceNow instance from the Word Online application. For more information, see [Log in to your ServiceNow instance for authoring knowledge articles in Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/authenticate-article-word.md).

-   You must have signed in to your Office 365 account.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated. For more information, see [Activate the Knowledge Management Advanced plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/activate-knowledge-advanced-plugin.md).
-   The article versioning feature is enabled. For more information, see [Article versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/article-versioning.md).
-   The Knowledge Management - Add-in for Microsoft Word is enabled. \(For more information, see [Configure Knowledge Management - Add-in for Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/configure-km-add-in-word.md).\)

## Procedure

1.  From the Microsoft 365 app launcher, select the icon to launch the Microsoft Word app.

    For more information, see [Use the Office 365 app launcher](https://support.microsoft.com/en-us/office/use-the-office-365-app-launcher-0c183e98-a718-4592-9f58-4b47a4074d0b).

2.  In the New section, click **New blank document**, or open any existing Microsoft Word document.

3.  On the Home tab of the Word document, click the Knowledge icon \(\[Omitted image "word-addin.png"\] Alt text: Knowledge icon\).

4.  In the Knowledge Management pane of the Word document, in the **Search** box, enter the knowledge article short description.

5.  Click the link to the knowledge article in the Draft state that you want to schedule for publishing.

    **Note:** The knowledge article must have been originally created using Microsoft Word.

6.  In the **Scheduled publish date** field, click the show calendar icon \[Omitted image "show-calendar.png"\] Alt text: Show calendar icon.

7.  Select any future date from the calendar.

8.  In the **Select Time** field, enter a time in the format hh:mm:ss.

9.  Click **OK**.

10. Click **Publish** to enable the publishing workflow.

    **Tip:** If you want to cancel an article's scheduled publication and move the article back to the Draft state, click **Recall**.


## Result

If approvals are disabled, the state of the knowledge article is changed to **Scheduled for Publish** and the article is automatically published on the scheduled publish date.

If approvals are enabled, the state of the knowledge article is changed to Review. If the article is approved, the state of the article is changed to Scheduled for Publish. If the article was approved after the scheduled publish date, the article is published immediately.

The version number of the knowledge article increments based on the publishing workflow. For more information, see [Knowledge article version numbers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/knowledge-article-version-numbers.md).

**Related topics**  


[Knowledge workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/r_KnowledgeWorkflows.md)

[Approve an article that is being reviewed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/approve-article-in-review.md)

