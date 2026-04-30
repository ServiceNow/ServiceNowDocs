---
title: Now Assist for Sales CRM for Telecommunications AI agent collection Order Enrichment AI agent
description: Use the Order Enrichment AI agent to collect customer order information, identify if the order needs enrichment, and create enrichment tasks.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Standalone agents in SOMT, Use agentic workflows, Now Assist for Sales CRM for Telecommunications, Telecommunications, Media, and Technology]
---

# Now Assist for Sales CRM for Telecommunications AI agent collection Order Enrichment AI agent

Use the Order Enrichment AI agent to collect customer order information, identify if the order needs enrichment, and create enrichment tasks.

## Order Enrichment AI agent overview

The Order Enrichment AI agent creates a task and triggers the order fulfillment AI agent upon its completion. On closure of the enrichment task, it invokes the order fulfillment agent.

Given a top Order Line Item \(OLI\) finds all tasks needed to enrich it and all it child OLIs.

For each top order line item \(OLI\) and its child OLIs, the Order Enrichment Agent uses historical data from similar orders to determine which enrichment tasks are required.

To activate the Group Action Framework \(GAF\), see [Activate Group Action Framework for Now Assist for Sales CRM for Telecommunications](../task/activate-group-action-framework-somt.md).

If needed, the outcome of the order tasks can be modified by the agent.

When an order line item is created, if an enrichment process isn’t defined for that order line specification, a place order task is created. When this task is assigned to an agent, it triggers the Enrichment AI Agent for this order line item.

If the specification enrichment tasks defined in the decision table aren’t available to create the enrichment tasks, the default flow Trigger EnrichmentAI Agent is triggered to create the enrichment tasks for an order line item during the enrichment process. To configure the order enrichment flows using Decision Tables, see [Configuring order enrichment flows using Decision Tables](https://www.servicenow.com/docs/access?context=configure-order-enrichment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US).

To modify the Order Enrichment AI agent, [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

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

To test the use case, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

