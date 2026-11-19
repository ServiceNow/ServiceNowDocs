---
title: Change the large language model \(LLM\) for a use case
description: Choose a large language model \(LLM\) used to generate predictions for extraction and Q&amp;A use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-in-document-intelligence/change-llm-for-use-case.html
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: task
last_updated: "2025-07-15"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Configuring Now Assist in Document Intelligence, Now Assist in Document Intelligence, Enable AI experiences]
---

# Change the large language model \(LLM\) for a use case

Choose a large language model \(LLM\) used to generate predictions for extraction and Q&amp;A use cases.

## Before you begin

-   Set up a use case for the document extraction or document Q&amp;A skill. For more information, see [Set up a use case for Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-in-document-intelligence/set-up-use-case-for-now-assist-document-intelligence.md).
-   Role required: sn\_docintel.manager

## About this task

Third-party LLM providers are available for Now Assist skills and AI agents in addition to Now LLM Service. For more information on LLMs in Now Assist, see [Manage large language models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/manage-large-language-models.md).

For each Now Assist in Document Intelligence use case, only one LLM can be enabled at a time. Now Assist employs the selected LLM when processing documents for the use case.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Platform skills list, find the applicable document intelligence skill and select **Edit** in the options menu \( \[Omitted image "icon-docintel-field-options-menu.png"\] Alt text: Field options menu icon\).

4.  Select the use case you would like to configure.

5.  Click the settings icon \(\[Omitted image "icon-docintel-settings-gear.png"\] Alt text: Use case settings icon\).

6.  On the Manage LLMs screen, select the **LLM provider**.

7.  Select **Save**.


## Result

The selected LLM is enabled for the use case.

**Parent Topic:**[Configuring Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-in-document-intelligence/docintel-configuring-now-assist.md)

**Related topics**  


[Activate a Now Assist in Document Intelligence skill]()

[Set up a use case for Now Assist in Document Intelligence]()

[Turn on Full automation mode for a document extraction use case]()

[Edit a use case in Now Assist in Document Intelligence]()

[Make a copy of a use case in Now Assist in Document Intelligence]()

[Deactivate a use case in Now Assist in Document Intelligence]()

[Delete a use case in Now Assist in Document Intelligence]()

