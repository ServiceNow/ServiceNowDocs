---
title: Configuring Now Assist for Order Management
description: If you have the admin role, you can configure the Now Assist for Order Management application so that your agents can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-01-13"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist for Order Management]
---

# Configuring Now Assist for Order Management

If you have the admin role, you can configure the Now Assist for Order Management application so that your agents can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.

Installing the Now Assist for Order Management application installs the following AI applications and skills on your ServiceNow instance:

-   Manage Order Operations \(com.sn\_ord\_ops\_aias\)
-   Manage Invoice Operations \(com.sn\_inv\_ops\_aias\)
-   Summarization for Order Management

Request the Now Assist for Order Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/b75a55a63f71b6108428dd8d001f8bca) and install it using the Application Manager. For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Configuring order summarization skill

The Now Assist skills for Sales CRM:

-   Order summarization for order capture
-   Order summarization for order fulfillment

For information on customizing the order summarization skill, see [Customize an order summarization skill in Now Assist for Order Management](../task/customize-order-summarization-skill-now-assist-order-management.md).

**Note:** Microsoft Azure, Amazon bedrock, Now LLM, Now LLM LTS, and Google Cloud vertex AI are currently the providers for this Now Assist application's skills.

## Configuring the Manage Order Operations application

Business-to-business \(B2B\) customers can submit order cases using Now Assist Virtual Assistant from the Business Portal. Interaction channels include chat and voice options. Before you can use the AI agents for managing order operations from the Business Portal:

-   [Enable the manage order operations agent on the Business Portal](../task/enable-manage-order-operations-ai-agent.md)
-   [Configure ATP API for the manage order operations agent](../task/create-atp-api-call.md)

Enable AI voice agent support on your phone channels by installing the Now Assist Voice \[sn\_voice\_aia\] plugin. For more information, see [Deploy AI voice agents](https://www.servicenow.com/docs/access?context=deploy-ai-agents-for-voice&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Configuring the Manage Invoice Operations application

Business-to-business \(B2B\) customers can submit invoice cases using Now Assist Virtual Assistant from the Business Portal. Interaction channels include chat and voice options. Billing specialists and agents can use the invoice dispute assist agentic workflow from the CSM/FSM Configurable Workspace to resolve invoice cases. Before you can use the AI agents for managing order operations agent in the Business Portal:

-   [Configure AI-assisted invoice dispute intake on the Business Portal](../task/enable-manage-invoice-operations-ai-agent.md)
-   [Configure the invoice quantity validation extension point](../task/configure-invoice-quantity-check-ep.md)
-   [Configure the invoice dispute resolution extension point](../task/configure-invoice-case-resolution-ep.md)
-   [Make the invoice dispute assist workflow available in the Now Assist panel](../task/enable-invoice-dispute-assist-agentic-workflow.md)

Enable AI voice agent support on your phone channels by installing the Now Assist Voice \[sn\_voice\_aia\] plugin. For more information, see [Deploy AI voice agents](https://www.servicenow.com/docs/access?context=deploy-ai-agents-for-voice&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Related topics**  


[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Configuring Now Assist Admin features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Using Now Assist for Order Management](now-assist-order-management-using.md)

