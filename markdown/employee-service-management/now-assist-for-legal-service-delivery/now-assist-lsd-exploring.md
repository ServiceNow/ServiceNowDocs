---
title: Explore Now Assist for Legal Service Delivery \(LSD\)
description: With the Now Assist for Legal Service Delivery \(LSD\) application, request fulfillers can use generative AI to summarize a legal request or legal matter. Request fulfillers or legal users can also generate actionable answers from knowledge article search results in Employee Center, Legal Counsel Center, and global search.
locale: en-US
release: yokohama
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Explore Now Assist for Legal Service Delivery \(LSD\)

With the Now Assist for Legal Service Delivery \(LSD\) application, request fulfillers can use generative AI to summarize a legal request or legal matter.Request fulfillers or legal users can also generate actionable answers from knowledge article search results in Employee Center, Legal Counsel Center, and global search.

## Now Assist for Legal Service Delivery \(LSD\) overview

The following generative AI capabilities are available in Now Assist for Legal Service Delivery \(LSD\):

-   Summarization capability for the request fulfillers to get a concise summary of a request or matter. This generative AI summary enables a request fulfiller to understand the context of the request so that they can close the request or matter more quickly. The summarization capability is available in Legal Counsel Center as well as the Now Assist panel.
-   Q&amp;A Genius Results capability for request fulfillers and legal users to generate concise, actionable answers from knowledge article results in Legal Counsel Center, Employee Center, and global search.

## Legal Request and Legal Matter summarization skills

The Now Assist for Legal Service Delivery \(LSD\) application provides an AI-generated summary of the legal request or matter. The summary includes the request or matter details and the actions that were taken for this request or matter. A request fulfiller can view this summary to understand the context, refresh the summary, and post the summary to the work notes.

The summary is displayed above the activity stream and includes the information from the fields and variablesconfigured as inputs.![Legal matter summarization](../image/lsd-sum-matter-landing.png)

For more information on the fields and variables that are considered for summarization, see [Skill inputs for Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-skill-inputs.md) and [Configure variables for Now Assist summarization](../task/configure-variables-for-now-assist-summarization.md).

For information on activating the Legal Request summarization skill or the Legal Matter summarization skill, see [Configure Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-configuring.md). For information on how to use the skills on Legal Counsel Center, see [Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)](../task/now-assist-lsd-summarize-case.md).

## Q&amp;A Genius Results

Q&amp;A Genius Results use the Now LLM Service to generate search results from knowledge article results in Employee Center, Legal Counsel Center, and global search.

The Q&amp;A Genius Result answer card shows a topic snippet and an answer snippet that was extracted from a knowledge article. You can view the full article directly from the answer card. For more information, see [Genius Results](https://www.servicenow.com/docs/access?context=genius-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

It is enabled when both AI Search and Now Assist for Legal Service Delivery \(LSD\) are activated.

![Q&A Genius search results in Legal Counsel Center.](../image/lsd-na-genius-result.png)

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Now Assist for Legal Service Delivery \(LSD\) users

<table id="table_ns3_1vj_qcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator\[sn\_lg\_gen\_ai.admin\]

</td><td>

Provides administrative access to Now Assist for Legal Service Delivery \(LSD\).Installs Now Assist for Legal Service Delivery \(LSD\) plugin, and activates the required skills.

</td></tr><tr><td>

Request Fulfiller\[sn\_lg\_gen\_ai.request\_fulfiller\]

</td><td>

Provides access for users to utilize skill for legal requests provided via Now Assist for Legal Service Delivery \(LSD\).

</td></tr><tr><td>

Matter Fulfiller\[sn\_lg\_gen\_ai.matter\_fulfiller\]

</td><td>

Provides access for users to utilize skill for legal matters provided via Now Assist for Legal Service Delivery \(LSD\).

</td></tr></tbody>
</table>-   **[Supporting information for Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-support-info.md)**  
Get a quick overview of the important information that is related to the Now Assist for Legal Service Delivery \(LSD\) application.

**Parent Topic:**[Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-landing.md)

