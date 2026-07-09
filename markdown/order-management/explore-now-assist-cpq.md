---
title: Exploring Now Assist for Configure, Price, Quote \(CPQ\)
description: With the Now Assist for Configure, Price, Quote \(CPQ\) application, you can use generative AI to summarize quotes and provide immediate, comprehensive visibility into key quote information such as products, pricing, and terms. This functionality reduces errors, accelerates quote creation, and helps teams deliver accurate quotes faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/explore-now-assist-cpq.html
release: australia
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 3
breadcrumb: [Now Assist for CPQ, Sales Customer Relationship Management]
---

# Exploring Now Assist for Configure, Price, Quote \(CPQ\)

With the Now Assist for Configure, Price, Quote \(CPQ\) application, you can use generative AI to summarize quotes and provide immediate, comprehensive visibility into key quote information such as products, pricing, and terms. This functionality reduces errors, accelerates quote creation, and helps teams deliver accurate quotes faster.

## Now Assist for CPQ overview

The AI summarization of quotes provides sales teams and stakeholders with fast, reliable insight into complex quote information. AI summaries help:

-   Deliver fast, consistent insight into key quote details.
-   Reduce manual review and speed up quote turnaround.
-   Surface issues early to prevent deal delays.
-   Keep teams aligned and helps move deals forward.

The Now Assist for CPQ includes Quote AI Agent that automates quote creation and modification for faster respond to customers with fewer errors.

## Now Assist for CPQ skills

The Now Assist for CPQ application includes the generative AI skill that enables quote summarization. When activated, this skill helps agents gather context faster.

Get started by performing the following tasks:

-   [Configuring Now Assist for Configure, Price, Quote \(CPQ\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-now-assist-cpq.md)
-   [Summarize a quote using quote summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/summarize-quote.md)

## Agentic AI application for quote generation

The Quote AI Agent is part of Now Assist for CPQ that interprets sales representative intent, retrieves opportunity and contract data, configures products, applies pricing and discounts, generates quote documents, and drafts client emails. Sales representatives review and approve each step before the agent proceeds. The Quote AI Agent uses an orchestrator that coordinates seven specialized agents.

The agent compresses the quote-building lifecycle by handling repetitive, deterministic work autonomously. A single prompt can drive multiple actions in one turn—for example, adding several products, configuring one of them, and applying a discount—without requiring the sales representative to issue each action separately.

**Note:** The Quote AI Agent uses AI to interpret intent and retrieve context. Outputs may not reflect the full complexity of a deal. Review all agent-generated quotes before sharing them with customers.

The Quote AI Agent operates in two modes:

-   **Autonomous**

    The agent completes the full sequence—opportunity context retrieval, product addition, configuration, discounting, and document generation—without pausing for confirmation. Use this mode for well-scoped, low-risk requests.

-   **Human-in-the-loop**

    The agent pauses at predefined decision points and asks the sales representative to confirm or adjust before continuing. Decision points include applying a discount that exceeds a threshold, adding a product with ambiguous configuration, and generating the final quote document.


When creating a quote from an opportunity, the agent retrieves relevant opportunity context—including customer needs, products of interest, and expected commercial terms—to ground the quote in the opportunity data. This context retrieval uses the Opportunity Summarization skill when it's installed and entitled on the instance. When that skill isn't available, the agent retrieves opportunity fields directly and constructs a structured context object without AI inference, so the agent remains functional regardless of entitlement.

For configurable products, the agent starts a configuration session, applies your inputs as configuration field values, and reads back the resulting bill of materials. The configured product is added to the quote with full configuration lineage retained, so you can reconfigure it later.

The agent applies discounts at two levels:

-   **Header level**: A discount applied to the overall quote.
-   **Line level**: A discount applied to a specific line item.

Discounts can be in percentage or absolute terms. They can be explicit where you state the amount directly, or implicit where the agent derives the discount from context such as a previously negotiated rate. The agent surfaces the applied discounts back to you as part of its response. When a discount exceeds the approval threshold, the agent notifies you and starts the approval workflow automatically.

