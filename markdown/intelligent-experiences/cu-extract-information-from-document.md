---
title: Extract information from documents
description: The Extract Information from documents skill \(Information Extraction skill\) uses generative AI to automatically extract content from documents and images, and to respond to questions about that content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cu-extract-information-from-document.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Explore, Content Understanding, Enable AI experiences]
---

# Extract information from documents

The Extract Information from documents skill \(Information Extraction skill\) uses generative AI to automatically extract content from documents and images, and to respond to questions about that content.

With the Information Extraction skill, you can extract specific fields, tabular data, and answers about documents or images. You can then integrate the extracted data into your workflows. The skill transforms unstructured files, such as invoices, purchase orders, and contracts, into structured data that populates ServiceNow records, eliminating the need for manual data entry.

You configure this skill in the AI Admin Hub. You can define one or more use cases that specify what to extract from a particular type of document. For example, a use case for purchase order forms can extract the form date and number, capture an itemized list with prices in a table, and answer questions such as whether any items include a specific term in the description.

**Note:** The Extract information from documents skill uses generative AI to process documents. Results may be inaccurate or incomplete. Review extracted data before using it in production workflows.

## Define the information to extract

Within a single use case, you can define any combination of the following:

-   Specific fields to extract, such as a date or a document number.
-   A table structure with multiple columns to capture repeating line items.
-   Questions for generative AI to answer based on the text and images in a document.

## Benefits

The Extract information from documents skill provides the following benefits:

-   Populates ServiceNow records with data extracted from documents.
-   Reads both text and images in a document.
-   Runs automatically or routes results to a reviewer for validation, depending on the automation mode.

## Scenarios

The Extract information from documents skill supports the following scenarios:

-   **Field population**

    Extracts values from an uploaded document and writes them to the fields of a record.

-   **Assisted review**

    Presents predicted values to a reviewer for validation before saving them to a record.


**Related topics**  


[Use cases in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-use-cases.md)

[Automation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/automation-modes.md)

