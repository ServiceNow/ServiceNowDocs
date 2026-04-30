---
title: Data extraction modes
description: Extraction modes determine how the data is extracted in the document task and how the task is processed. The mode changes the behavior of the fields in the Document Intelligence workspace.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Document Intelligence references, Document Intelligence, Enable AI experiences]
---

# Data extraction modes

Extraction modes determine how the data is extracted in the document task and how the task is processed. The mode changes the behavior of the fields in the Document Intelligence workspace.

DocIntel uses the following extraction modes.

<table id="table_pmc_dqx_qbc"><thead><tr><th>

Extraction mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommendation

</td><td>

DocIntel provides recommendations for the fields in the Document Intelligence workspace. Choose the recommendation or manually enter the value. All fields must be reviewed.

 Recommendations are ordered based on how confident the AI is in the prediction. As DocIntel continues processing your documents, recommendations improve over time.

</td></tr><tr><td>

Auto-fill

</td><td>

DocIntel auto-fills the fields in the Document Intelligence workspace. All fields must be reviewed.

 Auto-fill works only if the AI has enough confidence to make the prediction. You can change the confidence threshold by updating the **Auto-fill threshold** field in the use case.

</td></tr><tr><td>

Fully automated

 \(Straight-through processing\)

</td><td>

DocIntel automatically extracts the data for all fields and processes the document task if the confidence scores for all required fields are above the defined confidence threshold. Fields don’t need to be reviewed.

 **Note:** For Fully automated mode to process tasks successfully, the use case must have at least one field designated as required.

 DocIntel becomes more confident over time, as it processes more and more documents. Choose Fully automated mode for frequently processed documents or if you’re confident in the system.

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence references](docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence](installed-with-document-intelligence.md)

[Confidence scores](../concept/docintel-confidence-scores.md)

[Data normalization](../concept/data-normalization.md)

[Document field statuses](docintel-field-statuses.md)

[Document Intelligence forms](document-intelligence-forms.md)

[Document Intelligence properties](document-intelligence-properties.md)

[Document Intelligence roles](document-intelligence-user-roles.md#)

[Document Intelligence terminology](../concept/docintel-terminology.md#)

[Document task statuses](docintel-task-statuses.md)

[Domain separation and Document Intelligence](domain-separation-and-doc-intel.md)

[Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md)

[Limitations in Document Intelligence](hard-limits-in-doc-intel.md)

