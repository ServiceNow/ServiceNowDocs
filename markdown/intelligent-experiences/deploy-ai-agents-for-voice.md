---
title: Deploy AI voice agents
description: AI voice agents are generative AI-powered agents that bring natural, conversational experiences to phone-based support. As part of the broader AI agent ecosystem, they connect with telephony providers to replace rigid menu trees with seamless and human-like interactions that make support faster and more intuitive.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Deploy AI voice agents

AI voice agents are generative AI-powered agents that bring natural, conversational experiences to phone-based support. As part of the broader AI agent ecosystem, they connect with telephony providers to replace rigid menu trees with seamless and human-like interactions that make support faster and more intuitive.

## AI voice agents overview

AI voice agents use generative AI to deliver natural, dynamic conversations that help users complete tasks, resolve issues, and access information—anytime, anywhere.

AI voice agents are part of the ServiceNow AI Platform capabilities and can be deployed from the base system or customized to meet specific business needs. AI voice agents are managed through the AI Agent Studio, which provides tools for creating, deploying, and monitoring AI voice agents.

AI voice agents are associated with voice assistants, which act as a virtual help desk. A voice assistant can host multiple AI voice agents. Each AI voice agent is equipped with specific AI instructions, tools, and knowledge to resolve user issues. You can configure welcome messages, select voice profiles from the voice library, and define fallback options like live agent routing or record producer-based ticket creation.

**Note:** AI voice agents support the following LLMs: Azure OpenAI, Google Gemini, and AWS Claude. Now LLM Service is also supported but limited to English language only.

## Deploying AI voice agents

To get started with AI voice agents, perform the following steps.

1.  [Install Now Assist AI voice agents](../task/install-ai-voice-agents-plugins.md)
2.  [Configure user identification and authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.md)
3.  [Create an AI voice assistant](create-an-ai-voice-service.md)
4.  [Create an AI voice agent](create-a-voice-enabled-ai-agent.md)
5.  [Test AI voice agents](test-ai-voice-agents.md)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](../../now-assist-admin/task/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](../../now-assist-platform/concept/platform-now-assist-landing.md).

## Privacy notice

By using this feature, you confirm that your use \(including use by your service providers\) complies with relevant anti-wiretapping, recording consent, and other privacy laws, as applicable.

**Related topics**  


[HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-voice-ai-agents.md)

[Agentic AI in the Voice application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-voice.md)

