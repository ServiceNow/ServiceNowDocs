---
title: Use cases in Information Extraction skill
description: Use cases in the Information Extraction skill define what documents to process and what information to extract, so generative AI can accurately retrieve structured data from unstructured documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cu-use-cases.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [use case, information extraction, generative AI]
breadcrumb: [Information Extraction skill, Explore, Content Understanding, Enable AI experiences]
---

# Use cases in Information Extraction skill

Use cases in the Information Extraction skill define what documents to process and what information to extract, so generative AI can accurately retrieve structured data from unstructured documents.

A use case defines the document type to process and the specific information generative AI extracts from it. A single use case applies to all documents that share a common set of values to extract, even when those documents aren't in the same format.

## Common use cases

-   **Invoice processing**

    Extract line items, invoice numbers, totals, and vendor details from PDFs or scanned vendor invoices. For an example implementation, see [ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-apo.md).

-   **HR onboarding**

    Extract fields such as national IDs, tax declarations, and emergency contacts from employee documents.

-   **Field service**

    Extract data from purchase orders, equipment maintenance sheets, or work orders to pre-populate service tasks.


## Use case structure

A use case consists of the use case record and its related fields, tables, questions, any integrations, and workflows.

-   Fields identify specific information within documents relevant to predictions.
-   Tables extract information from cells within table columns.
-   Questions generate answers based on an analysis of the text and images within a document.

## Use case setup

Use case setup includes defining the use case name and details, specifying fields, tables, and questions, configuring integrations and flows, and testing the use case.

The following guidelines help improve extraction precision and relevance.

-   **Identify your requirements**

    Clearly describe the specific field, table, or answer you want to extract.

-   **Use field prompts**

    Use the relevant field prompts and descriptions customized for your use case. This guides the extraction process.

-   **Follow the recommended format**

    To improve accuracy, follow the format provided in the on-screen **Field Assistance** tab. This produces consistent results.

-   **Adjust descriptions**

    Field descriptions may change during test executions. Reviewing changes helps improve your extraction results.


Follow

## Use case–based extraction flow

-   **Schema definition**

    You create a use case by defining a schema — a set of specific fields, tables, and questions that you need from that document.

-   **Intelligent extraction**

    Rather than using rigid templates, generative AI uses the use case to identify the document's structure and extract the target information. Results may vary and human review is recommended before using extracted data in automated workflows.

-   **Workflow automation**

    After generative AI extracts the data, it populates the required fields in your ServiceNow® workflows, such as ITSM, Field Service Management for Telecommunication, or ServiceNow Otto for HRSD.

    **Note:** When full automation mode is enabled, fulfiller verification is skipped.


**Related topics**  


[Predictions in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictions.md)

[Content Understanding personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/personas.md)

[Automation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/automation-modes.md)

[Set up a use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-use-case.md)

