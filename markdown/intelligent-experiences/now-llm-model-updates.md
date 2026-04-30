---
title: Now LLM Service updates
description: The Now LLM Service provides access to specialized large language models \(LLMs\) that are developed by ServiceNow. It also provides access to open-source LLMs that are selected, configured, or enhanced by ServiceNow, from the ServiceNow community and partners. Review these reference materials and model cards for additional information about the Now LLM Service and about the models used.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [model card, Now LLM Service, LLM, Large language model, Generative AI, Gen AI, Now Assist]
breadcrumb: [Now Assist, Enable AI experiences]
---

# Now LLM Service updates

The Now LLM Service provides access to specialized large language models \(LLMs\) that are developed by ServiceNow. It also provides access to open-source LLMs that are selected, configured, or enhanced by ServiceNow, from the ServiceNow community and partners. Review these reference materials and model cards for additional information about the Now LLM Service and about the models used.

## Model cards

Large language models \(LLMs\) are complex machine-learning models that are trained on large datasets like websites and documentation to perform language-related tasks, such as text generation for case summaries and resolution notes.

Model cards explain the specific model's context, intended use, training data, limitations, and other important information.

These model cards are for skills that use the Now LLM Service. There are certain skills, such as Now Assist Multi-Turn Catalog Ordering, that use Azure OpenAI instead. To see what LLM a skill is using, you can check the skill list in the Now Assist Admin console and review the LLM service column.

-   **[Model card for ServiceNow text-to-text LLM](https://downloads.docs.servicenow.com/resource/enus/infocard/text-to-text-llm.pdf)**

    Model used for conversational use cases like Virtual Agent topic execution and conversational catalog and agent assist use cases like alert analysis, AI search, and incident, case, and chat summarization.

-   **[Model card for ServiceNow text-to-code LLM](https://downloads.docs.servicenow.com/resource/enus/infocard/text-to-code-llm.pdf)**

    Model used for code generation.

-   **[Model card for ServiceNow flow next-best-action LLM](https://downloads.docs.servicenow.com/resource/enus/infocard/flow-best-action-llm.pdf)**

    Model used for flow recommendations.

-   **[Model card for ServiceNow text-to-flow LLM](https://downloads.docs.servicenow.com/resource/enus/infocard/text2flow-llm.pdf)**

    Model used for flow generation.

-   **[Model card for ServiceNow text-to-text SLM](https://downloads.docs.servicenow.com/resource/enus/infocard/text-to-text-slm.pdf)**

    Model used for Now Assist Guardian, text-to-cypher and other use cases that demand rapid inference and high throughput.

-   **[https://downloads.docs.servicenow.com/resource/enus/infocard/third-party-llm.pdf](https://downloads.docs.servicenow.com/resource/enus/infocard/third-party-llm.pdf)**

    Model used for AI-driven solutions for text generation, summarization, and conversational AI.


## November 2024

Several key improvements were added to the Now LLM Service that are aimed at enhancing performance and quality.

-   Multilingual support: Now LLM Service supports 8 additional languages, enabling global teams to use the model in their native languages.

    The supported languages are: English, German, French, Japanese, Dutch, French Canadian, Spanish, Brazilian Portuguese, and Italian.

-   JSON format support: The model now provides output in JSON format, making it easier for developers to integrate with various applications and automate workflows seamlessly.
    -   Deterministic responses: JSON mode ensures structured, consistent output, which improves predictability and reliability when integrating with applications.
    -   Error reduction: Unlike free-form text mode, JSON responses are less prone to format errors or stray characters, minimizing integration issues.
    -   Lower token consumption: The fixed structure of JSON can reduce token usage, making it more efficient and cost-effective for applications with high response frequency.
-   Improvements in instruction following: The model has been fine-tuned to understand and follow instructions more precisely. This enables the model to deliver more to-the-point and actionable responses, helping users get the information they need faster and more efficiently.

