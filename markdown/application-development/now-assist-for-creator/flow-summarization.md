---
title: Exploring Flow summarization
description: Summarize what a flow or subflow does by using generative AI.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Flow summarization, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Exploring Flow summarization

Summarize what a flow or subflow does by using generative AI.

## Activation

The flow summarization skill is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

Enable flow summarization to gain these benefits.

-   Enhance collaboration by describing what a flow does.
-   Reduce manual effort to generate flow details.

## Supported LLMs

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Flow summaries

![Flow summary option from the Flow context menu.](../images/flow-summary-01.png)

You can generate and view flow summaries from the More Actions menu.

![The Flow summary dialog box has a Summarize button.](../images/flow-summary-02.png)

From the Flow summary dialog box, you can generate a new flow summary or view any previously generated summary. A flow that has never been summarized displays a **Summarize** button.

![A summary of the Change - Standard flow, which also lists a creation date.](../images/flow-summary-03.png)

An existing flow summary lists its creation date. You can regenerate a flow summary from the Flow summary dialog box.

## Subflow summaries

![Subflow summary option from the Flow context menu.](../images/subflow-summary-01.png)

You can generate and view subflow summaries from the More Actions menu.

![The Subflow summary dialog box has a Summarize button.](../images/subflow-summary-02.png)

From the Subflow summary dialog box, you can generate a new subflow summary or view any previously generated summary. A subflow that has never been summarized displays a **Summarize** button.

![A summary of the Change - Implementation tasks subflow, which also lists a creation date.](../images/subflow-summary-03.png)

An existing subflow summary lists its creation date. You can regenerate a subflow summary from the Subflow summary dialog box.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

**Parent Topic:**[Flow summarization](../reference/flow-summarization-landing.md)

