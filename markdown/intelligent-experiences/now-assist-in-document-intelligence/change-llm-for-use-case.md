---
title: Change the language models for a use case
description: Choose the language models for a Now Assist in Document Intelligence use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-in-document-intelligence/change-llm-for-use-case.html
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Configure, Now Assist in Document Intelligence, Enable AI experiences]
---

# Change the language modelsfor a use case

Choose the language models for a Now Assist in Document Intelligenceuse case.

## Before you begin

-   Set up a use case for the extract information from documentsskill. For more information, see [Set up a use case for Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/set-up-use-case-for-now-assist-document-intelligence.md).
-   Role required: sn\_docintel.manager

## About this task

Language models are used to detect information in documents and make predictions for information extraction.

Third-party large language model \(LLM\) providers are available for Now Assist skills and AI agents in addition to Now LLM Service. For more information on LLMs in Now Assist, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

For each Now Assist in Document Intelligence use case, only one LLM can be enabled at a time. Now Assist employs the selected LLM when processing documents for the use case.

For image files that need optical character recognition \(OCR\) to detect the text in them, OCR models are used to support different language groups. The language selected during use case setup helps the OCR model to detect text in the images.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Platform skills list, find the applicable document intelligence skill and select **Edit** in the options menu \( \[Omitted image "icon-docintel-field-options-menu.png"\] Alt text: Field options menu icon\).

4.  Select the use case you would like to configure.

5.  Select the settings icon \(\[Omitted image "icon-docintel-settings-gear.png"\] Alt text: Use case settings icon\).

6.  Selectthe Manage LLMs screen.

7.  Select the LLM that will make predictions for the documents processed with this use case.

    For more information, see [Large language models used by Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/llms-now-assist-document-intelligence.md).

8.  Turn on image mode to process images more efficiently.

    Image mode sends pages to the LLM as images to leverage the visual capability of the multimodal LLM as well as any of the languages supported by it.

    The image mode option is available when a multimodal LLM is selected.

    **Note:** Selecting image mode reduces the page count limit to 10 pages per file.

9.  Select the **Language of the files** processed for the use case.

    If the files contain multiple languages, select the primary language.

    For more information, see [Languages supported by Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/languages-supported-now-assist-document-intelligence.md).

10. Select **Save**.


## Result

The selected languages areenabled for the use case.

**Parent Topic:**[Configuring Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/docintel-configuring-now-assist.md)

**Related topics**  


[Activate a Now Assist in Document Intelligence skill]()

[Set up a use case for Now Assist in Document Intelligence]()

[Turn on Full automation mode for a use case]()

[Edit a use case in Now Assist in Document Intelligence]()

[Make a copy of a use case in Now Assist in Document Intelligence]()

[Deactivate a use case in Now Assist in Document Intelligence]()

[Delete a use case in Now Assist in Document Intelligence]()

