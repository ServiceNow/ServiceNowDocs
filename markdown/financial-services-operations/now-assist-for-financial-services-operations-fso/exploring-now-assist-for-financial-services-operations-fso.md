---
title: Exploring Now Assist for Financial Services Operations \(FSO\)
description: With the Now Assist for Financial Services Operations \(FSO\) application, use AI skills and agentic AI to summarize case and customer details, enhance disputes intake with Disputes intake via Virtual Agent, and leverage agentic workflows and AI agents to automate dispute resolution.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI for FSO overview, generative AI for financial service operations overview, generative AI for financial service operations sensitive data handling]
breadcrumb: [Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Exploring Now Assist for Financial Services Operations \(FSO\)

With the Now Assist for Financial Services Operations \(FSO\) application, use AI skills and agentic AI to summarize case and customerdetails, enhance disputes intake with Disputes intake via Virtual Agent, and leverage agentic workflows and AI agents to automate dispute resolution.

## Overview of Now Assist for Financial Services Operations \(FSO\)

The following AI capabilities are available:

-   Summarize the details of a case for an insurance claim or a card dispute.
-   Use a Virtual Agent chatbot as part of the customer dispute intake flow. Card network and issuer policies are integrated in the chatbot conversation. Information on the dispute is gathered and inferred from the customer's responses and populated in case form fields.
-   Use agentic AI to assist dispute agents in handling transactions that are flagged as friendly fraud. The AI agent leverages the results from a friendly fraud detection tool to generate recommendations the appropriate action. If the transaction is rejected, it also helps draft a rationale to explain the decision to the end user.
-   Use AI agents and AI skills to support customer front-office interactions, and to discover customer insights.

For more information on generative AI skills, including case and customer profile summarization, see [Using generative AI in Now Assist for Financial Services Operations \(FSO\)](using-now-assist-for-financial-services-operations-fso.md).

For more information on AI agents and agentic workflows, see [Agentic AI use cases for FSO](../../fso-now-assist/concept/usecase-now-assist.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

## Now Assist panel in Financial Services Workspace

An agent can use the Now Assist panel in Financial Services Workspace for scenarios such as:

-   Case summarization
-   Conversational interaction for dispute resolution
-   Interacting with AI agents during interactions or customer analysis

For more information about the Now Assist panel, see Now Assist panel.

## Sensitive data handling

Personally identifiable information and other sensitive data can be masked so that it doesn't appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the Now LLM Service isn't exposed to any sensitive information. For more information, see .

**Important:** Exercise caution when using Now Assist for FSO with cases that contain sensitive data or other regulated workloads, such as healthcare claims. Now Assist for FSO should not be used for processing protected health information \(PHI\). When using Now Assist for FSO in a protected industry, validate and test the generated results in accordance with corresponding legislation and requirements. See [AI limitations](now-assist-for-financial-services-operations.md#id_jvg_1wv_lbc) for more information.

