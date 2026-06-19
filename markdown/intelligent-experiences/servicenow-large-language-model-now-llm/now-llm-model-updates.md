---
title: Now LLM Service updates
description: The Now LLM Service provides access to specialized large language models \(LLMs\) that are developed by ServiceNow. It also provides access to open-source LLMs that are selected, configured, or enhanced by ServiceNow, from the ServiceNow community and partners. Review these reference materials and model cards for additional information about the Now LLM Service and about the models used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-large-language-model-now-llm/now-llm-model-updates.html
release: australia
product: ServiceNow Large Language Model \(Now LLM\)
classification: servicenow-large-language-model-now-llm
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 6
keywords: [model card, Now LLM Service, LLM, Large language model, Generative AI, Gen AI, Now Assist]
breadcrumb: [Large language models on the ServiceNow AI Platform, Enable AI experiences]
---

# Now LLM Service updates

The Now LLM Service provides access to specialized large language models \(LLMs\) that are developed by ServiceNow. It also provides access to open-source LLMs that are selected, configured, or enhanced by ServiceNow, from the ServiceNow community and partners. Review these reference materials and model cards for additional information about the Now LLM Service and about the models used.

## Model cards

Large language models \(LLMs\) are complex machine-learning models that are trained on large datasets like websites and documentation to perform language-related tasks, such as text generation for case summaries and resolution notes.

Model cards explain the specific model's context, intended use, training data, limitations, and other important information.

These model cards are for skills that use the Now LLM Service. There are certain skills, such as Now Assist Multi-Turn Catalog Ordering, that use Azure OpenAI instead. To see what LLM a skill is using, you can check the skill list in the Now Assist Admin console and review the LLM service column.

-   **[Model card for ServiceNow large language model](https://downloads.docs.servicenow.com/resource/enus/infocard/sn-llm.pdf)**

    Model used for AI-driven solutions to support natural language understanding, automation, and decision support.

    This model card is available in Yokohama patch 1 and later.

-   **[Model card for ServiceNow large language model \(V2\)](https://downloads.docs.servicenow.com/resource/enus/infocard/sn-llm-v2.pdf)**

    Model for enterprise AI that enhances text-based automation and content generation in ServiceNow workflows, including requester OOTB skills, custom skills, and agentic use cases.

    This model is for Generative AI Controller application 11.2 or higher.

-   **[Model card for ServiceNow small language model](https://downloads.docs.servicenow.com/resource/enus/infocard/sn-slm.pdf)**

    Model used for enterprise AI applications by enhancing text-based automation and content generation within ServiceNow workflows.

    This model card is available in Yokohama patch 1 and later.

-   **[Model card for ServiceNow small language model \(V2\)](https://downloads.docs.servicenow.com/resource/enus/infocard/sn-slm-v2.pdf)**

    Model for enterprise AI that enhances text-based automation and content generation in ServiceNow workflows, including creator and fulfiller OOTB skills as well as custom skills.

    This model is for Generative AI Controller application 11.2 or higher.

-   **[Model card for ServiceNow third party large language model](https://downloads.docs.servicenow.com/resource/enus/infocard/third-party-llm.pdf)**

    Model used for AI-driven solutions for text generation, summarization, and conversational AI.

-   **[Model card for ServiceNow Voice AI Speech-to-Text and Text-to-Speech models](https://downloads.docs.servicenow.com/resource/enus/infocard/sn-voice.pdf)**

    Models used within ServiceNow AI Voice Agents for converting spoken user input to text and generating natural-sounding speech from AI responses.

-   **[Model card for ServiceNow Now Assist Guardian model](https://downloads.docs.servicenow.com/resource/enus/infocard/sn-na-guardian.pdf)**

    This model provides content moderation and helps identify different kinds of prompt injection attacks and offensive content.

-   **[Model card for ServiceNow Inferred CSAT and Factors large language model](https://downloads.docs.servicenow.com/resource/enus/infocard/csat-llm.pdf)**

    This model is designed to ingest a conversation and predict a CSAT score as well as factors that explain the predicted score.


## June 2026

The June release includes updates to third-party model defaults, a change to the default reasoning effort setting for GPT-5 Mini, and the retirement of the Now LLM long-term support \(LTS\) SKU.

-   Third-party default model version update: Teams that did not update their third-party default model versions to the latest available versions in the May release must do so in the June release. GAIC 13.1.2 is the required version for this update.

-   GPT-5 Mini: `reasoning_effort` default change: The default `reasoning_effort` setting for GPT-5 Mini has changed from `none` to `minimal`. This change is included in GAIC Snapshot 14.0.0, which is compatible with Now Assist for Platform 12.0.0.

    Teams using GPT-5 Mini should run regression and functional testing to confirm that the new default works as expected. If you explicitly set `reasoning_effort` in your generative AI config additional properties, smoke test to verify there are no unexpected effects. If you have `reasoning_effort: none` set in additional properties, update the value to `minimal` and run regression and functional testing.

-   Claude Sonnet 4.0 retirement: Claude Sonnet 4.0 references are being redirected on the backend. No team action is required.

    -   `claude_large` / Claude 4.0 Sonnet redirects to Claude 4.5 Sonnet
    -   `claude_small` / Claude 4.0 Sonnet redirects to Claude 4.5 Sonnet
-   Now LLM LTS SKU retired: ServiceNow no longer offers the LTS model SKU. There are no testing requirements or expectations for teams related to this retirement.


## May 2025

An advanced 12B general-purpose small language model \(SLM\) with a singular, high-performance architecture that supports a wide range of tasks in ServiceNow’s context was released. Fine-tuned on Mistral-Nemo-12B-Instruct, this model is designed and optimized for tasks like Agent Assist, Text-to-Flow, Text-to-Cypher, Safety &amp; Content Moderation and Text-to-Code.

Key Enhancements:

-   Enhanced instruction adherence: Improved the model’s capability to accurately interpret and follow user instructions, ensuring that the model can better understand and execute complex commands. Leading to more precise and reliable outcomes than previous releases.
-   Increased context window: increased context window from 16K to 32K, enabling the model to better understand long-form inputs, maintain coherence over extended interactions, and support more complex tasks with richer contextual awareness.
-   Improved multilingual proficiency: Boosted performance across languages compared to previous releases, with notable enhancements in Japanese processing.
-   Optimized for ServiceNow workflow related capabilities: Extended support coverage for Text-to-Flow, and improved the performance of Text-to-Code, Text-to-Cypher etc.
-   Continuously enhanced model deployment consolidation: Integrates ServiceNow-related tasks into a single model, reducing system complexity at the same time while elevating overall performance.

## March 2025

A powerful 12B general-purpose small language model \(SLM\) designed to enhance a wide range of applications, including text-to-code and agent use cases was released. Fine-tuned on Mistral-Nemo-12B, it streamlines deployment and consolidates multiple functionalities into a singular, architecture.

Key Enhancements:

-   Optimized to fulfill use cases: Enhances case summarization, chat summarization, resolution notes, and knowledge base generation across supported languages, including improvements in Japanese quality.
-   Superior text-to-code and text-to-cypher performance: Delivers major advancements in Glide JavaScript and generic JavaScript editing and generation, along with improved accuracy in query generation and execution for structured databases.
-   Robust content moderation and safety: Provides stronger protection against adversarial prompts, jail-breaking attempts, and harmful content generation, ensuring safer deployment with built-in content filtering.
-   Unified model deployment:integrates ServiceNow-related tasks into a single model, thereby reducing system complexity while elevating overall performance.
-   Improved instruction adherence: Delivers better instruction following and consistency across varying levels of prompt and instruction strictness than the current text-to-text NowLLM.

## November 2024

Several key improvements were added to the Now LLM Service that are aimed at enhancing performance and quality.

-   Multilingual support: Now LLM Service supports 8 additional languages, enabling global teams to use the model in their native languages.

    The supported languages are: English, German, French, Japanese, Dutch, French Canadian, Spanish, Brazilian Portuguese, and Italian.

-   JSON format support: The model now provides output in JSON format, making it easier for developers to integrate with various applications and automate workflows seamlessly.
    -   Deterministic responses: JSON mode ensures structured, consistent output, which improves predictability and reliability when integrating with applications.
    -   Error reduction: Unlike free-form text mode, JSON responses are less prone to format errors or stray characters, minimizing integration issues.
    -   Lower token consumption: The fixed structure of JSON can reduce token usage, making it more efficient and cost-effective for applications with high response frequency.
-   Improvements in instruction following: The model has been fine-tuned to understand and follow instructions more precisely. This enables the model to deliver more to-the-point and actionable responses, helping users get the information they need faster and more efficiently.

**Parent Topic:**[Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md)

