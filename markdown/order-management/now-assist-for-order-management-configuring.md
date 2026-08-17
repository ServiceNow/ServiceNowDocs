---
title: Configuring ServiceNow Otto for Order Management
description: If you have the admin role, you can configure the ServiceNow Otto for Order Management application so that your agents can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/now-assist-for-order-management-configuring.html
release: zurich
topic_type: concept
last_updated: "2026-01-13"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Otto for Order Management]
---

# Configuring ServiceNow Otto for Order Management

If you have the admin role, you can configure the ServiceNow Otto for Order Management application so that your agents can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.

Installing the ServiceNow Otto for Order Management application installs the following AI applications and skills on your ServiceNow instance:

-   Manage Order Operations \(com.sn\_ord\_ops\_aias\)
-   Manage Invoice Operations \(com.sn\_inv\_ops\_aias\)
-   Summarization for Order Management

Request the ServiceNow Otto for Order Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/b75a55a63f71b6108428dd8d001f8bca) and install it using the Application Manager. For more information, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_InstallApplications.md).

## Configuring order summarization skill

The AI skills for Sales CRM:

-   Order summarization for order capture
-   Order summarization for order fulfillment

For information on customizing the order summarization skill, see [Customize an order summarization skill in ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/customize-order-summarization-skill-now-assist-order-management.md).

**Note:** Microsoft Azure, Amazon bedrock, Now LLM, Now LLM LTS, and Google Cloud vertex AI are currently the providers for this ServiceNow Otto application's skills.

## Configuring the Manage Order Operations application

Business-to-business \(B2B\) customers can submit order cases using ServiceNow Otto Virtual Agent from the Business Portal. Interaction channels include chat and voice options. Before you can use the AI agents for managing order operations from the Business Portal:

-   [Enable the manage order operations agent on Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/enable-manage-order-operations-ai-agent.md)
-   [Configure scripted extension points for the manage order operations AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/create-atp-api-call.md)
-   [Email notifications for order cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/order-case-email-notifications.md)

Enable AI voice agent support on your phone channels by installing the ServiceNow Otto Voice \[sn\_voice\_aia\] plugin. For more information, see [Deploy AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/deploy-ai-agents-for-voice.md).

Configure Chat Summarization to enable the AI summarization and recommendation features in Active Chat. For more information, see [Configure chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-chat-summarization-in-now-assist_0.md).

## Configuring the Manage Invoice Operations application

Business-to-business \(B2B\) customers can submit invoice cases using ServiceNow Otto Virtual Agent from the Business Portal. Interaction channels include chat and voice options. Billing specialists and agents can use the invoice dispute assist agentic workflow from the CSM/FSM Configurable Workspace to resolve invoice cases. Before you can use the AI agents for managing order operations agent in the Business Portal:

-   [Configure AI-assisted invoice dispute intake on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/enable-manage-invoice-operations-ai-agent.md)
-   [Configure the invoice quantity validation extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configure-invoice-quantity-check-ep.md)
-   [Configure the invoice dispute resolution extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configure-invoice-case-resolution-ep.md)
-   [Make the invoice dispute assist workflow available in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/enable-invoice-dispute-assist-agentic-workflow.md)

Enable AI voice agent support on your phone channels by installing the ServiceNow Otto Voice \[sn\_voice\_aia\] plugin. For more information, see [Deploy AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/deploy-ai-agents-for-voice.md).

Configure Chat Summarization to enable the AI summarization and recommendation features in Active Chat. For more information, see [Configure chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-chat-summarization-in-now-assist_0.md).

**Related topics**  


[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-na-landing.md)

[Using ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/now-assist-order-management-using.md)

