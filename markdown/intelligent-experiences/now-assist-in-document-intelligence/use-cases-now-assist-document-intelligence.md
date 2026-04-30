---
title: Use cases in Now Assist in Document Intelligence
description: In Now Assist in Document Intelligence, a use case is used to define the information you want generative AI to detect from a document.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Exploring Now Assist in Document Intelligence, Now Assist in Document Intelligence, Enable AI experiences]
---

# Use cases in Now Assist in Document Intelligence

In Now Assist in Document Intelligence, a use case is used to define the information you want generative AI to detect from a document.

## Use cases for Now Assist in Document Intelligence skills

Now Assist in Document Intelligence supports use cases for the following skills:

-   **Document extraction**

    In a document extraction use case, define the text you want Now Assist to extract from a document.

    For example, if you need to process employee documents, you may want an “Emergency Contact Information Form” use case with fields for employee name, department, emergency contact name, and so on, to define which information needs to be extracted from the document.

-   **Document Q&amp;A \(question and answer\)**

    In a document Q&amp;A use case, define the questions you want generative AI to answer based on the text in a document.

    For example, if you need information from service agreements, you may want a “Service agreements” use case with questions such as “What parties are involved” or “Is the agreement term within 3 to 5 years”.


## Use case structure

A use case is made up of the use case record and its related fields, field groups, integrations, and flows.

Now Assist in Document Intelligence uses fields to identify the information in documents to consider when making predictions. Fields can be grouped together to form structured sections or help extract data from tables and other logical groupings of fields.

## Use case setup

Use the Now Assist Features interface to set up use cases for Now Assist in Document Intelligence skills. Use cases for the Document Intelligence application have a separate setup process. For more information, see [Configuring Document Intelligence](doc-intel-administration.md).

Use case setup involves defining the use case name and target table, selecting the LLM for the predictions,defining the fields, setting up integrations and flows, and testing the use case.

For more information, see [Set up a use case for Now Assist in Document Intelligence](../task/set-up-use-case-for-now-assist-document-intelligence.md).

**Tip:** To save time when you need to create a new use case that shares a similar structure to another, make a copy of the existing use case and edit the details of the copy. For more information, see [Make a copy of a use case in Now Assist in Document Intelligence](../task/make-copy-of-now-assist-document-intelligence-use-case.md).

Once you completed the setup of a use case, agents can begin processing documents for it.

