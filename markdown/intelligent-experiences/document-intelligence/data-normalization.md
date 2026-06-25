---
title: Data normalization
description: Certain types of data extracted from documents are converted into a standard format so that they appear the same across all fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/document-intelligence/data-normalization.html
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Document Intelligence, Enable AI experiences]
---

# Data normalization

Certain types of data extracted from documents are converted into a standard format so that they appear the same across all fields.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/docintel-nowassist-landing.md).

This process increases the usefulness of the data by enabling it to be grouped and analyzed more easily. It also supports integration with other applications on the ServiceNow AI Platform.

## Field types

The following field types are converted to support data normalization:

<table id="table_qbs_lsl_rxb"><thead><tr><th>

Field type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date

</td><td>

Standard date format. For example, YYYY-MM-DD.

</td></tr><tr><td>

Reference field

</td><td>

A field that uses a field in another table as a standard. DocIntel matches the extracted data to the standard.

 For example, a use case has a reference field called **Vendor** that points to the Name column in the Company table as the reference. When processing a document task, DocIntel extracts “Degas Dairy Products, Inc” from the document and fills the **Vendor** field with that value. DocIntel compares the value to the company names in the reference table and finds “Degas Dairy Products, Inc” as a match. In the document task, “Degas Dairy Products, Inc” is matched to “Degas Dairy Products, Inc” in the reference.

 \[Omitted image "mmasset0020489-data-normalization-landing.png"\] Alt text: Reference field flow.

</td></tr><tr><td>

Integer

</td><td>

Whole number. For example, 12.

</td></tr><tr><td>

Decimal

</td><td>

Number with up to two decimal places. For example, 12.5 or 12.55.

</td></tr><tr><td>

Floating point number

</td><td>

Number with up to seven decimal places. For example, 12.0 to 12.0000000.

</td></tr></tbody>
</table>To set the field type, see [Create a field for data extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/manage-keys.md).

## Display

A completed data extraction field shows the converted value next to it.

\[Omitted image "docintel-normalization-example2.png"\] Alt text: Data extraction integer field and its converted value field. \[Omitted image "docintel-normalization-example.png"\] Alt text: Data extraction date field and its converted value field.

You can adjust the converted date value by selecting **Edit**.

**Note:** In some cases, the data extracted from the document may not be in a valid format to be converted. For example, if DocIntel read the letter O instead of a number 0 in a date field \(11.12.2o23\), then it would not be converted. In this case, edit the field to the correct format.

## Ambiguous data

If there is data in a document that can be understood in more than one way, DocIntel interprets that value based on the default selected for it in the use case configuration. DocIntel must interpret an ambiguous value in order to accurately convert it to the normalized format.

For example, a use case has a **Date** field, and `Month first` is selected as the default order to interpret ambiguous dates. When a document containing the date 1/2/2024 is processed for the use case, DocIntel interprets that date as January 2, not February 1, when it extracts that value and converts it.

In such cases, the user completing a document task may need to confirm or correct the conversion of ambiguous values. Depending on the field’s configuration in the use case, automated document processing may be interrupted to ensure the conversion is accurate.

**Parent Topic:**[Document Intelligence references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence]()

[Confidence scores]()

[Data extraction modes]()

[Document field statuses]()

[Document Intelligence forms]()

[Document Intelligence properties]()

[Document Intelligence roles]()

[Document Intelligence terminology]()

[Document task statuses]()

[Domain separation and Document Intelligence]()

[Languages supported by Document Intelligence]()

[Limitations in Document Intelligence]()

