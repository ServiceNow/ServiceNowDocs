---
title: Configure Veza access intelligence in the agent map
description: Integrate Veza with ServiceNow using OAuth 2.0 to display agent risk scores and severity levels in the agent map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-veza-access-intelligence.html
release: brazil
topic_type: concept
last_updated: "2026-09-08"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configure Veza access intelligence in the agent map

Integrate Veza with ServiceNow using OAuth 2.0 to display agent risk scores and severity levels in the agent map.

Veza access intelligence requires a connection between ServiceNow and each hyperscaler that hosts governed AI assets. ServiceNow and Veza each maintain separate connections to hyperscalers to retrieve and correlate AI asset data. Access intelligence supports governed agents hosted by Amazon Web Services \(AWS\), Gemini Enterprise Agent Platform, Azure AI Foundry, and Salesforce.

Complete the following in order:

1.  In your Veza tenant, configure integrations for all of the supported hyperscalers that you want to connect to. For more information, see [Veza integrations](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/integrations/integrations).
2.  In AI Control Tower, navigate to **Settings** &gt; **Integrations** &gt; **Connectors** to configure integrations for the same hyperscalers. For more information, see [Create an AI connection for discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-create-ai-connection-discovery.md).
3.  The Veza connector itself authenticates using OAuth 2.0 only. Configure OAuth in your Veza tenant. See [Configure OAuth in Veza](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-oauth.md).
4.  Configure OAuth in the ServiceNow platform and link it to the pre-provided `SN AI Security Veza Connector` connection alias. See [Configure OAuth for Veza in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-servicenow.md).
5.  Create the AI connection for Veza in **Settings** &gt; **Integrations** &gt; **Connectors**. See [Create an AI connection for Veza access intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-create-ai-connection-veza.md).

Once configured, select an AI asset in the agent map and view the Access intelligence tab to see risk score and other information. If your token has expired or you haven't yet authenticated, select **Re-Authenticate** on that tab. See [Discover your agent network with the map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-use-map.md).

**Tip:** If your AI asset appears in the agent map but doesn't have information shown in the Access intelligence tab, make sure that it's a governed asset with `external_ref_id` populated and `model_category=Agentic AI`.

-   **[Configure OAuth in Veza](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-oauth.md)**  
Create an OAuth 2.0 client and an OAuth 2.0 app in your Veza tenant so that AI Control Tower can authenticate to Veza using OAuth 2.0 instead of an API key.
-   **[Configure OAuth for Veza in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-servicenow.md)**  
Set up two application registries, their OAuth entity scopes and credentials, then link them to the pre-provided connection alias, so that AI Control Tower can authenticate to Veza using OAuth 2.0.

**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configuring.md)

