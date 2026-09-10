---
title: AI capabilities in Field Service Management
description: Field Service Management includes generative and agentic AI capabilities, powered by ServiceNow Otto, that help agents, dispatchers, and managers close tasks faster and work more efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/exploring-now-assist-fsm.html
release: australia
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 7
breadcrumb: [Explore, Field Service Management]
---

# AI capabilities in Field Service Management

Field Service Management includes generative and agentic AI capabilities, powered by ServiceNow Otto, that help agents, dispatchers, and managers close tasks faster and work more efficiently.

## AI plugins for Field Service Management

ServiceNow AI Platform and the ServiceNow Otto for Field Service Management \(FSM\) plugin \(sn\_fsm\_gen\_ai\) provide AI capabilities for Field Service Management workflows.

The ServiceNow® large language model \(Now LLM Service\) is currently the only provider for ServiceNow Otto for FSM skills.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Generative AI skills

|Benefit|Feature|Used with|
|-------|-------|---------|
|Close tasks faster by generating a summary from work order task information.|[Generate a work order task summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/close-wo-wot-mobile.md)|ServiceNow Agent \(mobile\)|
|Generate closure notes directly on mobile when closing a task.|[Generate work order task closure summaries in ServiceNow Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/close-wo-wot-mobile.md)|ServiceNow Agent \(mobile\)|
|Summarize a Sidebar discussion and save it to work notes.|[Summarize a Sidebar discussion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/na-fsm-summarize-sidebar-platform.md)|Web interface|
|Summarize a Sidebar discussion and save it to work notes, from the mobile app.|[Summarize a Sidebar discussion on the ServiceNow Agent application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/na-fsm-summarize-sidebar-mobile.md)|ServiceNow Agent \(mobile\)|
|Generate a knowledge article automatically from a closed work order task.|[Generate knowledge article with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/na-fsm-generate-kb-article.md)|Web interface|
|Get an immediate summary of a record without reviewing multiple related records.|[Summarize a record using ServiceNow Otto in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/summarize-a-record-using-now-assist-virtual-agent.md)|ServiceNow Agent \(mobile\)|
|Search technical documentation conversationally while in the field.|[Use conversational search for technician support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/access-information-you-need-mobile.md)|ServiceNow Agent \(mobile\)|
|Automatically fill form fields using image capture.|[ServiceNow AI Lens form auto-filler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/c_form-auto-filler-fsm.md)|ServiceNow Agent \(mobile\)|

## Agentic AI

|Benefit|Feature|Used with|
|-------|-------|---------|
|Create a work order using text or an image instead of filling out a form manually.|[Create a work order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/create-work-order-now-assist-fsm.md)|Web interface|
|Create a work order using text or an image, from the mobile app.|[Create a work order on the ServiceNow Agent mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/create-work-order-mobile-now-assist-fsm.md)|ServiceNow Agent \(mobile\)|
|Automatically track and validate parts usage when closing a work order task.|[Validate parts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/validate-parts-now-assist-fsm.md)|Web interface|
|Automatically track and validate parts usage when closing a work order task, from the mobile app.|[Validate parts on the ServiceNow Agent mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/close-wo-wot-mobile.md)|ServiceNow Agent \(mobile\)|

To install and set up AI agents on your instance, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md) and [Set up AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-na-aia.md).

**Note:**

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

**Important:** By default, all agentic workflows and AI agent records are read only.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

## Availability

**Important:** Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Please check for availability updates in future releases.

**Important:** Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.

## What to do next

Install and configure the AI plugin to enable generative and agentic AI features for Field Service Management. For more information, see [Configure ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/configure-now-assist-fsm.md) and [Configuring Field Service Virtual Agent Conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/mobile-experience-for-field-service-management-glide-family/fsm-va-conversation.md).

## Troubleshoot and get help

-   [ServiceNow Community AI &amp; Intelligence](https://www.servicenow.com/community/ai-intelligence/ct-p/ai-intelligence)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect task data \(for Case Assist\) and chat transcripts \(for Chat Assist\). Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

