---
title: Create knowledge articles using Now Assist and Box
description: Use Box to create knowledge articles from content stored in an external Box account. When you initiate article creation and select Box as the source, Now Assist searches the connected Box account for files relevant to the prompt, then generates an article based on the results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/kc-create-article-with-Box.html
release: australia
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 2
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create knowledge articles using Now Assist and Box

Use Box to create knowledge articles from content stored in an external Box account. When you initiate article creation and select Box as the source, Now Assist searches the connected Box account for files relevant to the prompt, then generates an article based on the results.

## Before you begin

The prerequisites for using Box to create knowledge articles in the Knowledge Center are:

-   Verify that your administrator has configured Box for your instance.
-   To create articles using Box, you must have a Box user account.

Role required: agent

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** and start the article creation process.

    Select a template and complete any required initial setup for the new article. For more information see, [Generate and edit articles using the article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-edit-knowledge-article.md).

2.  In the article editor section, in the **Source** drop-down under **Integrations**, select **Box**.

    **Note:** If **Box** doesn't appear in the **Source** drop-down, contact your administrator.

3.  In the Now Assist context menu, enter a prompt that describes the article you want to create.

    For example, enter `Create an article about password reset`.

4.  Submit the prompt.

    The system connects to Box, analyzes the request, and searches for relevant files. One of the following outcomes occurs:

    -   **Files found**: Now Assist generates an article using the content from the matching Box files. The generated article includes a short description and article body.
    -   **No files found**: A message indicates that no relevant information was found. The system creates an article based on the prompt alone, without Box content.
    -   **User not authorized**: An error message states `Unable to retrieve Box identity for this account`. This occurs when you do not have a Box account. Contact your administrator to set up a Box account for you.
5.  Review the article for accuracy and completeness, and make any necessary edits before publishing.


**Parent Topic:**[Using Now Assist in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/using-now-assist-in-km.md)

**Related topics**  


[Integrate Box in Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-configuring-box-integration.md)

