---
title: Field types in Content Understanding
description: Field types determine what kind of information is extracted from a document and how that information is stored or displayed in a use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/field-types.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Reference, Content Understanding, Enable AI experiences]
---

# Field types in Content Understanding

Field types determine what kind of information is extracted from a document and how that information is stored or displayed in a use case.

The following field types are available to administrators when configuring fields for use cases.

**Note:** Some field types convert the extracted value into a standard format. For more information, see [Data normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/data-normalization.md).

<table id="table_nql_cxs_12c"><thead><tr><th>

Field type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Boolean \(True/False\)**

</td><td>

True or false value. In document Q&amp;A, this value appears as a "yes" or "no" answer. If enabled by the administrator, the answer may include an AI-generated explanation, which may not always be accurate. Available for questions defined in the use case setup. \[Omitted image "cu-boolean-field-question.png"\] Alt text: Boolean field type

</td></tr><tr><td>

**Date**

</td><td>

Date displayed in the format extracted from the document. Available for fields and tables defined in the use case setup. \[Omitted image "cu-date-field.png"\] Alt text: Date field type

</td></tr><tr><td>

**Decimal**

</td><td>

Number with up to two decimal places \(for example, 12.5 or 12.55\). Available for fields and tables defined in the use case setup. \[Omitted image "cu-decimal-field.png"\] Alt text: Decimal field type

</td></tr><tr><td>

**Float \(floating point number\)**

</td><td>

Number with up to seven decimal places \(for example, 12.0 to 12.0000000\). Available for fields and tables defined in the use case setup. \[Omitted image "cu-float-field.png"\] Alt text: Float field type

</td></tr><tr><td>

**Integer**

</td><td>

Whole number \(for example, 12\). Available for fields and tables defined in the use case setup. \[Omitted image "cu-integer-field.png"\] Alt text: Integer field type

</td></tr><tr><td>

**Reference**

</td><td>

Reference to a field on another table. For example, the **Caller** field on the incident table is a reference to the User \[sys\_user\] table. For more information, see [Reference field type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceField.md).

 Available for fields and tables defined in the use case setup.

 \[Omitted image "cu-reference-field.png"\] Alt text: Reference field type

</td></tr><tr><td>

**Text**

</td><td>

Text value. Available for fields, tables, and questions defined in the use case setup. \[Omitted image "cu-text-field.png"\] Alt text: Text field type

</td></tr></tbody>
</table>**Parent Topic:**[Content Understanding Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-reference.md)

