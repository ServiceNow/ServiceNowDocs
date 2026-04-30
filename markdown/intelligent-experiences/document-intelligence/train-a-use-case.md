---
title: Train a use case
description: Train the document classification use case with user input from completed document tasks to improve Document Intelligence recommendations over time.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up document classification use cases, Configuring Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Train a use case

Train the document classification use case with user input from completed document tasks to improve Document Intelligence recommendations over time.

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

