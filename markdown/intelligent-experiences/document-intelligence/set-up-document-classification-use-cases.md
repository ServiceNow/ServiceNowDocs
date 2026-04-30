---
title: Set up document classification use cases
description: A document classification use case is a set of categories used to classify your documents and their individual pages. It’s made up of the use case record and its related fields \(classes\), and all related machine learning \(ML\) models.
locale: en-US
release: zurich
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2026-01-27"
reading_time_minutes: 2
breadcrumb: [Configure, Document Intelligence, Enable AI experiences]
---

# Set up document classification use cases

A document classification use case is a set of categories used to classify your documents and their individual pages. It’s made up of the use case record and its related fields \(classes\), and all related machine learning \(ML\) models.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](docintel-nowassist-landing.md).

## Overview of document classification use cases

In a document classification use case, you define the classes or categories that you want the AI to detect and apply to a document. Do this by specifying the type of document to process, the classes to apply, and the location where document processing results are stored.

For example, if you want to process identification documents, you may want an “Identity Documents” use case. Then, add classes for passports, driver’s licenses, military IDs, and so on, to label which type of documents are being processed.

After you’ve defined a document classification use case, agents can begin processing documents for it in document tasks.

## Workflow

Set up a document classification use case in the following steps.

1.  [Create a use case](../task/create-a-document-classification-use-case.md).

    Define the name and properties for the use case.

2.  [Create document classes using fields](../task/create-document-classes.md).

    Define the classes or categories that the AI will learn to detect and apply to documents.

3.  [Train the use case](../task/train-a-use-case.md).

    Initiate a training job to provide user inputs from completed document tasks to the AI for continuous improvement.


As agents work on document tasks to classify documents and their individual pages, the AI learns from the feedback and continues to improve.

