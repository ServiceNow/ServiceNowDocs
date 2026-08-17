---
title: Table form fields
description: The Table form contains fields for defining a table and its columns for document extraction in a use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/table-form.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Forms, Reference, Content Understanding, Enable AI experiences]
---

# Table form fields

The Table form contains fields for defining a table and its columns for document extraction in a use case.

\[Omitted image "cu-table-field.png"\] Alt text: Table form used to specify information to extract from a document.

<table id="table_e3f_xyw_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

Name of the table.

</td></tr><tr><td>

Additional Details

</td><td>

Description of the table information to extract. Along with the table name, the description helps the large language model \(LLM\) predict which table fields to extract from the document. Include any relevant context or additional details to identify the correct information.

</td></tr><tr><td>

Target table

</td><td>

Table that stores the document processing results for these table fields.

</td></tr><tr><td>

Parent mapping to field

</td><td>

Field on the target table to align this table with. Select a target table before configuring this field.

</td></tr><tr><td>

This table is required for extraction

</td><td>

When selected, the table is required for extraction. Required fields must be completed and cannot be left empty or cleared.

</td></tr><tr><td>

Column title

</td><td>

Name of the column header in the table.

</td></tr><tr><td>

Column type

</td><td>

Type of field in the table column — for example, a text or date field. For more information, see [Field types in Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/field-types.md). Some field types convert the extracted value into a standard format. For more information, see [Data normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/data-normalization.md).

</td></tr><tr><td>

Select target field

</td><td>

Field on the target table to align with. **Note:** The use case must include a selected target table.

</td></tr><tr><td>

New column

</td><td>

Option to add a column to the table.

</td></tr><tr><td>

Create multiple tables

</td><td>

When selected, keeps the form open after saving. Select this option when adding more than one table to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Content Understanding forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-forms.md)

