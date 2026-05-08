---
title: Now Assist for Sales CRM for Telecommunications AI agent collection order fulfillment AI agent
description: Use the order fulfillment AI agent to identify the tasks required for domain orders by using historical data from similar orders.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AI agents in SOMT, Use agentic workflows, Now Assist for Sales CRM for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Sales CRM for Telecommunications AI agent collection order fulfillment AI agent

Use the order fulfillment AI agent to identify the tasks required for domain orders by using historical data from similar orders.

## Order fulfillment AI agent overview

The order fulfillment AI agent uses historic order tasks to create the order tasks. If the historic data doesn't return any results, then a large language model \(LLM\) is used to get the response. After decomposition, the order fulfillment AI agent creates order tasks by checking historical and applicable tasks.

Based on the domain order, this agent retrieves a list of tasks that must be fulfilled. For each such domain order, the agent uses historical data from similar orders to find all such tasks.

If the Product offering or Category fulfillment tasks defined in the decision table aren’t available to create the fulfillment tasks for product, service, and resource, the default flow Service order trigger fulfillment AI agent, resource order trigger fulfillment AI agent, and Product order trigger fulfillment AI agent are considered to create the fulfillment tasks for an order line item during the fulfillment process. For more information on configuring decision tables, see Decision tables.

When a domain order is created, if a fulfillment process isn’t defined for that domain order specification category, a place order task is created. When this task is assigned to an agent, it triggers the order fulfillment AI agent for this domain order.

To modify the order fulfillment AI agent, Duplicate an agentic workflow, and adjust the settings according to your requirements.

The order fulfillment AI agent adds tasks apart from the generated tasks from Group Action Framework \(GAF\). To activate the GAF, see [Activate Group Action Framework for Now Assist for Sales CRM for Telecommunications](../task/activate-group-action-framework-somt.md). The GAF and AI search are both used for order tasks.

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

