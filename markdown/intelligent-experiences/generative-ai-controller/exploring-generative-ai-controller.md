---
title: Exploring Generative AI Controller
description: Learn how Generative AI Controller works as the control and visibility layer for all generative AI requests across your ServiceNow applications, what it controls, and how it integrates with third-party LLM providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/exploring-generative-ai-controller.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Exploring Generative AI Controller

Learn how Generative AI Controller works as the control and visibility layer for all generative AI requests across your ServiceNow applications, what it controls, and how it integrates with third-party LLM providers.

## Generative AI Controller overview

Every AI request from generative AI features, AI agents, and custom skills passes through Generative AI Controller before reaching your LLM provider. The controller enforces governance policies, applies privacy controls, and records activity for monitoring and troubleshooting.

Generative AI Controller integrates with external LLMs, including ones by OpenAI, Azure OpenAI, Google Cloud \(AI Studio and Vertex\), IBM watsonx, and Amazon Bedrock.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Generative AI Controller governance and controls

Generative AI Controller manages the following controls for generative AI activity across your ServiceNow applications:

-   **Logging**

    Records all generative AI requests and responses for debugging and auditing.

-   **Rate limiting**

    Restricts the number of requests to an LLM provider within a given time frame.

-   **Data privacy**

    Masks personally identifiable information in prompts before they are sent to an LLM.

-   **External LLM connectivity**

    Connects your Now Assist applications to a third-party LLM provider.

-   **Guardian guardrails**

    Applies content and safety policies to generative AI requests.


## Generative AI Controller benefits

|Benefit|Feature|
|-------|-------|
|Integrate with third-party AI service providers to customize your AI experience|OpenAI, Azure OpenAI, Google AI, IBM watsonx, Amazon Bedrock|
|Govern and monitor all generative AI activity in your ServiceNow applications|Data Privacy, Guardian guardrails, [Rate limiting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configure-rate-limit.md), and Activity logging|
|Use your own API keys for AI processing|[Bring your own key for third-party AI provider integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/byok-for-azure-open-ai.md)|

## Get started with Generative AI Controller

-   The Generative AI Controller application is installed automatically with any [ServiceNow AI application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).
-   Sign up and create an account with a generative AI provider.
    -   To sign up with OpenAI, go to their [official platform website](https://platform.openai.com/).
    -   To get started with Azure OpenAI, go to their [documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/quickstart).
    -   To start using AI Studio with Gemini API, go to the [AI Studio homepage](https://ai.google.dev/aistudio/).
    -   To use Vertex AI on the Google Cloud, go to the [Vertex AI homepage](https://cloud.google.com/vertex-ai).
    -   To get started with IBM watsonx, go to [Getting started with IBM watsonx as a Service](https://www.ibm.com/docs/en/watsonx/saas?topic=getting-started).
    -   To get started with Amazon Bedrock, [set up an IAM user with the correct permissions](https://repost.aws/knowledge-center/create-access-key) and then [explore the Converse API](https://docs.aws.amazon.com/bedrock/latest/APIReference/API_runtime_Converse.html).
-   [Configure credentials for your preferred AI service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configuring-api-credentials-for-generative-ai-capabilities.md) for the Generative AI Controller capabilities.
-   Activate AI assets for your workflows and configure governance settings such as data privacy, guardrails, and [rate limiting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configure-rate-limit.md).
-   Build custom skills for your organization's unique requirements using [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).
-   [Monitor generative AI activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/generative-ai-controller-tables.md) through logs for troubleshooting and compliance.

