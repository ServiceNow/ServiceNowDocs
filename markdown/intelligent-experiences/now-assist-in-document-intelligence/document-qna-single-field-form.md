---
title: Question form for use case setup
description: The Question form enables you to define a question you want to ask about the document.
locale: en-US
release: zurich
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Forms, Reference, Now Assist in Document Intelligence, Enable AI experiences]
---

# Question form for use casesetup

The Question form enables you to define a question you want to ask about the document.

The Question form includes the following fields.

<table id="table_e3b_jz5_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

The question about the document. This question is sent to the generative AI for a prediction.

 Write a clear and concise question about the information you want to find in the document. For example, "Is this document subject to expiration?". 

 Below the question, add details about how generative AI can best provide the correct answer. For example, “Review the sections where validity, duration or time frames are discussed and look for any details about expiration dates, renewal requirements, or explicit statements declaring the document as permanent. Answer ‘Yes’ if the document is subject to an expiration date. Answer ‘No’ if there is no mention of expiration or contains an explicit statement that it is permanent.”

 **Tip:** View the **Question assistance** tab for additional guidance on forming an effective question.

 This question is displayed to the agent when reviewing the answers in the Document Intelligence workspace.

</td></tr><tr><td>

Field Type

</td><td>

The type of field \(for example, a text or Boolean field\).

 For more information, see [Field types in Now Assist in Document Intelligence](now-assist-document-intelligence-field-types.md).

</td></tr><tr><td>

Provide an explanation for the answer

</td><td>

Option to have the generative AI provide an explanation based on the document text that supports a yes or no answer.

 This field is available when the **Field Type** field is set to `Boolean (True/False)`.

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

Option to make a questionrequired. Required questions can’t be left empty or unreviewed.

</td></tr><tr><td>

Create multiple single fields

</td><td>

Option to keep the form displayed on the screen. Enable this if you are adding more than one questionto the use case.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist in Document Intelligence forms](now-assist-document-intelligence-forms.md)

**Related topics**  


[Field form for use case setup](document-extraction-single-field-form.md)

[Table form for use case setup](document-extraction-table-form.md)

