---
title: Table form for document extraction setup
description: The Table form enables you to define a table for extraction.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Now Assist in Document Intelligence forms, Now Assist in Document Intelligence reference, Now Assist in Document Intelligence, Enable AI experiences]
---

# Table form for document extraction setup

The Table form enables you to define a table for extraction.

The Table form includes the following fields.

<table id="table_e3f_xyw_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td>

Table

</td><td>

 

</td></tr><tr><td>

Table name

</td><td>

The name for the table as it appears in the Document Intelligence workspace.

</td></tr><tr><td>

Additional Details

</td><td>

A description of the table information you want to extract. Along with the table name, the description is used to help the LLM predict the table fields to extract from the document.

 Include any relevant context or additional details to identify the right information.

</td></tr><tr><td>

Target table

</td><td>

The table that stores the document processing results for these table fields.

</td></tr><tr><td>

Parent mapping to field

</td><td>

Field on the target table you want to align this table with.

 You must first select a target table.

</td></tr><tr><td>

This table is required for extraction

</td><td>

Option to make the table fields required.

 Required table fields can’t be left empty or unreviewed.

</td></tr><tr class="sub-head"><td>

Columns

</td><td>

 

</td></tr><tr><td>

Column title

</td><td>

Name of the column header in the table.

</td></tr><tr><td>

Column type

</td><td>

The type of field in the table column. For example, a text or date field. For more information, see [Field types in Now Assist in Document Intelligence](now-assist-document-intelligence-field-types.md).

 Some field types convert the extracted value into a standard format. For more information, see [Data normalization](../concept/data-normalization.md).

</td></tr><tr><td>

Select target field

</td><td>

Field on the target table you want to align this field with.

 The use case must have a target table selected.

</td></tr><tr><td>

New column

</td><td>

Option to add a column to the table.

</td></tr><tr><td>

Create multiple tables

</td><td>

Option to keep the form displayed on the screen. Enable this option if you’re adding more than one table to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist in Document Intelligence forms](now-assist-document-intelligence-forms.md)

**Related topics**  


[Question form for document Q&amp;A setup](document-qna-single-field-form.md)

[Field form for document extraction setup](document-extraction-single-field-form.md)

