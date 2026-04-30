---
title: Set up document extraction use cases
description: In Document Intelligence, a use case is used to define the structure of a type of document you want to process. It's made up of the use case record and its related fields, field groups, integrations, flows, and all the related machine learning \(ML\) models.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Set up document extraction use cases

In Document Intelligence, a use case is used to define the structure of a type of document you want to process. It's made up of the use case record and its related fields, field groups, integrations, flows, and all the related machine learning \(ML\) models.

## Overview of document extraction use cases

In a document extraction use case, you define the information that you want the AI to detect in a document. Do this by specifying the type of document to process, the fields to detect, and the location where document processing results are to be stored.

For example, if you want to process invoice documents, you may want an “Invoice” use case. This use case could have fields for date, invoice number, item, and so on, to define which information needs to be extracted from the document.

![Document extraction use case showing fields and field groups.](../image/docintel-ext-use-case-example.png)

After you've defined a document extraction use case, agents can begin processing documents for it in document tasks.

**Note:** Use cases for Now Assist in Document Intelligence skills have a separate setup process. For more information, see [Configuring Now Assist in Document Intelligence](docintel-configuring-now-assist.md).

## Workflow

Set up a document extraction use case in the following steps.

1.  [Create a use case](../task/create-tasks.md).

    Define the name, target table, and language for the use case.

2.  [Create a field for data extraction](../task/manage-keys.md).

    Define the fields that the AI will learn to detect and extract values from.

    Define any groupings of fields to help extract and organize data gathered from tables or information patterns, like check box lists.

3.  [Configure data extraction modes](../task/configure-data-extraction-modes.md).

    Define how fields should be extracted from documents in a document task.

4.  [Set up integrations](../task/configure-integration-setup.md).

    Configure an integration to trigger document task processing or value extraction for workflows with other applications.


As agents work on document tasks to extract field values from individual documents, the AI will learn from the feedback and continue to improve.

