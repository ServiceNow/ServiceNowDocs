---
title: Content extraction methods
description: The Extract information from documents skill \(Information Extraction skill\) supports three extraction methods—field, table, and Q&amp;A—each suited for different types of document data. Understanding which method to use helps you capture and store the right information in ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/content-extraction-methods.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Information Extraction skill, Explore, Content Understanding, Enable AI experiences]
---

# Content extraction methods

The Extract information from documents skill \(Information Extraction skill\) supports three extraction methods—field, table, and Q&amp;A—each suited for different types of document data. Understanding which method to use helps you capture and store the right information in ServiceNow.

The Information Extraction skill uses AI-assisted parsing to extract data from documents \(invoices, purchase orders, and contracts\) and then populates records in ServiceNow. Select a method or combination of methods that matches the type of information you want to capture and store in ServiceNow tables.

## Field extraction

Field extraction captures specific, isolated data points from a document—values that appear exactly once—and maps each to a single field on a ServiceNow record.

Use field extraction for data such as:

-   Invoice numbers, purchase order numbers, or document identifiers
-   Vendor or customer names
-   Dates, such as an invoice date, due date, or contract start date
-   Monetary totals or tax amounts
-   Addresses or other contact details

You can bundle related single fields into a logical group. For example, a Billing Address group can capture Street, City, State, and ZIP from the same region of a document.

## Table extraction

Table extraction captures dynamic, multi-row data from documents where the number of entries varies between documents, such as invoice line items or expense report details. A table acts as a two-dimensional grid of rows and columns that captures a list of related records.

Use table extraction for data such as:

-   Invoice or purchase order line items \(quantity, description, unit price, total\)
-   Expense report breakdowns
-   Parts lists or bills of materials
-   Multi-page flight itineraries or timesheet entries

## Q&amp;A extraction

Q&amp;A extraction uses generative AI to answer open-ended, natural language questions about the contents of a document. It is suited for unstructured text that does not fit neatly into a predefined field or table schema. The extraction processes meaning rather than matching a fixed pattern.

**Warning:** Q&amp;A extraction uses generative AI and may produce inaccurate or incomplete results. Review all AI-generated output before using it to populate records.

Use Q&amp;A extraction for questions such as:

-   The reason for termination
-   Special shipping or delivery terms
-   The designated project manager
-   Narrative clauses or conditional language from contracts

You can also use Q&amp;A extraction to categorize documents.

## Selecting an extraction method

Use the following guidance to choose the appropriate extraction method.

|Extraction method|When to use|Example|
|-----------------|-----------|-------|
|Field extraction|Use when the data point appears once and has a well-defined type.|A number, date, or name.|
|Table extraction|Use when the document contains a list or grid of repeating items where the row count is unknown or varies across documents.|Line items in an invoice or purchase order.|
|Q&amp;A extraction|Use when the information is embedded in narrative text and requires interpretation rather than pattern matching.|An answer based on contract terms or policy text.|

You can combine multiple methods within a single use case to handle all of the data types present in a document.

**Related topics**  


[Use cases for the Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-use-cases.md)

