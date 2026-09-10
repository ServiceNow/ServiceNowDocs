---
title: Configuring ServiceNow Quote Experience
description: Configuration tasks and sequence for setting up the ServiceNow Quote Experience with Quote Experience for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-crm-tm-quoting-configure.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 7
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring ServiceNow Quote Experience

Configuration tasks and sequence for setting up the ServiceNow® Quote Experience with Quote Experience for your organization.

## Quote Experience

Using ServiceNow Quote Experience, administrators can:

-   Control the quote layout and behavior for your users. The fields they see, how pricing is calculated, which approvals are required, and what actions are available at each stage of the quote lifecycle.
-   Access and configure stages, associated fields, related rules, rule groups, events, layouts, views, and personas.
-   Define the sales workflow stages your organization needs and define the conditions that must be true before a transaction can enter each stage.
-   Identify the transaction-level \(header\) fields and transaction line-level fields to capture on each quote.

## Configuration overview

Complete the following tasks to configure the quoting experience for your users considering the organization and implementation requirements.

-   [Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-stages.md) — Stages structure the quoting process into discrete phases. Each stage can have entry criteria, rule group associations, and stage-specific layout behavior including idle timeout and behavior on open.
-   [Quote transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-fields.md) — Fields store data on a quote at the transaction \(header\) level and the transaction line level. Quote Experience supports five field types: Text, Number, Boolean, Picklist, and Date/Time.
-   [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md) — Rules evaluate conditions and perform actions such as hiding fields, displaying messages, filtering picklist values, and setting or clearing field values. Rule groupings bundle rules together for assignment to stages and events.
-   [Quote transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-events.md) — Events are buttons or API triggers that run rule groups, call integrations, and drive stage transitions. Quote Experience provides system events for common operations and supports custom events for business-specific actions.
-   [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md) — Layouts define the quote user interface, controlling which fields, events, and UI effects appear and how the quote is organized into tiers, columnsets, and a line item grid.
-   [Quote transaction views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-views.md) — Views control field and event access permissions for each persona at each stage. A view defines which fields are editable, read-only, or hidden, and which events are active or unavailable.
-   [Quote transaction personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-personas.md) — Personas represent distinct user types in the quoting experience. Each persona is assigned to a view that defines its permissions at each stage of the quote lifecycle.
-   [Quote transaction integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-integrations.md) — Integrations connect Quote Experience to external data sources, enabling bidirectional data exchange between quotes and third-party systems using HTTP methods, connections, and transformation templates.
-   [Pricing setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-external-connection-logik.md) — Enable pricing for the deployment by setting up an external connection to the pricing service. For more information, see [Set up an external connection in CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-external-connection-logik.md). When pricing is set up, quote and line pricing fields are populated automatically and the quote can be repriced manually or automatically. For more information about repricing behavior, see [Transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-events.md).
-   [Advanced product filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-advanced-product-filtering.md) — Advanced product filtering dynamically controls which products appear in the quote catalog based on admin-defined rules and transaction context. Requires the `enableCatalogFilter` tenant setting.
-   [Quote Experience runtime API calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-runtime-api-calls.md) — Runtime APIs support headless quoting operations including initializing sessions, creating transactions, running events, and adding products via upsert.
-   [Quote Experience metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-metrics-api.md) — The metrics API retrieves usage analytics including views by user, session time, and time spent in each stage, with configurable date ranges defaulting to the last 30 days.

-   **[Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-stages.md)**  
Stages represent phases in the quoting process. Each stage can have entry criteria, rule group associations, and stage-specific layout behavior in CPQ.
-   **[Quote transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-fields.md)**  
ServiceNow Quote Experience supports five field types at two levels —transaction \(header\) and transaction line —enabling administrators to capture all required quote data in CPQ.
-   **[Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md)**  
Rules in ServiceNow Quote Experience evaluate conditions and perform actions on quote fields and layouts. Rule groupings bundle rules together to run at stages and events in CPQ.
-   **[Transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-events.md)**  
Events trigger rule groups, integrations, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.
-   **[Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md)**  
Layouts define the quote user interface in ServiceNow Quote Experience, controlling which fields, events, and UI effects are visible and how the quote is organized for users in CPQ.
-   **[Quote transaction views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-views.md)**  
Views control how users with specific personas can view and modify fields and events at each stage of a quote in CPQ.
-   **[Quote transaction integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-integrations.md)**  
Integrations connect ServiceNow Quote Experience to external data sources, enabling the exchange of data between quotes and third-party systems such as Salesforce in CPQ.
-   **[Quote transaction personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-personas.md)**  
Personas define distinct user types in the quoting experience, controlling what users can view and edit on a quote at each stage in CPQ.
-   **[Advanced product filtering for quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-advanced-product-filtering.md)**  
Advanced product filtering dynamically controls which products appear in the quote catalog based on admin-defined business rules and transaction context in CPQ.
-   **[ServiceNow Quote Experience: Access Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-transaction-manager-transaction-access-control.md)**  
ServiceNow Quote Experience controls access at two levels: record access, which determines who can view or modify a quote, and field access, which controls the fields a user sees within a quote. Record access can be managed by your CRM or natively within ServiceNow Quote Experience.
-   **[Quote Experience metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-metrics-api.md)**  
Reference for the Quote Experience metrics API, including query parameters, default behavior, and metric definitions for views, session time, and stage time in CPQ.
-   **[ServiceNow Quote Experience runtime API calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-runtime-api-calls.md)**  
Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a Postman collection for testing in CPQ.
-   **[Sync Primary Quote to Opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-sync-primary-quote-to-opportunity.md)**  
Designate a quote as primary and sync the quote's lines to the opportunity. When sync is enabled, any changes to the quote's lines are synced to the source opportunity lines. An opportunity can have only one quote marked as primary and enabled for sync.
-   **[Configure transaction-to-quote field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-opportunity-quote-mapping.md)**  
When you use Sales CRM capabilities such as opportunity management, advanced approvals, or PDF document generation, CPQ Microservices sync data to the ServiceNow platform. This sync is set up automatically, but custom transaction fields require you to configure the data mapping.
-   **[Enable order creation from a quote](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-create-order-integration.md)**  
Add the **Create Order** event to a blueprint layout so that users can create an order from a quote in the CPQ Quote experience.
-   **[Configure quote PDF documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management-configure-pdf-documents.md)**  
As a sales operation specialist, you can generate professional-looking PDF templates that present quotes in a standardized format that reflects company branding and logos. You can also set up Docusign to enable signers to sign quotes electronically and send them through email.
-   **[Customize a quote summarization skill in ServiceNow Otto for Configure, Price, Quote \(CPQ\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/customize-quote-summarization-skill.md)**  
Configure the ServiceNow Otto for Configure, Price, Quote \(CPQ\) application so that the agent can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.
-   **[Agentic AI application for quote generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/agentic-ai-app-quote-generation.md)**  
The Quote AI Agent is part of ServiceNow Otto for CPQ that interprets sales representative intent, retrieves opportunity and contract data, configures products, applies pricing and discounts, generates quote documents, and drafts client emails. Sales representatives review and approve each step before the agent proceeds. The Quote AI Agent uses an orchestrator that coordinates seven specialized agents.

**Parent Topic:**[Configuring the configure, price, quote applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-cpq.md)

