---
title: Use cases in Now Assist in Document Intelligence
description: In Now Assist in Document Intelligence, a use case is used to define the information you want generative AI to detect from a document.
locale: en-US
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Explore, Now Assist in Document Intelligence, Enable AI experiences]
---

# Use cases in Now Assist in Document Intelligence

In Now Assist in Document Intelligence, a use case is used to define the information you want generative AI to detect from a document.

## Use cases for Now Assist in Document Intelligence skills

Now Assist in Document Intelligence supports use cases for the following skills:

-   **Extract information from documents**

    In an extract information use case, define the information you want Now Assist to extract from a document in the form of fields, tables, and questions.

    You can define a specific field to extract, a table structure with multiple columns, or a question you want generative AI to answer based on the text in a document.

    For example, if you need to process information from purchase order forms, you may want a use case with fields to extract the form date and number, a table to extract the itemized list with prices, and questions such as “Does the order include any items with ‘gift card’ in the description".


## Use case structure

A use case is made up of the use case record and its related fields, tables, and questions as well as anyintegrations, and flows.

Now Assist in Document Intelligence uses fields to identify the specific information in documents to consider when making predictions.Tables are used to extract information in the cells that appear under table columns. Questions are used to produce an answer based on analysis of the text in a document.

## Use case setup

Use the Now Assist Features interface to set up use cases for Now Assist in Document Intelligence skills. Use cases for the Document Intelligence application have a separate setup process. For more information, see [Configuring Document Intelligence](doc-intel-administration.md).

Use case setup involves defining the use case name and details, defining the fields, tables, and questions, setting up integrations and flows, and testing the use case.

For more information, see [Set up a use case for Now Assist in Document Intelligence](../task/set-up-use-case-for-now-assist-document-intelligence.md).

**Tip:** To save time when you need to create a new use case that shares a similar structure to another, make a copy of the existing use case and edit the details of the copy. For more information, see [Make a copy of a use case in Now Assist in Document Intelligence](../task/make-copy-of-now-assist-document-intelligence-use-case.md).

Once you completed the setup of a use case, agents can begin processing documents for it.

