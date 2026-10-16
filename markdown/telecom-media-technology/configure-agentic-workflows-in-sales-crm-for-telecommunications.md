---
title: Configure agentic workflows for Sales CRM for Telecommunications
description: Duplicate and activate the Sales CRM for Telecommunications AI agents, and complete any additional setup a specific agent requires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/configure-agentic-workflows-in-sales-crm-for-telecommunications.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 2
breadcrumb: [Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Configure agentic workflows for Sales CRM for Telecommunications

Duplicate and activate the Sales CRM for Telecommunications AI agents, and complete any additional setup a specific agent requires.

Role required: admin

Agentic workflows included with the base system are read-only. Before you use one, duplicate it and activate it, along with any AI agents and triggers it depends on. See [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md) and [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-aia-use-case.md). This applies to every agent below; the sections that follow list only what's *additionally* required for that specific agent.

## Move order voice AI agent

Role required: sn\_customerservice.consumer

-   In **Assistant Designer** &gt; **Assistants**, open the ServiceNow Otto Voice Deployment tile and review the **Settings** tab.
-   To create a SoftPIN, see [Configure Soft PIN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/configure-soft-pin.md).
-   On the select channels and status page, turn on **Active** to activate the agent.

See [ServiceNow Otto for Sales Customer Relationship Management for Telecommunications AI agent Move order voice AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-move-order-somt.md) for full configuration and access steps.

## Order enrichment AI agent

Role required: sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

-   Activate the Group Action Framework \(GAF\). See [Activate Group Action Framework for ServiceNow Otto for Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/activate-group-action-framework-somt.md).
-   In the **Edit trigger** form, turn on **Active** so the agent can trigger autonomously.

See [ServiceNow Otto for Sales Customer Relationship Management for Telecommunications AI agent collection order enrichment AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/order-enrichment-agent-somt.md) for full configuration, access, and testing steps.

## Order fulfillment AI agent

Role required: sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

In the **Edit trigger** form, turn on **Active** so the agent can trigger autonomously.

See [ServiceNow Otto for Sales CRM for Telecommunications AI agent collection order fulfillment AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/order-fulfillment-agent-somt.md) for full configuration, access, and testing steps.

## Order fallout AI agent

Role required: sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

On the select channels and status page, turn on **Active** to activate the agent.

See [ServiceNow Otto for Sales CRM for Telecommunications AI agent Order fallout AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-order-fallout-somt.md) for full configuration, access, and testing steps.

## Image to task plan template AI agent

Role required: sn\_task\_plan.admin and sn\_prd\_pm.product\_catalog\_admin

-   To access the agent in AI Agent Studio, see [Access the Image to task plan template AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/access-image-to-task-plan-template-ai-agent-somt.md).
-   To test the agent, see [Test the Image to task plan template AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/test-image-to-task-plan-template-ai-agent-somt.md).

See [ServiceNow Otto for Sales CRM for Telecommunications AI agent Image to task plan template AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-task-template-generation-somt.md) for full details.

**Related topics**  


[ServiceNow agentic workflows in Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/servicenow-agentic-workflows-in-sales-crm-for-telecommunications.md)

[Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md)

