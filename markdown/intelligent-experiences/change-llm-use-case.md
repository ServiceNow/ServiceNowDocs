---
title: Change the language models for a use case
description: Select the LLM and file language for a use case to control how documents are processed for information extraction. Change these settings when the default model doesn't suit your use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/change-llm-use-case.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Manage use case, Reference, Content Understanding, Enable AI experiences]
---

# Change the language models for a use case

Select the LLM and file language for a use case to control how documents are processed for information extraction. Change these settings when the default model doesn't suit your use case.

## Before you begin

-   Set up a use case for the Information Extraction skill. For more information, see [Set up a use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-use-case.md).
-   Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\].

## About this task

Language models detect information in documents and make predictions for information extraction.

Third-party LLM providers are available for skills and AI agents in addition to Now LLM Service. For more information on LLMs, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

For each use case, only one LLM can be enabled at a time. The selected LLM processes documents for the use case.

For image files that need optical character recognition \(OCR\) to detect the text in them, OCR models are used to support different language groups. The language selected during use case setup helps the OCR model to detect text in the images.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Platform skills list, find the applicable skill.

4.  Select **Edit** in the options menu \(\[Omitted image "cu-options-menu.png"\] Alt text:\) for that skill.

5.  Select the use case to configure.

6.  Select the Settings icon \(\[Omitted image "cu-settings-gear-icon.png"\] Alt text:\).

7.  Select the **Manage LLMs** tab.

8.  Select the LLM to use for predictions on documents processed with this use case.

    For more information, see [Large language models used by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-llms.md).

9.  Turn on image mode to process images more efficiently.

    Image mode sends pages to the LLM as images to use the visual capability of the multimodal LLM and any languages it supports.

    The image mode option is available when a multimodal LLM is selected.

    **Note:** Selecting image mode reduces the page count limit to 10 pages per file.

10. Select the **Language of the files** processed for the use case.

    If the files contain multiple languages, select the primary language.

    For more information, see [Languages supported by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/languages-supported.md).

11. Select **Save**.


## Result

The selected LLM and file language are saved for the use case.

**Parent Topic:**[Manage use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-use-case.md)

