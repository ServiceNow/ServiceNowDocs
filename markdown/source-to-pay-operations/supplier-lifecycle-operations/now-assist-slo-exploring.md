---
title: Explore ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)
description: With the ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) application, supplier managers can summarize the details of supplier-related cases to keep them informed about their progress and action items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-exploring.html
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [ServiceNow Otto for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Explore ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)

With the ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) application, supplier managers can summarize the details of supplier-related cases to keep them informed about their progress and action items.

## Overview of ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)

With ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) skills, supplier managers can generate summary of supplier cases and supplier's KPI performance. The Supplier case summarization skill provides supplier managers a concise overview of the case, actions completed so far, and the next steps that need to be taken. The Supplier performance summarization skill helps the supplier managers know the overall supplier performance score, trend, performance details, historical context, and next steps.

ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) includes the following capabilities:

-   Supplier case summarization provides supplier managers a summary of the supplier-related cases. This enables them to quickly assess the status of any case in the supply process and take the necessary actions.
-   Supplier performance summarization provides supplier managers a complete KPI performance summary, including overall performance scores, and trends.
-   Sentiment Analysis helps reduce escalated cases by providing agents with the current sentiment on a case, based on interactions and the latest trends. It also offers insights into why the sentiment is what it is today.
-   Email response generation generates contextually relevant email responses by analyzing case and task details.

\[Omitted image "now-assist-slo-skills.png"\] Alt text: Now Assist skills for Supplier Lifecycle Operations

**Note:**

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md).

## Skills

The ServiceNow Otto for SLO application includes generative AI skills and features that enable supplier managers to summarize the supplier-related cases within the Source-to-Pay Workspace.

-   **Supplier case summarization**

    Provides supplier managers a summary of the supplier-related cases. Supplier managers can see the status of any case in the supply process and take the necessary actions quickly. Supplier managers can also refresh and post the summary to the work notes or activity stream.

    Fulfillers can customize prompt configuration and prompt optimization using the preprocessor in the AI Skill kit. The skill supports multiple models such as status of any case in the supp. To customize the prompt instructions, sn\_skill\_builder\_admin role is mandatory.

    For more information about how to summarize a case, see [Summarize a case by using ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) in Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-summarize-case.md).

-   **Supplier performance summarization**

    Provides supplier managers the complete KPI performance summary including overall performance scores, trends, and action items.

    For more information about how to summarize a supplier's performance, see [Summarize supplier performance in Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/summarize-supp-perf.md).

-   **Sentiment Analysis for supplier case**

    The Sentiment Analysis skill analyzes requester's responses and determines the overall sentiment associated with a supplier case. The sentiment and sentiment trend help you gauge the urgency of a case. They indicate whether the requester's tone is improving, worsening, or remaining consistent over time. For more information, see [Analyze sentiments in supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/slo-analyze-sentiments.md).

-   **Email response for supplier case**

    The Email response for supplier case skill generates contextually relevant email responses. It analyzes case details such as case type, short description, description, work notes, activity stream, additional comments, related records, and relevant knowledge base articles. Use this skill to draft, adjust the tone, shorten, or elaborate email responses, reducing the time spent on manual email composition. You can also use predefined templates to maintain consistency in your email responses. For more information, see [Generate an email response for supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/generate-email-response-for-supplier-case.md).

-   **Email response for supplier task**

    The Email response for supplier task skill generates contextually relevant email responses. It analyzes task details such as case type, short description, description, work notes, activity stream, additional comments, related records, and relevant knowledge base articles. Use this skill to draft, adjust the tone, shorten, or elaborate email responses, reducing the time spent on manual email composition. You can also use predefined templates to maintain consistency in your email responses. For more information, see [Generate an email response for supplier tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/generate-email-response-for-supplier-tasks.md).


To learn how to configure ServiceNow Otto for SLO, see [Configure ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-configuring.md).

To learn more about how to use ServiceNow Otto for SLO, see [Use ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-using.md).

**Related topics**  


[Supporting information for ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-supporting-info.md)

[Configure ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-configuring.md)

[Use ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-using.md)

