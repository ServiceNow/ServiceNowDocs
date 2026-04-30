---
title: Check out a published article and create a new version
description: Create a new version of a knowledge article by checking out the latest published version.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use article versioning, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Check out a published article and create a new version

Create a new version of a knowledge article by checking out the latest published version.

## Before you begin

Roles required: knowledge owner, knowledge manager, or knowledge administrator

## About this task

You cannot check out a published article unless there is already a checked out version. If a version has been checked out, the **Checkout** button does not appear on the Knowledge form header and you cannot edit the knowledge article. To make changes, you must first publish the knowledge article.

When you check out an article, the default value of **Valid to** field of the article is derived from the **Article Validity** field configured for the knowledge base \(see [Create a knowledge base](create-a-knowledgebase.md)\). If the **Article Validity** field is blank, the date in the **Valid to** field date is set to January 1, 2100. An article author or editor can select whether to keep or change the default **Valid to** date.

When you check out an article, attachments from the article's base version are copied into the new article version and relative paths to these attachments are also updated.

**Note:** For article versions that were created in the previous releases, the relative paths to the attachments may not be updated. To update them, activate and run the Fix attachment links on article versions fix script.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **Published**.

2.  Select the desired article from the list.

3.  Click **Checkout** in the Knowledge form header.

    The system creates a new version of the knowledge article and displays a message to the user. The article number for the new version remains the same, the version number is increased by 0.01, and the state changes to **Draft**.

4.  Make your changes and click **Publish**.

    The new version of the article is added to the Knowledge list and to the **Article Versions** related list on the Knowledge form.


**Parent Topic:**[Use article versioning](../../../use-article-versioning_0.md)

