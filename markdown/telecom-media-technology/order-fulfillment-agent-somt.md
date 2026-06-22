---
title: Now Assist for Sales CRM for Telecommunications AI agent collection Order Fulfillment AI agent
description: Use the Order Fulfillment AI agent to identify the tasks required for domain orders by using historical data from similar orders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/telecom-media-technology/order-fulfillment-agent-somt.html
release: yokohama
topic_type: concept
last_updated: "2025-10-29"
reading_time_minutes: 2
breadcrumb: [Standalone agents in SOMT, Use agentic workflows, Now Assist for Sales CRM for Telecommunications, Telecommunications, Media, and Technology]
---

# Now Assist for Sales CRM for Telecommunications AI agent collection Order Fulfillment AI agent

Use the Order Fulfillment AI agent to identify the tasks required for domain orders by using historical data from similar orders.

## Order Fulfillment AI agent overview

The Order Fulfillment AI agent uses historic order tasks to create the order tasks. If the historic data doesn't return any results, then an LLM is used to get the response. After decomposition, the Fulfillment AI Agent creates order tasks by checking historical and applicable tasks.

Based on the domain order, this agent retrieves a list of tasks that must be fulfilled. For each such domain order, it uses historical data from similar orders to find all such tasks.

If the Product offering or Category fulfillment tasks defined in the decision table aren’t available to create the fulfillment tasks for product, service, and resource, the default flow Service order Trigger Fulfillment AI Agent, Resource order Trigger Fulfillment AI Agent, and Product order Trigger Fulfillment AI Agent is considered to create the fulfillment tasks for an order line item during the fulfillment process. For more information on configuring decision tables, see [Decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/decision-tables/decision-table.md).

When a domain order is created, if a fulfillment process isn’t defined for that domain order specification category, a place order task is created. When this task is assigned to an agent, it triggers the Fulfillment AI Agent for this domain order.

To modify the Order Fulfillment AI agent, [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

The Order Fulfillment AI agent adds tasks apart from the generated tasks from GAF. To activate the GAF, see [Activate Group Action Framework for Now Assist for Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/telecom-media-technology/activate-group-action-framework-somt.md). The GAF and AI search are both used for order tasks.

Role required: sn\_somt\_gen\_ai.sales\_and \_order\_fulfillment\_ai\_agent

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Order Fulfillment AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Order Fulfillment AI agent**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Testing the AI agent

To access the use case testing page:

-   Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
-   On the Overview page, select **Test use cases**.

