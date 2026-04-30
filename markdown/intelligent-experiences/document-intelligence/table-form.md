---
title: Table form
description: The Table form enables you to define a table for extraction.
locale: en-US
release: zurich
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2026-01-27"
reading_time_minutes: 4
breadcrumb: [DocIntel forms, Reference, Document Intelligence, Enable AI experiences]
---

# Table form

The Table form enables you to define a table for extraction.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

The Table form includes the following fields.

<table id="table_wxp_lpt_bzb"><thead><tr><th>

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

Target table

</td><td>

The table that stores the document processing results for these table fields.

</td></tr><tr><td>

Parent mapping to field

</td><td>

Field on the target table that you want to align this table with.

 **Note:** You must first select a target table.

</td></tr><tr><td>

This table is required for extraction

</td><td>

Option to make the table fields required.

 Required table fields can't be left empty or unreviewed. They also can’t contain ambiguous values. An ambiguous value is a field entry that can be interpreted in more than one way.

 Required fields affect how document tasks are processed in the Fully automated extraction mode. For more information, see [Configure data extraction modes](../task/configure-data-extraction-modes.md).

</td></tr><tr class="sub-head"><td>

Columns

</td><td>

 

</td></tr><tr><td>

Column title

</td><td>

Name of the column header in the table.

</td></tr><tr><td>

Type

</td><td>

The type of the field in the table column. For example, a text or date field.

 Some field types convert the extracted value into a standard format. For more information, see [Data normalization](../concept/data-normalization.md).

</td></tr><tr><td>

Select target field

</td><td>

Field on the target table that you want to align this field with.

 This field is used for integration with other applications. For more information, see [Integrate with a custom application or workflow](../task/configure-integration-setup.md).

</td></tr><tr><td>

When the date is ambiguous in a document, DocIntel will interpret it in the following order

</td><td>

The default interpretation of the date format.

 For example, if you select `Month first` in this field, DocIntel will interpret an ambiguous date like 1/2/2024 as January 2 when it extracts that value from a document. If you select `Day first`, it will interpret it as February 1.

 This field is available when the **Type** field is set to `Date`.

</td></tr><tr><td>

When the number is ambiguous in a document, DocIntel will interpret it as

</td><td>

The default interpretation of the number format.

 For example, if you select `1,00` in this field, DocIntel will interpret an ambiguous number like 5 as 5,00 instead of 5.00 when it extracts that value from a document.

 This field is available when the **Type** field is set to `Integer`, `Decimal`, or `Float`.

</td></tr><tr><td>

Reference table

</td><td>

The table that stores the reference column. It’s automatically populated based on the selected target field.

 This field displays when the **Type** field is set to `Reference field`.

</td></tr><tr><td>

Reference column

</td><td>

The column in the reference table that contains the referenced data.

 DocIntel uses the reference column to find data that matches the extracted field value when processing a document task. The field value is then converted to the format of the reference. For more information on converted values, see [Data normalization](../concept/data-normalization.md).

 This field is available when the **Type** field is set to `Reference field`.

</td></tr><tr><td>

Distinguisher\(s\)

</td><td>

Additional columns in the reference table that help the user to distinguish between similar records.

 This field is available when the **Type** field is set to `Reference field`.

</td></tr><tr><td>

This field is required for extraction

</td><td>

Indicates whether a column required. It’s automatically selected or cleared based on whether the table is required.

 Required column fields can't be left empty or unreviewed. They also can’t contain ambiguous values. An ambiguous value is a field entry that can be interpreted in more than one way.

 If it’s a reference field type, the required field must have a valid, exact match. By default, DocIntel uses the first matched record.

 Required fields affect how document tasks are processed in the Fully automated extraction mode. For more information, see [Configure data extraction modes](../task/configure-data-extraction-modes.md).

</td></tr><tr><td>

Select one of these options for cases when:-   the date/number is ambiguous in the document
-   there are multiple reference matches in the document

</td><td>

Option for agent review in situations when DocIntel encounters an ambiguous value in a required field.

 In such cases, the selected default interpretation will apply to the extracted value.

 The option is whether to interrupt full automation of document tasks to allow agents to verify the interpreted values. Otherwise, continue automatic processing of document tasks without the agent review.

</td></tr><tr><td>

New column

</td><td>

Option to add a column to the table.

 Use the reorder icon \(![Reorder icon.](../image/icon-docintel-drag.png)\) to reorder a column in the table.

</td></tr><tr><td>

Create multiple tables

</td><td>

Option to keep the pop-up window displayed on the screen. Enable this option If you're adding more than one table to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence forms](document-intelligence-forms.md)

