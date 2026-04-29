---
title: Create a document classification use case
description: Create a use case record to begin defining the classes or categories that you want to apply to a type of document or pages within the document.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up document classification use cases, Configure, Document Intelligence, Enable AI experiences]
---

# Create a document classification use case

Create a use case record to begin defining the classes or categories that you want to apply to a type of document or pages within the document.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

Role required: sn\_docintel.manager

## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Classification** &gt; **Use Cases**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_hr4_fny_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

The name for the use case as it appears in the Document Intelligence workspace.

</td></tr><tr><td>

Document Type

</td><td>

Type of document to be processed for the use case.

</td></tr><tr><td>

Document Config

</td><td>

Configuration of the document to be processed for the use case.

</td></tr><tr><td>

Autofill Threshold

</td><td>

DocIntel only auto-fills the classes \(fields\) if the confidence score of the top recommendation is at or above the percentage you define.

 Fields with a confidence score lower than the threshold are left empty in the Document Intelligence workspace, and the recommendation mode is available to extract these fields.

 This field is available only if the Auto-fill mode is enabled.

</td></tr><tr><td>

Fully Automated Threshold

</td><td>

Confidence score threshold for document classifications, which enables a document task to be fully automated in the Fully Automated \(Straight Through Processing\) mode.

</td></tr><tr><td>

Warning Threshold

</td><td>

DocIntel shows a warning for empty fields and auto-filled fields with a confidence score at or below the percentage that you define.

 This field is available only if the Auto-fill mode is enabled.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After creating a use case, finish setting it up by adding fields to [create document classes](create-document-classes.md). Then, [train the use case](train-a-use-case.md).

