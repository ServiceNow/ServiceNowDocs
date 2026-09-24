---
title: Sourcing and Procurement Operations release notes
description: Sourcing and Procurement Operations provides employees with an automated tool for shopping for goods and services needed at work.The Brazil Early Availability release introduces a new Configuration Console and Product Hub to streamline Sourcing and Procurement Operations admin setup. Shoppers can manage delivery addresses and purchase on behalf of others, and a new progress tracker shows PR-to-PO status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/sourcing-procurement-operations-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [procurement, sourcing, purchase requisitions, purchase orders, procurement service management, SPO Configuration Console, SPO Product Hub, delivery address deletion, purchase on behalf of, progress tracker, Now Assist summarization]
breadcrumb: [Source-to-Pay Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Sourcing and Procurement Operations release notes

Sourcing and Procurement Operations provides employees with an automated tool for shopping for goods and services needed at work.

## About Sourcing and Procurement Operations

-   Browse a managed product catalog and submit purchase requests through a streamlined, e-commerce-like shopping experience.
-   Track purchase status, including approvals, tasks, and delivery milestones, from a single view.
-   Manage sourcing requests, purchase requisitions, negotiations, and procurement cases from a centralized workspace.
-   Automate end-to-end sourcing and purchasing workflows, including approvals, task generation, and purchase order creation.
-   Assess spend, operational efficiency, and team performance using pre-configured dashboards and metrics.

For an overview of Sourcing and Procurement Operations capabilities, see [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/psm-overview.md).

## Activation and other requirements

**Note:** Sourcing and Procurement Operations is available in the ServiceNow Store.

-   **Activation information**

    Request Sourcing and Procurement Operations from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/source-to-pay-operations-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release introduces a new Configuration Console and Product Hub to streamline Sourcing and Procurement Operations admin setup. Shoppers can manage delivery addresses and purchase on behalf of others, and a new progress tracker shows PR-to-PO status.

### What's new

-   **[SPO Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/spo-configuration-console.md)**

    Reduce setup time and configuration errors with a guided console that walks you through configuring all areas of your Sourcing and Procurement Operations deployment. Configure case types, playbooks, stepper statuses, assignment and routing, notifications, approvals, case resolution acceptance, the procurement specialist workspace, Now Assist AI skills, and new case type setup. Steps are sequenced, dependency-locked, and scoped to what admins are authorized and entitled to configure. Select steps can be configured conversationally with Now Assist where your SKU includes it. For example, you can configure SLA definitions for a new case type as a native console step with dependency locking and Now Assist guidance.

-   **[SPO Product Hub and Admin Home discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/spo-product-hub.md)**

    Discover Sourcing and Procurement Operations from an entitlement-driven tile on Admin Home. Install and configure it from a dedicated Product Hub that tracks installation status, guides you to add-on apps, applies default configurations, and surfaces learning resources.

-   **[Manage saved delivery addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/address-deletion-overview.md)**

    Delete saved delivery addresses you no longer need directly from Shopping Hub preferences. A confirmation step provides immediate feedback. Deleted addresses are removed from all locations where they were previously displayed, including at Shopping Hub checkout and on off-catalog record producers.

-   **[Purchase on behalf of others](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/purchase-on-behalf-sh.md)**

    The **On behalf of** list now defaults to the last-used recipient for consecutive purchases in the same session, so shoppers don't need to reselect them each time. This default no longer applies after the shopper clears the **On behalf of** selection, and it resets when a new session begins.

-   **[Purchase punchout items on behalf of others](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/purchase-punchout-on-behalf-sh.md)**

    Purchase punchout items on behalf of other users, with the same capabilities available for catalog items. This capability is available from punchout search results, supplier and product cards, the Browse supplier page, L2 punchout product details, and L1 punchout entry points in Employee Center.

    For L1 punchout suppliers, the selected business owner must be a member of the supplier's punchout group. That user's credentials and punchout group membership are used on the punchout supplier site, and any resulting cart items or orders are placed in their cart.

-   **[Enable a shopper to purchase on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/config-shoppinghub-purchase-behalf.md)**

    Admins can define who a buyer can purchase on behalf of by using broader criteria such as cost center, legal entity, or country.

-   **[Scope additional information questions to specific suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/configure-additional-information-prl.md)**

    Reduce checkout friction by limiting additional information checkout questions to the suppliers they actually apply to, instead of showing them for all suppliers of a product or category.

-   **[Progress tracker for PR-to-PO fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/progress-tracker-overview.md)**

    View the current status of a purchase requisition in the PR-to-PO journey with a real-time progress tracker. The tracker covers all states, including non-linear paths like punchout, revision, and cancellation. It surfaces next steps and owners. Procurement admins can configure which states display.

-   **[Received emails on purchase requisitions, purchase orders, and procurement cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/emails-related-list.md)**

    Received emails now also appear in an Emails related list on the record, alongside the existing Sent Emails and Draft Emails related lists. Procurement specialists can review incoming supplier or requester correspondence directly on the purchase requisition, purchase order, or procurement case without switching to a separate mailbox.

-   **[Conversational intake using SPO MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/conversational-intake-using-spo-mcp-server.md)**

    Request procurement items through conversational intake in your MCP client without leaving the chat interface. The MCP client guides you through discovery questions, recommends matching products based on your needs, and provides pre-filled request forms in Shopping Hub or Employee Center. This streamlined workflow eliminates the need to navigate multiple pages or manually search for products.

-   **[Task completion using SPO MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/task-completion-using-spo-mcp-server.md)**

    Manage all your procurement tasks in one place. View and complete tasks assigned to you based on your instance ACLs directly in your MCP client. The MCP client routes you to Employee Center only when e-signature or document uploads are required.

-   **[AI L1 SPO Service Desk Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/ztsd-agent-na-spo.md)**

    Automate high-volume L1 procurement inquiries end-to-end. Let the AI L1 SPO Service Desk Specialist resolve general inquiry cases autonomously, freeing your team to focus on complex procurement challenges that require human expertise.

-   **[Generate a knowledge article from a procurement case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/spo-generate-knowledge-article.md)**

    ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) generates knowledge articles from closed procurement cases. Use ServiceNow Otto to create articles directly from a closed procurement case or from the ServiceNow Otto panel, then publish them to your knowledge base.


### What's changed

-   **[Now Assist summarization includes email context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)**

    Now Assist summaries for purchase requisitions, purchase orders, and procurement cases now reflect the latest email communication. Summaries include sender, date, and key message alongside record fields. AI-generated next steps stay current with the most recent supplier or requester exchange.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


