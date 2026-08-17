---
title: Agentic AI application for quote generation
description: The Quote AI Agent is part of ServiceNow Otto for CPQ that interprets sales representative intent, retrieves opportunity and contract data, configures products, applies pricing and discounts, generates quote documents, and drafts client emails. Sales representatives review and approve each step before the agent proceeds. The Quote AI Agent uses an orchestrator that coordinates seven specialized agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/agentic-ai-app-quote-generation.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 2
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Agentic AI application for quote generation

The Quote AI Agent is part of ServiceNow Otto for CPQ that interprets sales representative intent, retrieves opportunity and contract data, configures products, applies pricing and discounts, generates quote documents, and drafts client emails. Sales representatives review and approve each step before the agent proceeds. The Quote AI Agent uses an orchestrator that coordinates seven specialized agents.

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

