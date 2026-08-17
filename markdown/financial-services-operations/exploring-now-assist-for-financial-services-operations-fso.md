---
title: AI in Financial Services Operations
description: Financial Services Operations has AI skills and agentic AI to support front and back office tasks. Users can summarize case and customer details, enhance disputes intake with Disputes intake via Virtual Agent, and use agentic workflows and AI agents to automate dispute resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/exploring-now-assist-for-financial-services-operations-fso.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [generative AI for FSO overview, generative AI for financial service operations overview, generative AI for financial service operations sensitive data handling]
breadcrumb: [Explore, Financial Services Operations \(FSO\)]
---

# AI in Financial Services Operations

Financial Services Operations has AI skills and agentic AI to support front and back office tasks. Users can summarize case and customer details, enhance disputes intake with Disputes intake via Virtual Agent, and use agentic workflows and AI agents to automate dispute resolution.

## Overview of AI capabilities in FSO

Use AI in FSO to do the following:

-   Summarize the details of a case for an insurance claim or a card dispute.
-   Use a Virtual Agent chatbot as part of the customer dispute intake flow. Card network and issuer policies are integrated in the chatbot conversation. Information on the dispute is gathered and inferred from the customer's responses and populated in case form fields.
-   Use agentic AI to assist dispute agents in handling transactions that are flagged as friendly fraud. The AI agent leverages the results from a friendly fraud detection tool to generate recommendations the appropriate action. If the transaction is rejected, it also helps draft a rationale to explain the decision to the end user.
-   Use AI agents to resolve ACH dispute cases.
-   Use AI agents and AI skills to support customer front-office interactions, and to discover customer insights.

For a full list of all AI skills, AI agents, and agentic workflows in FSO, see [AI capabilities in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/ai-capabilities-in-fso.md).

Other AI features and skills are also available in ServiceNow Otto and ServiceNow Otto for Customer Service Management. For more information, see [Enable AI experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-products.md) and .

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Sensitive data handling and masking

Personally identifiable information and other sensitive data can be masked so that it doesn't appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the LLM provider isn't exposed to any sensitive information. For more information, see .

**Important:** Exercise caution when using ServiceNow Otto with cases that contain sensitive data or other regulated workloads, such as healthcare claims. ServiceNow Otto should not be used for processing protected health information \(PHI\). When using ServiceNow Otto in a protected industry, validate and test the generated results in accordance with corresponding legislation and requirements. See [AI limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/exploring-now-assist-for-financial-services-operations-fso.md) for more information.

## Federal exclusion notice

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products.Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

