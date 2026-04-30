---
title: Exploring Generative AI Controller
description: Learn more about generative AI concepts and how to integrate third-party generative AI into the ServiceNow AI Platform to create content, summarize task records, and analyze user sentiment.
locale: en-US
release: yokohama
product: Generative AI Controller
classification: generative-ai-controller
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Generative AI Controller, Now Assist, Enable AI experiences]
---

# Exploring Generative AI Controller

Learn more about generative AI concepts and how to integrate third-party generative AI into the ServiceNow AI Platform to create content, summarize task records, and analyze user sentiment.

## Generative AI Controller overview

Complex algorithms and deep learning models learn patterns and use that knowledge to generate new outputs. With Generative AI Controller, you can generate content directly within the ServiceNow AI Platform.

Generative AI Controller integrates with external LLMs, including ones by OpenAI, Azure OpenAI, Google Cloud \(AI Studio and Vertex\), Aleph Alpha, IBM watsonx, and Amazon Bedrock. These capabilities are available in Workflow Studio flows, Virtual Agent topics, and scripting like background scripts and business rules.

## Generative AI Controller benefits

|Benefit|Feature|
|-------|-------|
|Generate text to summarize complex information.|Workflow Studio Actions to Generate Content and Summarize|
|Analyze user sentiment to identify and alleviate end-user concerns.|Sentiment Analysis Workflow Studio Action|
|Query a large language model \(LLM\) directly.|Generic Prompt Workflow Studio Action|
|Write scripts for AI model capabilities that are designed to increase the accuracy and scalability of your custom content.|Script with generative AI|
|Integrate with third-party AI service providers to customize your AI experience|OpenAI, Azure OpenAI, Google AI, Aleph Alpha, IBM watsonx, Amazon Bedrock|

## Get started with Generative AI Controller

-   The Generative AI Controller application is installed with any [Now Assist application](../../now-assist-platform/concept/platform-now-assist-landing.md).
-   Sign up and create an account with a generative AI provider.
    -   To sign up with OpenAI, go to their [official platform website](https://platform.openai.com/).
    -   To get started with Azure OpenAI, go to their [documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/quickstart).
    -   To start using AI Studio with Gemini API, go to the [AI Studio homepage](https://ai.google.dev/aistudio/).
    -   To use Vertex AI on the Google Cloud, go to the [Vertex AI homepage](https://cloud.google.com/vertex-ai).
    -   To get started with Aleph Alpha, go to [their website](https://app.aleph-alpha.com) and create an Aleph Alpha API account.
    -   To get started with IBM watsonx, go to [Getting started with IBM watsonx as a Service](https://www.ibm.com/docs/en/watsonx/saas?topic=getting-started).
    -   To get started with Amazon Bedrock, [set up an IAM user with the correct permissions](https://repost.aws/knowledge-center/create-access-key) and then [explore the Converse API](https://docs.aws.amazon.com/bedrock/latest/APIReference/API_runtime_Converse.html).
-   [Configure credentials for your preferred AI service provider](configuring-api-credentials-for-generative-ai-capabilities.md) for the Generative AI Controller capabilities.
-   Add Generative AI Controller capabilities to Virtual Agent Designer to start creating Virtual Agent topics with generative AI with your AI service provider.
-   Use Generative AI Controller with Virtual Agent Designer, Flow Designer, and scripts.

