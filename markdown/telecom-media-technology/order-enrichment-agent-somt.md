---
title: Now Assist for Sales CRM for Telecommunications AI agent collection order enrichment AI agent
description: Use the order enrichment AI agent to collect customer order information, identify if the order needs enrichment, and create enrichment tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI agents in SOMT, Use agentic workflows, Now Assist for Sales CRM for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Sales CRM for Telecommunications AI agent collection order enrichment AI agent

Use the order enrichment AI agent to collect customer order information, identify if the order needs enrichment, and create enrichment tasks.

## Order enrichment AI agent overview

The order enrichment AI agent creates a task and triggers the order fulfillment AI agent on its completion. On closure of the enrichment task, the order fulfillment agent is invoked.

For each top order line Item \(OLI\) and its child OLIs, the order enrichment agent uses historical data from similar orders to determine which enrichment tasks are required.

To activate the Group Action Framework \(GAF\), see [Activate Group Action Framework for Now Assist for Sales CRM for Telecommunications](../task/activate-group-action-framework-somt.md).

If needed, the outcome of the order tasks can be modified by the agent.

When an OLI is created, if an enrichment process isn’t defined for that order line specification, a place order task is created. When this task is assigned to an agent, it triggers the order enrichment AI agent for this order line item.

If the specification enrichment tasks defined in the decision table aren’t available to create the enrichment tasks, the default flow trigger enrichment AI agent is triggered to create the enrichment tasks for an order line item during the enrichment process. To configure the order enrichment flows using Decision Tables, see [Configure order enrichment flows using Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-order-enrichment.md).

To modify the order enrichment AI agent, [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

Role required: sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Order Enrichment AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Order Enrichment AI agent**.

## Testing the AI agent

To access the use case testing page:

-   Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
-   On the Overview page, select **Test use cases**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

