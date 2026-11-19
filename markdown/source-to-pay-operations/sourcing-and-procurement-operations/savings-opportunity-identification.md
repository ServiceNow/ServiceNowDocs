---
title: Savings opportunity identification
description: The Savings Opportunity Discovery agentic workflow automatically scans contracts, spend, and supplier data to surface ranked savings opportunities, helping category managers focus on review and action rather than manual discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-identification.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-11-17"
reading_time_minutes: 8
keywords: [savings opportunity, agentic workflow, savings lever, AI agent, category management]
breadcrumb: [Spend and Savings Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Savings opportunity identification

The Savings Opportunity Discovery agentic workflow automatically scans contracts, spend, and supplier data to surface ranked savings opportunities, helping category managers focus on review and action rather than manual discovery.

The Savings Opportunity Discovery agentic workflow scans contracts, spend, and supplier data on a recurring schedule and writes ranked savings opportunities to the Savings Opportunities \(`sn_spend_gen_ai_savings_opportunities`\) table. An AI orchestrator triggers three optimization sub-agents in parallel, normalizes the results, and surfaces findings for category managers to review. Each opportunity carries an estimated savings value, a complexity assessment, and supporting insights. Category managers see only the opportunities tied to spend categories they own.

\[Omitted image "spend-pot-saving-oppo.png"\] Alt text: Potential savings opportunities page in the Source-to-Pay Workspace.

## Plugin dependencies

The following plugins are required to use the Savings Opportunity Discovery agentic workflow:

-   Now Assist for Sourcing and Procurement Operations \(SPO\) \(`sn_spend_gen_ai`\)
-   Sourcing Pipeline Management \(`sn_spend_pipeline`\)
-   Spend and Savings Management \(`sn_spend_mgmt`\)

## Prerequisites

Before you run the Savings Opportunity Finder Agents Scheduled Job, make sure that the ServiceNow Otto panel is available to the Savings Opportunity Discovery agentic workflow. If it is not, the scheduled job runs but no agent conversation starts, so no savings opportunities are created.

1.  Make sure that the ServiceNow Otto panel is turned on. Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Experiences** &gt; **ServiceNow Otto Panel**. If the panel is turned off, select **Turn on**.

    \[Omitted image "otto-panel-ai-admin-hub.png"\] Alt text: ServiceNow Otto Panel page in AI Admin Hub showing that the panel is turned on for users.

2.  Make sure that the default ServiceNow Otto panel deployment is active. On the ServiceNow Otto Panel page, in the **Settings** section, select **Visit Assistant Designer**. In Assistant Designer, the **ServiceNow Otto panel - Platform \(default\)** assistant must have an **Active** status. If the deployment is not active, activate it.

    \[Omitted image "otto-panel-default-deployment.png"\] Alt text: Assistant Designer showing the ServiceNow Otto panel - Platform \(default\) assistant with an Active status.

3.  Turn on the ServiceNow Otto panel channel for the Savings Opportunity Discovery agentic workflow. The Contract, Supplier, and Spend Optimization Opportunity Finder agents are part of this workflow. Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows**, and then open **Savings Opportunity Discovery**. If the workflow is read-only, select **Edit in original scope**. In the left pane, select **Select channels and status**, and then turn on **Display** for **Engage via the Otto panel**. Save your changes.

    \[Omitted image "otto-panel-workflow-channel.png"\] Alt text: Select channels and status step of the Savings Opportunity Discovery workflow with Display turned on for Engage via the Otto panel.


## Business value

Category managers have historically relied on manual reviews of contracts, spend, and supplier data to identify sourcing opportunities. The process is inconsistent across categories and time-consuming, so opportunities are missed or surfaced too late to act on. Scheduled, agent-based identification produces consistent output for every spend category and lets the team focus attention on review, simulation, and action rather than discovery.

## Savings lever framework

Each opportunity is associated with a savings lever that describes the specific source of savings. Levers currently supported include renewal caps, price escalations, payment terms, off-contract spend, unconsolidated spend, supplier consolidation, and non-preferred supplier spend. The framework supports additional levers without changes to the user-facing review surface.

## Savings Opportunity Discovery agentic workflow

Savings Opportunity Discovery agentic workflow contains three Opportunity Finder agents.

|Agent|Analyzes|Savings levers covered|
|-----|--------|----------------------|
|Contract Optimization Opportunity Finder Agent|Extracts contract clauses, including escalation percentages, renewal caps, and payment terms, and forecasts future spend under the existing terms.|Price Escalations &amp; Renewal Caps; Payment Terms Optimization|
|Supplier Optimization Opportunity Finder Agent|Analyzes supplier spend for fragmentation across suppliers and for spend with non-preferred suppliers.|Non-preferred Supplier Spend; Unconsolidated Spend; Spend Fragmentation; supplier performance and risk|
|Spend Optimization Opportunity Finder Agent|Analyzes purchase order activity for off-contract spend, unconsolidated spend, and other spend-side levers.|Off-Contract Spend; Contract Leakage|

The Savings Opportunity Finder Agents Scheduled Job runs the agents weekly. You can also run this scheduled job on-demand by entering `sysauto.list` in the navigation filter. Search for and open the Savings Opportunity Finder Agents Scheduled Job, and then select **Execute Now**.

When the Savings Opportunity Finder Agents Scheduled Job runs, the Savings Opportunity Discovery agentic workflow uses all three agents and scans procurement data across contracts, suppliers, and purchase order lines and creates records on the Savings Opportunities table \(`sn_spend_gen_ai_savings_opportunities`\).

Each opportunity record contains an estimated opportunity value, a savings lever, a confidence score, supporting data, and links to the suppliers, spend categories, and contracts the analysis drew from. Category managers review the opportunities, accept or dismiss them, and convert accepted opportunities into pipeline projects for tracking.

For more information about the fields on a savings opportunity record, see [Savings opportunity fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-fields.md).

## Opportunity lifecycle

Each run generates new opportunities and reconciles existing ones according to the current state of the record:

-   An open opportunity that has not yet been acted upon is updated in place when its underlying data changes. For example, when new closed purchase order lines change the estimated savings.
-   A dismissed opportunity can reappear if fresh data changes the estimate enough to invalidate the original dismissal.
-   A closed opportunity for which a pipeline project has been created is not re-created. For spend and supplier optimization, the next run can create a delta opportunity that reflects only the new data since the original was actioned.

## Decision and action flow

Opportunities appear in two places in the Source-to-Pay Workspace: a unified **Potential savings opportunities** page that lists every opportunity accessible to the signed-in user, and a **Category Management** tab scoped to the spend category in context. From either entry point, the user opens the Now Assist Panel by selecting **Learn more** for a single opportunity to review supporting insights, ask clarifying questions, run simulations, and either action or dismiss the opportunity.

\[Omitted image "spend-cat-mgmt-tab.png"\] Alt text: Category Management tab in the Source-to-Pay Workspace showing savings opportunities.

When an opportunity is presented, the category manager can:

-   Open the opportunity in the Now Assist Panel to review details, ask follow-up questions, and simulate alternative values.
-   Act on the opportunity by creating a pipeline project with key fields prefilled from the opportunity.
-   Dismiss the opportunity with one or more reasons selected from a checklist.

Acted and dismissed decisions are captured as feedback to improve future opportunity generation.

For more information about actioning or dismissing a savings opportunity, see [Action or dismiss a savings opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/action-or-dismiss-savings-opportunity.md).

## Roles and access

Access to savings opportunity records is governed by the following roles:

-   sn\_spend\_mgmt.sourcing\_category\_manager: Read access to the Savings Opportunities \(`sn_spend_gen_ai_savings_opportunities`\) table and records.
-   sn\_spend\_mgmt.category\_manager\_admin: Write access to opportunity records, and read and write access to the `sn_spend_gen_ai.savings_opportunity.cost_of_capital` system property.

## Troubleshooting: no savings opportunities are created

If the Savings Opportunity Finder Agents Scheduled Job runs but no savings opportunities are created, check the system log for entries from the `sn_aia` source and from the scheduled job, and then use the following list to find the cause.

-   The log shows `startAiAgentConversation: Now Assist Panel default deployment is not active` and `Execution plan terminated, conversation never launched` for each agent, even though the scheduled job logged that the agent started successfully. No conversation or agent run starts, and nothing appears in the progress worker list. The default ServiceNow Otto panel deployment is not active. Activate it as described in [Prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-identification.md).
-   The log shows `savingsOpportunityFinderAgentsJob` followed by the agent name and `agent couldnt be started as NAP is inactive for the agent`. The ServiceNow Otto panel channel is not turned on for that agent. Turn it on for the Savings Opportunity Discovery agentic workflow as described in [Prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-identification.md).
-   The scheduled job does not run, and the log has no entries from it. The scheduled job runs only when the ServiceNow Otto panel channel is turned on for at least one of the three Opportunity Finder agents.

-   **[Supplier optimization savings opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/supplier-optimization-savings-opportunities.md)**  
The Supplier Optimization Opportunity Finder Agent identifies spend placed with non-preferred suppliers and fragmented across multiple suppliers for similar products. Addressing these opportunities helps redirect spend to preferred sources and consolidate supplier relationships.
-   **[Spend optimization savings opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/spend-optimization-savings-opportunities.md)**  
Spend Optimization Opportunity Finder Agent identifies opportunities where purchase activity is outside negotiated contracts or fragmented across multiple contracts. Addressing these opportunities helps redirect spend to contracted pricing and increase purchasing volume for negotiation.
-   **[Contract optimization savings opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/contract-optimization-savings-opportunities.md)**  
The Contract Optimization Opportunity Finder Agent identifies opportunities to reduce costs by renegotiating price escalations, renewal caps, and payment terms on supplier contracts.

**Parent Topic:**[Spend and Savings Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/spo-spend-mgmt.md)

