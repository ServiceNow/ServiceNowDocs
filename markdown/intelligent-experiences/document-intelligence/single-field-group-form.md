---
title: Single field group form
description: The Single field group form enables you to define a related group of single fields for extraction.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Document Intelligence forms, Document Intelligence references, Document Intelligence, Enable AI experiences]
---

# Single field group form

The Single field group form enables you to define a related group of single fields for extraction.

The Single field group form includes the following fields.

<table id="table_v5s_lpt_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td>

Field group

</td><td>

 

</td></tr><tr><td>

Field group name

</td><td>

The name for the field group as it appears in the Document Intelligence workspace.

</td></tr><tr><td>

Target table

</td><td>

The table that stores the document processing results for the fields.

</td></tr><tr><td>

Parent mapping to field

</td><td>

Field on the target table that you want to align this field group with.

 **Note:** You must first select a target table.

</td></tr><tr><td>

This field group is required for extraction

</td><td>

Option to make the field as required.

 Required fields can’t be left empty or unreviewed. They also can’t contain ambiguous values. An ambiguous value is a field entry that can be interpreted in more than one way.

 If it’s a reference field type, the required field must have a valid, exact match. By default, DocIntel uses the first matched record.

 Required fields affect how document tasks are processed in the Fully automated extraction mode. For more information, see [Configure data extraction modes](../task/configure-data-extraction-modes.md).

</td></tr><tr class="sub-head"><td>

Fields

</td><td>

 

</td></tr><tr><td>

Field name

</td><td>

The name for the field as it appears in the Document Intelligence workspace.

</td></tr><tr><td>

Type

</td><td>

The type of the field. For example, a text or date field.

 Some field types convert the extracted value into a standard format. For more information, see [Data normalization](../concept/data-normalization.md).

</td></tr><tr><td>

Select Target Field

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

 For example, if you select 1,00 in this field, DocIntel will interpret an ambiguous number like 5 as 5,00 instead of 5.00 when it extracts that value from a document.

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

Option to make a field required.

 Required fields can’t be left empty or unreviewed. They also can’t contain ambiguous values. An ambiguous value is a field entry that can be interpreted in more than one way.

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

New single field

</td><td>

Option to add a field to the group.

 Use the reorder icon \(![Reorder icon.](../image/icon-docintel-drag.png)\) to reorder a field in the group.

</td></tr><tr><td>

Create multiple field groups

</td><td>

Option to keep the pop-up window displayed on the screen. Enable this option if you're adding more than one single field group to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence forms](document-intelligence-forms.md)

