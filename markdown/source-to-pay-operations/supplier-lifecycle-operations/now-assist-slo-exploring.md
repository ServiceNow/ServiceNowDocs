---
title: Explore Now Assist for Supplier Lifecycle Operations \(SLO\)
description: With the Now Assist for Supplier Lifecycle Operations \(SLO\) application, supplier managers can summarize the details of supplier-related cases to keep them informed about their progress and action items.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Now Assist for Supplier Lifecycle Operations \(SLO\), Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Explore Now Assist for Supplier Lifecycle Operations \(SLO\)

With the Now Assist for Supplier Lifecycle Operations \(SLO\) application, supplier managers can summarize the details of supplier-related cases to keep them informed about their progress and action items.

## Overview of Now Assist for SLO

With Now Assist for Supplier Lifecycle Operations \(SLO\) skills, supplier managers can generate summary of supplier cases and supplier's KPI performance. The Supplier case summarization skill provides supplier managers a concise overview of the case, actions completed so far, and the next steps that need to be taken. The Supplier performance summarization skill helps the supplier managers know the overall supplier performance score, trend, performance details, historical context, and next steps.

Now Assist for Supplier Lifecycle Operations \(SLO\) includes the following capabilities:

-   Supplier case summarization provides supplier managers a summary of the supplier-related cases, enabling them to quickly assess the status of any case in the supply process and take the necessary actions.
-   Supplier performance summarization provides supplier managers a complete KPI performance summary, including overall performance scores, and trends.
-   Sentiment Analysis helps reduce escalated cases by providing agents with the current sentiment on a case, based on interactions and the latest trends. It also offers insights into why the sentiment is what it is today.
-   Email response generation generates contextually relevant email responses by analyzing case and task details.

![Now Assist skills for Supplier Lifecycle Operations](../image/now-assist-slo-skills.png "Now Assist skills for SLO")

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Skills

The Now Assist for SLO application includes generative AI skills and features that enable supplier managers to summarize the supplier-related cases within the Source-to-Pay Workspace.

-   **Supplier case summarization**

    Provides supplier managers a summary of the supplier-related cases. Supplier managers can see the status of any case in the supply process and take the necessary actions quickly. Supplier managers can also refresh and post the summary to the work notes or activity stream.

    Fulfillers can customize prompt configuration and prompt optimization using the preprocessor in the Now Assist Skill kit \(NASK\). The skill supports multiple models such as OpenAI, Claude, Gemini, Now LLM. To customize the prompt instructions, sn\_skill\_builder\_admin role is mandatory.

    For more information about how to summarize a case, see [Summarize a case by using Now Assist for Supplier Lifecycle Operations \(SLO\) in Source-to-Pay Workspace](../task/now-assist-slo-summarize-case.md).

-   **Supplier performance summarization**

    Provides supplier managers the complete KPI performance summary including overall performance scores, trends, and action items.

    For more information about how to summarize a supplier's performance, see [Summarize supplier performance in Source-to-Pay Workspace](../task/summarize-supp-perf.md).

-   **Sentiment Analysis for supplier case**

    The Sentiment Analysis skill analyzes requester's responses and determines the overall sentiment associated with a supplier case. The sentiment and sentiment trend generated helps you gauge the urgency of a supplier case by indicating whether the requester's tone is improving, worsening, or remaining consistent over time. For more information, see [Analyze sentiments in supplier cases](../task/slo-analyze-sentiments.md).

-   **Email response for supplier case**

    The Email response for supplier case skill generates contextually relevant email responses by analyzing case details such as case type, short description, description, work notes, activity stream, additional comments, related records, and relevant knowledge base articles. Use this skill to draft, adjust the tone, shorten, or elaborate email responses, reducing the time spent on manual email composition. You can also use predefined templates to maintain consistency in your email responses. For more information, see [Generate an email response for supplier cases](../task/generate-email-response-for-supplier-case.md).

-   **Email response for supplier task**

    The Email response for supplier task skill generates contextually relevant email responses by analyzing task details such as case type, short description, description, work notes, activity stream, additional comments, related records, and relevant knowledge base articles. Use this skill to draft, adjust the tone, shorten, or elaborate email responses, reducing the time spent on manual email composition. You can also use predefined templates to maintain consistency in your email responses. For more information, see [Generate an email response for supplier tasks](../task/generate-email-response-for-supplier-tasks.md).


To learn how to configure Now Assist for SLO, see [Configure Now Assist for Supplier Lifecycle Operations \(SLO\)](../task/now-assist-slo-configuring.md).

To learn more about how to use Now Assist for SLO, see [Use Now Assist for Supplier Lifecycle Operations \(SLO\)](now-assist-slo-using.md).

**Related topics**  


[Supporting information for Now Assist for Supplier Lifecycle Operations \(SLO\)](now-assist-slo-supporting-info.md)

[Configure Now Assist for Supplier Lifecycle Operations \(SLO\)](../task/now-assist-slo-configuring.md)

[Use Now Assist for Supplier Lifecycle Operations \(SLO\)](now-assist-slo-using.md)

