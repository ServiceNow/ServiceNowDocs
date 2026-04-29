---
title: Complete a document task
description: After the document task processing is finished, complete the task by providing input or review to train the AI.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Document Intelligence, Enable AI experiences]
---

# Complete a document task

After the document task processing is finished, complete the task by providing input or review to train the AI.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

Role required: sn\_docintel.extraction\_agent

## Procedure

1.  Do one of the following:

    -   To complete a document task for document data extraction, navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction** &gt; **Document Tasks**.
    -   To complete a document task for document classification, navigate to **All** &gt; **Document Intelligence** &gt; **Document Classification** &gt; **Document Tasks**.
2.  Review the document task list and ensure that the document task's Is Processed field is set to true.

    The following image shows the list of document tasks. If the **Is Processed** field for a task is true, that indicates that the task has been processed and is available for user input.

    If the status appears as Setup, go to the document task record and select **Process Task**.

    ![List of document tasks.](../image/doc-intel-tasks-list.png "Document tasks list")

3.  Select the processed document task.

4.  Select **Show in DocIntel**.

    The following image shows how to navigate to the Document Intelligence workspace for data extraction.

    ![Navigation to the Document Intelligence workspace](../image/docintel-show-in-docintel.png "Navigating to the DocIntel workspace")

    The Document Intelligence workspace opens in a new tab.

5.  Use the Document Intelligence workspace to review the document fields and select the appropriate recommendations.

    Learn how to [use the Document Intelligence workspace](../concept/doc-intel-workspace.md#) to extract fields.

    Learn how to [use the Document Intelligence workspace to classify documents.](../concept/use-the-docintel-workspace-to-classify.md#)

6.  Select **Submit** to complete the document task.


