---
title: Exploring ServiceNow Otto for Public Sector Digital Services \(PSDS\)
description: With the ServiceNow Otto for Public Sector Digital Services \(PSDS\) application, your agents can use AI capabilities to perform various tasks on a government service case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/now-assist-psds-exploring.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [ServiceNow Otto for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Exploring ServiceNow Otto for Public Sector Digital Services \(PSDS\)

With the ServiceNow Otto for Public Sector Digital Services \(PSDS\) application, your agents can use AI capabilities to perform various tasks on a government service case.

**Important:** Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.

## Features

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

The ServiceNow Otto for PSDS application includes the following AI features that enable your agents to work through cases.

-   **Investigative case summarization skill**

    Synthesizes case narratives, entities, evidence, and activity into a structured summary, enabling agents to grasp case context and respond to inquiries. Generates detailed resolution information for investigative outcomes, allowing agents to propose solutions and integrate generated information into the case record.

-   **Investigative case narrative refinement \(via ServiceNow Otto Context Menu\)**

    Reviews text and surfaces gaps, inconsistencies, and tone issues before a case narrative is submitted for supervisory review. Delivers real-time refinement suggestions grounded in linked entities, evidence, and case activity, leaving investigators with full control over accepting, rejecting, or editing every suggestion.

-   **Document screening skill**

    Review and validate uploaded documents autonomously, checking IDs, tax forms, and other supporting documents. This skill flags potential issues and surfaces key details, applying consistent validation logic across every submission.

-   **Government case summarization skill**

    Condenses comprehensive case records into concise summaries, including the issue and the actions taken, enabling agents to grasp case contexts and respond effectively to inquiries. Generates detailed resolution information for specific government case types, allowing agents to propose solutions to constituents or business contacts and integrate this information into the case record.

    The case summarization skill generates a case summary and displays it above the activity stream. The summary includes the information that the agent enters in the following case record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Email
    -   Service level agreement \(SLA\)
    \[Omitted image "psds-otto-case-summary.png"\] Alt text: AI-generated summary for a case record.

-   **Chat summarization skill**

    Automatically generate summaries of agent-facing chats. The summaries capture the context of conversations between agents and constituents or virtual agents at different points of the handoff. For example, summaries are generated when a Virtual Agent chat history is handed off to a live agent. Summaries are also generated when one live agent hands off a chat history with a customer to another live agent. Critical information from interactions is readily accessible for future reference and action.

-   **ServiceNow Otto for AI Search**

    use single-turn capabilities for legislation and policy summarization, providing agents with succinct overviews of complex documents and enhancing the ability to navigate and comprehend extensive legislative materials. This skill provides actionable AI-generated or AI-selected answers in searches, synthesizing and summarizing information from multiple knowledge bases to deliver relevant answers in a conversational format​.

-   **Fee waiver AI Agent skill**

    Determines the fee breakdown for an information request. The skill provides a subtotal fee estimate and a recommendation for whether a fee waiver request should be approved or rejected, including reasons for any rejection. It also provides a total fee estimate with the fee waiver, if applicable. This skill works via the Information Request Fee Estimation AI Agent to provide an autonomous decision based on guidelines added in a specific knowledge article. For information on standalone AI agents in Public Sector, see .


**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Tiers

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

-   Foundation: AI basics to deliver insights
-   Advanced: AI to boost productivity across relevant use cases
-   Prime: Act autonomously with all AI assets, and create your own

For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

For information about AI assets that are available on the ServiceNow AI Platform, see the following topics:

-   [Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills.md)
-   [Agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-aia-use-cases-list.md)

## ServiceNow Otto panel in CSM Configurable Workspace

An agent can use the ServiceNow Otto panel in CSM Configurable Workspace. This conversational interface enables an agent to request a case summary and generate the case resolution notes. For more information about the ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

**Important:** Some generative AI skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install an AI product, designated generative AI skills, AI agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The AI plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## ServiceNow Otto in AI Search

The ServiceNow Otto in AI Search application uses Now LLM Service to extract actionable Q&amp;A Genius Result answers from the knowledge articles that are found in Service Portal, Virtual Agent, Employee Center, and global searches. By using this application, an agent can improve the customer's experience by retrieving the relevant content from the knowledge base and generating concise answers. For more information, see [ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/now-assist-ais.md).

## Sensitive data handling

Personally identifiable information and other sensitive data is masked so that it does not appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the Now LLM Service is not exposed to any sensitive information. For more information, see Multi-turn catalog ordering.

## Troubleshoot and get help

-   [ServiceNow Community on AI and Intelligence](https://www.servicenow.com/community/ai-intelligence-articles/tkb-p/ai-platform-kb)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect case information \(for case summarization\). Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

**Related topics**  


[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)

[Configure ServiceNow Otto for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-psds-configuring.md)

[Using generative AI with ServiceNow Otto for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-psds-using.md)

[Exploring AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md)

