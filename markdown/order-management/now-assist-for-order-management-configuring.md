---
title: Configuring ServiceNow Otto for Order Management
description: If you have the admin role, you can configure the ServiceNow Otto for Order Management application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/order-management/now-assist-for-order-management-configuring.html
release: yokohama
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Order Management]
---

# Configuring ServiceNow Otto for Order Management

If you have the admin role, you can configure the ServiceNow Otto for Order Management application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Platform.

Use the AI Admin Hub console to configure ServiceNow Otto for Order Management. Use Summarization for Order Management plugin to install and configure the generative AI skills.

**Note:** Currently for the initial release, the plugin cannot be installed from the **Plugins** section of Now Assist Admin. As a workaround, you can install the application from Application Manager.

The Now Assist skills for SOM:

-   Order Summarization for Order Capture
-   Order Summarization for Order Fulfillment

**Note:**

Azure, Amazon bedrock, Now LLM, Now LLM LTS, and Google Cloud vertex AI are currently the providers for this Now Assist application's skills.

## Configuring standalone AI agents

Business-to-business \(B2B\) customers can submit order cases using Now Assist from the Business Portal. Interaction channels include chat and voice options. Before you can use the manage order operations agent in the Business Portal:

-   [Enable the manage order operations agent on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/enable-manage-order-operations-ai-agent.md)
-   [Configure ATP API for the manage order operations agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/create-atp-api-call.md)

Enable Voice AI agent support on your phone channels by installing the Now Assist Voice \[sn\_voice\_aia\]. For more information, see [Deploy AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/deploy-ai-agents-for-voice.md).

-   **[Customize an order summarization skill in ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/customize-order-summarization-skill-now-assist-order-management.md)**  
If you have the admin role, you can configure the ServiceNow Otto for Order Management application so that your order agent and fulfilment agent can use the generative AI skills in CSM Configurable Workspace and in Platform.
-   **[Enable the manage order operations agent on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/enable-manage-order-operations-ai-agent.md)**  
Activate and associate the Manage order operations agent on the Business Portal so your customers can use it to submit order cases autonomously using Now Assist.
-   **[Configure ATP API for the manage order operations agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/create-atp-api-call.md)**  
Create an Available-to-Promise \(ATP\) API call that enables the manage order operations agent to check product availability and determine the earliest possible delivery date when customers request expedited shipping.

**Parent Topic:**[ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/now-assist-order-management.md)

**Related topics**  


[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring Now Assist settings and features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-na-landing.md)

[Standalone agents in Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/now-assist-om-ai-agents.md)

