---
title: Train a use case
description: Train the document classification use case with user input from completed document tasks to improve Document Intelligence recommendations over time.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up document classification use cases, Configure, Document Intelligence, Enable AI experiences]
---

# Train a use case

Train the document classification use case with user input from completed document tasks to improve Document Intelligence recommendations over time.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

-   There must be at least one reviewed document task associated with the use case to train it. Across all reviewed tasks, there must be at least two attachments for each type you defined in your use case.

    Begin by [creating a document task](upload-documents-for-extraction.md) and [completing it](extract-data-from-documents.md) using the Document Intelligence workspace.

    **Note:** You won’t be able to process the task until the use case is trained, but you can complete it by completing all the fields and submitting it.

-   Role required: sn\_docintel.manager

## About this task

Document classification use cases don’t begin with pre-trained AI models, so it’s important to train the models with user input from completed document tasks.

**Note:** To reduce server load and minimize performance issues, the default limit for training a use case is once every 30 days.

## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Classification** &gt; **Use Cases**.

2.  Select a use case in the list.

3.  Select **Train Use Case**.

    DocIntel uses the extracted values from the document tasks in a Done status to train the model.

    ![Completed document tasks used to train the use case](../image/docintel-train-dc-use-case.png)


## Result

The train use case job begins. This job may take several hours to complete.

## Test a use case

The following example shows how to train a document classification use case to process identification documents.

1.  You start by creating a document classification use case called Identification. You create a field for each type of category you want to apply to your identification documents.

    In this case, there are fields for a **Drivers license**, **Passport**, **Military ID**, and **ID card**.

    ![Document classification use case with fields defined for each category.](../image/docintel-train-example-1.png)

2.  Then you create document tasks containing attached examples of the categories you defined in the fields.

    **Tip:** You should submit at least 50 documents to adequately train the AI model.

    ![Document classification use case showing document tasks created to train the model.](../image/docintel-train-example-2.png)

3.  You complete the tasks by opening the documents in Document Intelligence workspace, completing all the fields, and submitting them.

    1.  Select each document task to open it.
    2.  Select **Show in DocIntel**.

        ![Show in DocIntel button on the document task screen.](../image/docintel-train-example-3b.png)

    3.  Fill in the category.
    4.  Select **Submit**.

        ![Document Intelligence workspace showing the license document with a review panel.](../image/docintel-train-example-3d.png)

        The document tasks will be in a Done state and so become available to train the model.

4.  You go back to the Identification use case screen and select **Train Use Case**.

    ![Train Use Case button on the use case screen.](../image/docintel-train-example-4.png)


