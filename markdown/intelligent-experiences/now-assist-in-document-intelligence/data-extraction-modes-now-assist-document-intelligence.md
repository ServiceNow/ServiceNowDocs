---
title: Data extraction modes in Now Assist in Document Intelligence
description: The extraction mode determines how Now Assist in Document Intelligence processes a document task. Extraction modes only apply to use cases for the document extraction skill.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: reference
last_updated: "2025-04-02"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Now Assist in Document Intelligence reference, Now Assist in Document Intelligence, Enable AI experiences]
---

# Data extraction modes in Now Assist in Document Intelligence

The extraction mode determines how Now Assist in Document Intelligence processes a document task. Extraction modes only apply to use cases for the document extraction skill.

Now Assist in Document Intelligence uses the following data extraction modes.

<table id="table_iqg_n4k_w2c"><thead><tr><th>

Extraction mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default

</td><td>

Now Assist auto-fills each field in the Document Intelligence workspace if it recognizes a value for it in the document.

 Now Assist may not always produce accurate, complete, or appropriate information. All fields should be reviewed for accuracy.

 A reviewer can accept the predicted value or manually enter a value.

</td></tr><tr><td>

Full automation

</td><td>

Now Assist automatically completes and submits the document task without an agent review. The values for all required fields are auto-filled by Now Assist or are identified as missing in the document.

 By turning on Full automation mode, the agent review used to check the accuracy of the predicted values is bypassed.

 There is a configuration option to suspend the automation and require an agent review when any of the required fields are missing in the document.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist in Document Intelligence reference](now-assist-in-document-intelligence-reference.md)

**Related topics**  


[Components installed with Now Assist in Document Intelligence](now-assist-docintel-components.md)

[Document and visual insights AI agent](document-and-visual-insights-ai-agent.md)

[Field types in Now Assist in Document Intelligence](now-assist-document-intelligence-field-types.md)

[Now Assist in Document Intelligence forms](now-assist-document-intelligence-forms.md)

