---
title: Document Intelligence terminology
description: Before getting started with Document Intelligence \(DocIntel\), it's important to understand some key concepts used in the application.
locale: en-US
release: xanadu
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Document Intelligence references, Document Intelligence, Enable AI experiences]
---

# Document Intelligence terminology

Before getting started with Document Intelligence \(DocIntel\), it's important to understand some key concepts used in the application.

## Updated terminology

As of Document Intelligence v2.3, DocIntel features include updated terminology.

|New term|Old term|
|--------|--------|
|Document task|Task, extraction task|
|Field|Key, attribute|
|Field group|Key group|
|Field value|Extracted value|
|Integration|Integration setup|
|Recommendation|Candidate, suggestion|
|Fully automated|Straight through processing|
|Use case|Task definition|

**Parent Topic:**[Document Intelligence references](../reference/docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence](../reference/installed-with-document-intelligence.md)

[Confidence scores](docintel-confidence-scores.md)

[Data extraction modes](../reference/data-extraction-modes.md)

[Data normalization](data-normalization.md)

[Document field statuses](../reference/docintel-field-statuses.md)

[Document Intelligence forms](../reference/document-intelligence-forms.md)

[Document Intelligence properties](../reference/document-intelligence-properties.md)

[Document Intelligence roles](../reference/document-intelligence-user-roles.md#)

[Document task statuses](../reference/docintel-task-statuses.md)

[Domain separation and Document Intelligence](../reference/domain-separation-and-doc-intel.md)

[Languages supported by Document Intelligence](languages-supported-by-document-intelligence.md)

[Limitations in Document Intelligence](../reference/hard-limits-in-doc-intel.md)

## classification

In Document Intelligence, the process of categorizing documents and document pages based on their type.

## confidence score

A numerical value assigned to a recommendation by Document Intelligence indicating its certainty about the extracted information. The higher the score, the more reliable the recommendation.

## document class

A field used to apply a category or label to a document and to pages within a document in Document Intelligence.

For example, for an identity document use case, the classes might be passport, driver’s license, birth certificate, and the like.

## document task

A document processing activity in Document Intelligence. It includes the information that you want to extract from the document or documents.

## extraction

In Document Intelligence, the process of identifying relevant information in a document and using it as a basis for the AI to recommend a field value.

## field

A single piece of information to extract from a document in Document Intelligence. For example, the date on a document.

Fields are sometimes called keys or attributes.

## field group

A group of fields that belong together in Document Intelligence. Field groups are used to extract information from lists and tables.

For example, a group named "item" contains description, quantity, and unit price fields from a purchase order.

## field value

The final output of the Document Intelligence application. The output contains the values for the specified fields that were extracted for a given document task.

## recommendation

In Document Intelligence, a bit of text found on a document. The recommendation includes information about its location in the document, meaning the page of a document and the particular location on that page.

The recommendations that the AI provides are sorted based on how likely the AI believes a given recommendation to be the correct value for the current field.

## unstructured document

A document that mainly contains free-form textual information and does not conform to a specific format or structure.

## use case

A use case is a set of configurations used to define the structure of a type of document that you want to process. It’s made up of the use case record and its related fields, field groups, integrations, flows, and all the related machine learning \(ML\) models. The use case also includes the mode for how the extraction should occur.

