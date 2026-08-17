---
title: Predictions in Information Extraction skill
description: A prediction is the value that the Information Extraction skill infers for each field, table, or question in a use case. Predictions drive automation decisions and can be applied automatically or reviewed by a person, depending on the use case configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/predictions.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Information Extraction skill, Explore, Content Understanding, Enable AI experiences]
---

# Predictions in Information Extraction skill

A prediction is the value that the Information Extraction skill infers for each field, table, or question in a use case. Predictions drive automation decisions and can be applied automatically or reviewed by a person, depending on the use case configuration.

## How predictions are generated

A prediction is the value that the Information Extraction skill infers for a field, table, or question in a specific use case. When you submit a document for processing, the skill processes its content and generates a prediction for each field, table cell, and question set in that use case.

A prediction shows what the skill identifies as the correct value based on the content in the document. Whether a prediction is applied without review or reviewed by a person depends on the automation setting for the use case. To understand how automation settings control whether predictions are applied automatically or sent for review, see [Automation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/automation-modes.md).

## Prediction sources

|Use case element|Prediction|
|----------------|----------|
|Field|A single value recognized in the document, such as an invoice number or a date.|
|Table|Row-level values extracted from a tabular structure in the document, such as line items.|
|Question|An answer generated from the document content in response to a configured question.|

**Related topics**  


[Use cases in Information Extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-use-cases.md)

