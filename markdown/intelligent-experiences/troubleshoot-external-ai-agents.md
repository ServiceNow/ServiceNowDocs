---
title: Troubleshoot external AI agents
description: Use this troubleshooting guide to resolve issues with External AI agents' roles, testing procedures, failure diagnosis and reference resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/troubleshoot-external-ai-agents.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, AI Agent Studio, Enable AI experiences]
---

# Troubleshoot external AI agents

Use this troubleshooting guide to resolve issues with External AI agents' roles, testing procedures, failure diagnosis and reference resources.

## Prerequisites for External AI agents

The following plugins, versions, and roles are apply for external AI agents:

-   Application version: ServiceNow Otto AI Agents v6.0.x+.
-   Platform version: Zurich Patch 4+ or Yokohama Patch 11+.
-   Enable external agent interoperability \(AI Agent Studio → Settings\):
    -   Set the **sn\_aia.external\_agents.enabled** to **true** \(ServiceNow can call external agents\).
    -   Set the **sn\_aia.internal\_agents.enabled\_external** system property to **true** \(External agents can call ServiceNow AI Agents\).
-   Service account &amp; roles for inbound A2A calls: sn\_aia.integration \(runtime\) or sn\_aia\_admin \(testing\), plus rest\_service and snc\_platform\_rest\_api\_access.
-   AI Agent activation &amp; discoverability: Ensure the agent is active and enable the AI agent for discovery \(sets External discoverable on sn\_aia\_agent\_config\).

## Autonomous mode

You must enable the autonomous mode for executing External AI agents. Using the Supervised execution mode runs with human interaction or intervention as opposed to an agent interaction and needs the autonomous mode to be set up. For more information, see [Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-tool-aia-new.md).

The asynchronous mode is not supported for external AI agents in AI Agent Studio. Change the communication mode to the Synchronous mode while onboarding the external agents and enable push notifications.

## Review logs for external agents

You can retrieve tool logs using the sn\_aia\_external\_agent\_exec\_history table and to access the full conversation history via the task/get method, enable the **Display output** in tool settings.

## Additional resources

Use the following documentation resources for more information:

-   Enable MCP and A2A protocol: [Enable MCP and A2A for your agentic workflows](https://www.servicenow.com/community/servicenow-otto-articles/enable-mcp-and-a2a-for-your-agentic-workflows-with-faqs-updated/ta-p/3373907).
-   [AI Agents and 3rd-party integrations](https://www.servicenow.com/community/servicenow-otto-articles/ai-agents-and-3rd-party-integrations/ta-p/3316286).
-   [Setting up A2A authentication for ServiceNow AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)
-   [Sample payloads for A2A - ServiceNow as secondary Agent](https://www.servicenow.com/community/servicenow-otto-articles/sample-payloads-for-google-a2a-servicenow-as-secondary-agent/ta-p/3451904)
-   [AI Agents FAQ and Troubleshooting](https://www.servicenow.com/community/servicenow-otto-articles/ai-agents-faq-and-troubleshooting/ta-p/3200454)
-   [Troubleshooting AI Agents](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2419769)
-   [External AI agents in ServiceNow via A2A - ServiceNow as primary agent](https://www.servicenow.com/community/servicenow-otto-articles/external-agents-in-servicenow-via-google-a2a-servicenow-as/ta-p/3467587)
-   [Generative AI skill support in MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-support-mcp.md)
-   [Troubleshooting RaptorDB](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1513425)

