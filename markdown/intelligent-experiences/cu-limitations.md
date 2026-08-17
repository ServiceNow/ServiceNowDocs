---
title: Limitations in Content Understanding
description: Review the file format, size, page count, and language limitations that apply to skills and AI agents in Content Understanding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cu-limitations.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Reference, Content Understanding, Enable AI experiences]
---

# Limitations in Content Understanding

Review the file format, size, page count, and language limitations that apply to skills and AI agents in Content Understanding.

## Information extraction skill limitations

The following table lists the limitations for the Information Extraction skill in Content Understanding.

<table id="table_uds_5wj_lgc"><thead><tr><th>

Limit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File formats

</td><td>

The supported file formats are JPEG, PNG, PDF, and DOCX. **Note:** Encrypted files aren't supported.

</td></tr><tr><td>

File size limit

</td><td>

The file size limit is 20 MB.

</td></tr><tr><td>

Page count limit

</td><td>

When image mode is enabled, the suggested upper boundary is 50 pages per file, with a minimum of 10 pages. Actual performance varies based on the following factors:

 -   Model constraints: Some models limit the number of images per request. For example, some models allow a maximum of 20 images per request.
-   File complexity and size: Documents with dense text or large images consume more tokens and memory, which can affect processing time and efficiency.
-   Platform payload limits: The upper limit for data passed to the language model is 32 MB. Because image sizes vary, the exact page count that fits within this limit varies by document.

 Because these constraints depend on your configuration, document characteristics, and the model used, test your documents by gradually increasing the page count to identify the effective limits for your use case.

 If image mode is enabled, the page count limit is 10 pages per file.

 If image mode is inactive, the page count limit is:

-   200 pages per file if no tables are defined for the use case.
-   20 pages per file if a table is defined for the use case.

 Image mode is selected during use case setup. For more information, see [Set up a use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-use-case.md).

</td></tr><tr><td>

Maximum number of fields per use case

</td><td>

The maximum number of fields per use case is 50.

</td></tr><tr><td>

Supported languages

</td><td>

For image files that require OCR \(optical character recognition\) to detect text, OCR models support different language groups. For more information, see [Languages supported by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/languages-supported.md).

 For text-based files, the skill recognizes any language supported by the selected or default model, as described in the model card for the LLM. For more information on LLMs, see [Large language models used by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-llms.md).

</td></tr></tbody>
</table>## Limits for the Content insights AI agent

The following table lists the limitations for the Content insights AI agent.

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

 If the AI agent extracts data based on a use case that includes a table, the limit decreases to 20 pages per file.

</td></tr><tr><td>

Supported languages

</td><td>

For image and text-based files, the AI agent recognizes any language supported by the selected or default model, as described in the model card for the LLM. For more information on LLMs, see [Large language models used by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-llms.md).

</td></tr></tbody>
</table>**Parent Topic:**[Content Understanding Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-reference.md)

