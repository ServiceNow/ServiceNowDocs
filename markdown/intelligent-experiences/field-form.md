---
title: Field form fields
description: The field form defines the information to extract from a document, including the field name, type, and target table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/field-form.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Forms, Reference, Content Understanding, Enable AI experiences]
---

# Field form fields

The field form defines the information to extract from a document, including the field name, type, and target table.

The following fields are available when configuring a use case for document extraction.

\[Omitted image "cu-field-form.png"\] Alt text: Field form showing configuration options for document extraction, including field name, details, field type, and target table.

<table id="table_slt_m5b_zjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Name of the field to extract. State the information to extract clearly and concisely. For example: `Order number`

</td></tr><tr><td>

Details

</td><td>

Description of the information to extract. The field name and description together determine what text the system extracts from the document. Include relevant context or additional details to identify the correct information. This may include keywords. For example, `The contract number or the number of the reference contract`.

 Include examples of the information to extract. For example, `AGR-2023-0042`, `CON2039739`, or `BV-22122KEY`.

 Example field configuration:

 ```
Field name: Currency
Details: The currency in which the contract is denominated. Only valid
for Order Forms. Otherwise, leave it empty (''). If the currency symbol
is '$', answer 'USD'. Examples: 'USD', 'EUROS', 'GBP', etc.
```

 **Tip:** Select the **Field assistance** tab for additional guidance on forming an effective field.

</td></tr><tr><td>

Field Type

</td><td>

Type of field, such as text or date. For more information, see [Field types in Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/field-types.md). Some field types convert the extracted value into a standard format. For more information, see [Data normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/data-normalization.md).

</td></tr><tr><td>

Target table

</td><td>

Table that stores the document processing results for this use case.

</td></tr><tr><td>

Target field

</td><td>

Field on the target table to align with. **Note:** The use case must include a selected target table before this field is available.

</td></tr><tr><td>

This single field is required for extraction

</td><td>

Marks the field as required. Required fields must have a value and can't be left empty or cleared.

</td></tr><tr><td>

Create multiple single fields

</td><td>

Keeps the form open after saving. Select this option when adding more than one field to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Content Understanding forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-forms.md)

