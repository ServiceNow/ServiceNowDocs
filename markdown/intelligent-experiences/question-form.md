---
title: Question form fields
description: The Question form contains fields that define a question and how its answer is extracted from a document in a use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/question-form.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Forms, Reference, Content Understanding, Enable AI experiences]
---

# Question form fields

The Question form contains fields that define a question and how its answer is extracted from a document in a use case.

## Question form fields

\[Omitted image "cu-question-form.png"\] Alt text: A question form used to specify the information that must be extracted from a document.

<table id="id_xzg_5pb_zjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

The question about the document that generative AI uses to extract information. This question is displayed to the agent when reviewing answers in the Document Intelligence workspace. **Tip:** Select the **Question assistance** tab for guidance on formulating effective questions.

</td></tr><tr><td>

Field Type

</td><td>

Type of field — for example, text or Boolean. For descriptions of available field types, see [Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/field-types.md).

</td></tr><tr><td>

Provide an explanation for the answer

</td><td>

Option to have generative AI provide an explanation, based on the document text, that supports a yes or no answer. This field appears only when the **Field Type** field is set to **Boolean \(True/False\)**.

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

Option to mark a question as required. Required questions must be answered and can't be left empty or cleared.

</td></tr><tr><td>

Create multiple single fields

</td><td>

Option to keep the form displayed on the screen. Select this option when adding more than one question to the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Content Understanding forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-forms.md)

