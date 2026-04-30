---
title: Field form for document extraction setup
description: The Field form enables you to define a single field for extraction.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Now Assist in Document Intelligence forms, Now Assist in Document Intelligence reference, Now Assist in Document Intelligence, Enable AI experiences]
---

# Field form for document extraction setup

The Field form enables you to define a single field for extraction.

The Field form includes the following fields.

<table id="table_mzd_zcv_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

The name for the field as it appears in the Document Intelligence workspace.

 Clearly state the information you want to extract. Be specific, clear and concise. For example: "Order number"

</td></tr><tr><td>

Details

</td><td>

A description of the information you want to extract. Along with the field name, the description is used to help the LLM predict the text to extract from the document.

 Include any relevant context or additional details to identify the right information. This might include keywords. For example, "The contract number or the number of the reference contract”.

 Provide examples of what information you want to extract. For example, “AGR-2023-0042”, “CON2039739”, or “BV-22122KEY”.

 Example of a description:

 Field name: “Currency”

 Details: “The currency in which the contract is denominated. Only valid for Order Forms. Otherwise, leave it empty \(''\). If the currency symbol is '$', answer 'USD'. Examples: 'USD', 'EUROS', 'GBP', etc.”

</td></tr><tr><td>

Field Type

</td><td>

The type of field. For example, a text or date field. For more information, see [Field types in Now Assist in Document Intelligence](now-assist-document-intelligence-field-types.md).

 Some field types convert the extracted value into a standard format. For more information, see [Data normalization](../concept/data-normalization.md).

</td></tr><tr><td>

Target table

</td><td>

The table that stores the document processing results for this use case.

</td></tr><tr><td>

Target field

</td><td>

Field on the target table you want to align this field with.

 The use case must have a target table selected.

</td></tr><tr><td>

This single field is required for extraction

</td><td>

Option to make a field required.

 Required fields can’t be left empty or unreviewed.

</td></tr><tr><td>

Create multiple single fields

</td><td>

Option to keep the form displayed on the screen. Enable this if you are adding more than one single field to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist in Document Intelligence forms](now-assist-document-intelligence-forms.md)

**Related topics**  


[Question form for document Q&amp;A setup](document-qna-single-field-form.md)

[Table form for document extraction setup](document-extraction-table-form.md)

