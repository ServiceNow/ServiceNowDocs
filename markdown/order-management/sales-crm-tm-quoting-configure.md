---
title: Configuring CPQ Quote Experience
description: Configuration tasks and sequence for setting up the CPQ Quote Experience with Quote Experience for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-crm-tm-quoting-configure.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring CPQ Quote Experience

Configuration tasks and sequence for setting up the CPQ Quote Experience with Quote Experience for your organization.

Configure the Quote Experience to control the quote layout and behavior for your users — the fields they see, how pricing is calculated, which approvals are required, and what actions are available at each stage of the quote lifecycle.

Complete the required configuration tasks in order before you enable the quoting experience for your users. Complete optional tasks based on your implementation requirements.

## Quote Experience

Using CPQ Quote Experience, administrators can:

-   Access and configure stages, associated fields, related rules, rule groups, events, layouts, views, and personas.
-   Define the sales workflow stages your organization needs and define the conditions that must be true before a transaction can enter each stage.
-   Identify the transaction-level \(header\) fields and transaction line-level fields to capture on each quote.

## Configuration overview

Complete the following tasks to configure the quoting experience.

-   [Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-stages.md) — Stages structure the quoting process into discrete phases. Each stage can have entry criteria, rule group associations, and stage-specific layout behavior including idle timeout and behavior on open.
-   [Quote transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-fields.md) — Fields store data on a quote at the transaction \(header\) level and the transaction line level. Quote Experience supports five field types: Text, Number, Boolean, Picklist, and Date/Time.
-   [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md) — Rules evaluate conditions and perform actions such as hiding fields, displaying messages, filtering picklist values, and setting or clearing field values. Rule groupings bundle rules together for assignment to stages and events.
-   [Quote transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-events.md) — Events are buttons or API triggers that run rule groups, call integrations, and drive stage transitions. Quote Experience provides system events for common operations and supports custom events for business-specific actions.
-   [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md) — Layouts define the quote user interface, controlling which fields, events, and UI effects appear and how the quote is organized into tiers, columnsets, and a line item grid.
-   [Quote transaction views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-views.md) — Views control field and event access permissions for each persona at each stage. A view defines which fields are editable, read-only, or hidden, and which events are active or unavailable.
-   [Quote transaction personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-personas.md) — Personas represent distinct user types in the quoting experience. Each persona is assigned to a view that defines its permissions at each stage of the quote lifecycle.
-   [Quote transaction integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-integrations.md) — Integrations connect Quote Experience to external data sources, enabling bidirectional data exchange between quotes and third-party systems using HTTP methods, connections, and transformation templates.
-   [Advanced product filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-advanced-product-filtering.md) — Advanced product filtering dynamically controls which products appear in the quote catalog based on admin-defined rules and transaction context. Requires the `enableCatalogFilter` tenant setting.
-   [Quote Experience runtime API calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-runtime-api-calls.md) — Runtime APIs support headless quoting operations including initializing sessions, creating transactions, running events, and adding products via upsert.
-   [Quote Experience metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-metrics-api.md) — The metrics API retrieves usage analytics including views by user, session time, and time spent in each stage, with configurable date ranges defaulting to the last 30 days.

