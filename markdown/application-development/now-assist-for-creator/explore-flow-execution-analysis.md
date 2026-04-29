---
title: Explore flow execution analysis
description: Summarize flow execution details and get recommendations to resolve errors with generative AI.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Flow execution analysis, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Explore flow execution analysis

Summarize flow execution details and get recommendations to resolve errors with generative AI.

## Activation

The flow summarization skill is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

Enable flow execution analysis to gain these benefits.

-   Summarize flow execution details when flow reporting is off.
-   Identify potential causes of flow errors.
-   Resolve flow errors with suggested fixes.

## Supported LLMs

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Flow analysis

![Flow execution analysis sidebar option.](../images/flow-execution-analysis-animated.gif)

You can generate and view a flow execution analysis from the Workflow Studio sidebar.

![Flow execution analysis sidebar option.](../images/flow-execution-analysis-01.png)

From the Analysis sidebar, you can generate an analysis of the flow execution details. A flow that has never been analyzed displays a **Analyze flow** button.

![Analyze flow option.](../images/flow-execution-analysis-02.png)

An existing flow analysis lists its creation date.

![A summary of the Change - Standard flow, which also lists a creation date.](../images/flow-execution-analysis-03.png)

You can regenerate a flow execution analysis from the Analysis sidebar.

## Flow reporting requirements

Flow execution analysis requires flow execution details to analyze. When flow reporting is on, you can analyze any flow using information from its flow execution details. When flow reporting is off, you can only analyze flows that are in an error state using information from the flow context record. For more information about setting flow reporting, see [Activate flow reporting](https://www.servicenow.com/docs/access?context=enable-flow-reporting&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

**Parent Topic:**[Flow execution analysis](../reference/flow-execution-analysis-landing.md)

