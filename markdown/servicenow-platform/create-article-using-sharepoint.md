---
title: Create knowledge articles using AI and Microsoft SharePoint
description: Create knowledge articles from content stored in a SharePoint account. When you select SharePoint as the source, AI searches the connected SharePoint account for files relevant to the prompt, and generates an article based on the results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/create-article-using-sharepoint.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [SharePoint, external content connection, Knowledge Center]
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create knowledge articles using AI and Microsoft SharePoint

Create knowledge articles from content stored in a SharePoint account. When you select SharePoint as the source, AI searches the connected SharePoint account for files relevant to the prompt, and generates an article based on the results.

## Before you begin

The prerequisites for using SharePoint to create knowledge articles in the Knowledge Center are:

-   Verify that your administrator has configured Microsoft SharePoint for your instance by following the steps in [Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/microsoft-sharepoint-online-external-content-connector.md).
-   Your administrator must set up the SharePoint External Connector. This includes plugin activation, admin setup on the SharePoint side, credential setup on the ServiceNow side, the crawling schedule, and user mapping.
-   To create articles using SharePoint, you must have a Microsoft SharePoint user account.

Role required: knowledge admin, knowledge manager, or knowledge

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** and start the article creation process.

    Select a template and complete any required initial setup for the new article. For more information, see [Generate and edit articles using the article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/kc-edit-knowledge-article.md).

2.  In the article editor section, in the **Source** drop-down under **Integrations**, select **SharePoint**.

    **Note:** If **SharePoint** doesn't appear in the **Source** drop-down, contact your administrator.

3.  In the AI context menu, enter a prompt that describes the article you want to create.

    For example, enter `Create an article about password reset`.

4.  Submit the prompt.

    The system connects to Microsoft SharePoint, analyzes the request, and searches for relevant files. One of the following outcomes occurs:

    -   **Files found**: AI generates an article using the content from the matching Microsoft SharePoint files. The generated article includes a short description and article body.
    -   **No files found**: A message indicates that no relevant information was found. The system creates an article based on the prompt alone, without Microsoft SharePoint content.
    -   **User not authorized**: An error message states `Unable to retrieve SharePoint identity for this account`. This occurs when you do not have a Microsoft SharePoint account. Contact your administrator to set up a Microsoft SharePoint account for you.
5.  Review the article for accuracy and completeness, and make any necessary edits before publishing.


