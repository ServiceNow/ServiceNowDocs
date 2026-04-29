---
title: Limitations in Now Assist in Document Intelligence
description: There are several important limitations to be aware of when you’re using Now Assist in Document Intelligence.
locale: en-US
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Reference, Now Assist in Document Intelligence, Enable AI experiences]
---

# Limitations in Now Assist in Document Intelligence

There are several important limitations to be aware of when you’re using Now Assist in Document Intelligence.

## Now Assist in Document Intelligence skill limits

The following table lists the important limitations for the skills in Now Assist in Document Intelligence.

<table id="table_uds_5wj_lgc"><thead><tr><th>

Limit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File formats

</td><td>

The supported file formats are JPEG, PNG, PDF, and DOCX.

**Note:** Encrypted files are not supported.

</td></tr><tr><td>

File size limit

</td><td>

The file size limit is 20 MB.

</td></tr><tr><td>

Page count limit

</td><td>

If image mode is turned on for the use case, the page count limit is 10 pages per file.

 If image mode is turned off, the page count limit is:

-   200 pages per file if no tables are defined for the use case.
-   20 pages per file if a table is defined for the use case.

 Image mode is selected during use case setup. For more information, see [Set up a use case for Now Assist in Document Intelligence](../task/set-up-use-case-for-now-assist-document-intelligence.md).

</td></tr><tr><td>

Maximum number of fields per use case

</td><td>

The maximum number of fields per use case is 50.

</td></tr><tr><td>

Supported languages

</td><td>

For image files that need optical character recognition \(OCR\) to detect the text in them, there are OCR models to support different language groups. For more information, see [Languages supported by Now Assist in Document Intelligence](languages-supported-now-assist-document-intelligence.md).

 For text-based files, the skill recognizes any language supported by the selected or default model, as described in the model card for the LLM. For more information on LLMs, see [Large language models used by Now Assist in Document Intelligence](llms-now-assist-document-intelligence.md).

</td></tr></tbody>
</table>## Limits for the document and visual insights AI agent

The following table lists the important limitations for the document and visual insights AI agent.

<table id="table_lkm_ywj_lgc"><thead><tr><th>

Limit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File formats

</td><td>

The supported file formats are JPEG, PNG, PDF, DOCX, XLSX, CSV, TXT, and PPTX.

</td></tr><tr><td>

File size limit

</td><td>

The file size limit is 20 MB.

</td></tr><tr><td>

Page count limit

</td><td>

For each document task, the page count limit is 200 pages per file.

 If the AI agent performs the extraction based on a use case that includes a table, the limit decreases to 20 pages per file.

</td></tr><tr><td>

Supported languages

</td><td>

For image and text-based files, the AI agent recognizes any language supported by the selected or default model, as described in the model card for the LLM. For more information on LLMs, see [Large language models used by Now Assist in Document Intelligence](llms-now-assist-document-intelligence.md).

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist in Document Intelligence reference](now-assist-in-document-intelligence-reference.md)

**Related topics**  


[Components installed with Now Assist in Document Intelligence](now-assist-docintel-components.md)

[Data extraction modes in Now Assist in Document Intelligence](data-extraction-modes-now-assist-document-intelligence.md)

[Document and visual insights AI agent](document-and-visual-insights-ai-agent.md)

[Document Intelligence tool for Now Assist Skill Kit](document-visual-intelligence-skill-kit-tool.md)

[Field types in Now Assist in Document Intelligence](now-assist-document-intelligence-field-types.md)

[Now Assist in Document Intelligence forms](now-assist-document-intelligence-forms.md)

[Large language models used by Now Assist in Document Intelligence](llms-now-assist-document-intelligence.md)

[Languages supported by Now Assist in Document Intelligence](languages-supported-now-assist-document-intelligence.md)

