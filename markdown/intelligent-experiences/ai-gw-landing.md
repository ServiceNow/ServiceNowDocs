---
title: AI Gateway in AI Control Tower
description: Route AI agent connections to MCP servers through AI Gateway, so you control which servers and tools agents can reach and what data passes between them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-landing.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, AI Gateway, MCP server, MCP client, Model Context Protocol]
breadcrumb: [Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI Gateway in AI Control Tower

Route AI agent connections to MCP servers through AI Gateway, so you control which servers and tools agents can reach and what data passes between them.

## Get started

<table id="table_ai-gw-landing" class="nav-card presentation"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn how AI Gateway governs, controls, and observes MCP server connections.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-exploring.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Prepare your instance, approve MCP servers, and set the AI Gateway settings that apply to every connection.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-configuring.md)

</td><td>

[Connect agents\[Omitted image "bus-agent-workspace-1.svg"\] Alt text:Register clients and point agents at the AI Gateway MCP server URL.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-connecting-agents.md)

</td></tr><tr><td>

[Govern tools and data\[Omitted image "bus-compliance.svg"\] Alt text:Decide which tools agents can call and help filter sensitive data in MCP traffic.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-governing-tools-data.md)

</td><td>

[Control traffic\[Omitted image "bus-switch.svg"\] Alt text:Turn MCP server connections off and on, and review server activity.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-traffic.md)

</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Find roles and system properties for AI Gateway.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-reference.md)

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

AI agents use the Model Context Protocol \(MCP\) to call tools on MCP servers, for example, to read data, search a knowledge base, or update a record. AI Gateway sits between AI agents and the MCP servers that they call. Agents, whether they run in AI Agent Studio or on an external platform, connect to an AI Gateway MCP server URL instead of to the MCP server directly. AI Gateway is designed to authenticate each client, check each call against your policies, and record the result.

Instance-wide controls are on the **AI Gateway** settings page. Controls for one MCP server are on the **AI Gateway** tab of that server's record.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [AI Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [ServiceNow AI documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-products.md).

