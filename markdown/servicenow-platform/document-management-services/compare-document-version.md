---
title: Compare document versions
description: Document version comparison enables you to view differences between two versions of a document, highlighting changes such as added, removed, or modified content.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document versions, Document repository, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Compare document versions

Document version comparison enables you to view differences between two versions of a document, highlighting changes such as added, removed, or modified content.

## Before you begin

Role required: admin

## About this task

In the navigation filter, enter `sys_property.list` and ensure **glide.documents.compare.enabled** property is set to **true**.

## Procedure

1.  [Create an experience for UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-experience.md), if an experience is already created, go to Step 5.

2.  [Create a page from a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/reuse-page-definitions.md).

3.  Go to created page template and select **Use template**.

4.  Go to home page, select **Workspaces**.

5.  Select the workspace and the record.

6.  Select the **Documents** tab, select the document from the list of documents.

7.  Select the **Versions** tab.

8.  Select the **Compare** button.

9.  Select the **Source version** and the **Target version** you want to compare and select **Compare**.

    **Note:** Both the versions must be in the same format. Only .doc and .docx formats are supported.

10. A new **Compare** tab opens up showing the comparison summary with Total changes, Edited, Deleted, and Format changes.

11. You can review the changes and have the option to hide the redlines on the side by selecting **hide redlines**.

12. To download the document, select **Download redlined document** showing the changes.


**Parent Topic:**[Document versions](../concept/document-mgt-versions.md)

