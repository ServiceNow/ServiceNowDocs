---
title: Create a document extraction use case
description: Create a use case record to define a document you want to process in Document Intelligence. For example, invoices or driving licenses.
locale: en-US
release: zurich
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-01-27"
reading_time_minutes: 1
breadcrumb: [Set up document extraction use cases, Configure, Document Intelligence, Enable AI experiences]
---

# Create a document extraction use case

Create a use case record to define a document you want to process in Document Intelligence. For example, invoices or driving licenses.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

Role required: sn\_docintel.manager

## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

2.  Select **New use case**.

3.  Enter a name for the use case.

4.  Select a target table to store the document processing results for this use case.

5.  Change the language model used to support document extraction.

    For more information, see [Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md).

6.  Select **Save**.


## What to do next

After creating a use case, finish setting it up by adding [fields](manage-keys.md) and configuring the [data extraction modes](configure-data-extraction-modes.md).

