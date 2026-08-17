---
title: Data normalization
description: Data extracted from documents is converted into a standard format. This ensures that values appear consistently across all fields, making the data easier to group, analyze, and integrate with other applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/data-normalization.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Content Understanding, Enable AI experiences]
---

# Data normalization

Data extracted from documents is converted into a standard format. This ensures that values appear consistently across all fields, making the data easier to group, analyze, and integrate with other applications.

Data normalization supports integration with other applications on the ServiceNow AI Platform.

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

A field that uses a field in another table as a standard. Content Understanding matches the extracted data to the standard. For example, a use case has a reference field called **Vendor** that points to the Name column in the Company table as the reference. When processing a document task, Content Understanding extracts "Degas Dairy Products, Inc" from the document and fills the **Vendor** field with that value. Content Understanding compares the value to the company names in the reference table and finds "Degas Dairy Products, Inc" as a match. In the document task, "Degas Dairy Products, Inc" is matched to "Degas Dairy Products, Inc" in the reference.

 \[Omitted image "cu-data-normalization.png"\] Alt text: Reference field type showing extracted vendor value matched to a company name in the reference table.

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
</table>## Display

A completed data extraction field shows the converted value next to it.

\[Omitted image "cu-data-normalization-example2.png"\] Alt text: Data extraction integer field and its converted value field.

\[Omitted image "cu-data-normalization-example1.png"\] Alt text: Data extraction date field and its converted value field.

You can adjust the converted date value by selecting **Edit**.

**Note:** In some cases, the data extracted from the document may not be in a valid format to be converted. For example, if Content Understanding read the letter O instead of a number 0 in a date field \(11.12.2o23\), then it would not be converted. In this case, edit the field to the correct format.

## Ambiguous data

When a document contains ambiguous data, Content Understanding uses the default setting in the use case configuration to determine the correct interpretation. The value requires clarification before it can be converted into a normalized format.

For example, consider a use case with a Date field. The default interpretation of ambiguous dates is set to "Month first." A document containing the date 1/2/2024 is interpreted as January 2, 2024, rather than February 1, 2024.

In such cases, you may need to confirm or correct the interpretation of ambiguous dates. Depending on the configuration of the field within the use case, automated document processing may pause so you can verify that the conversion is accurate.

**Parent Topic:**[Content Understanding Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-reference.md)

