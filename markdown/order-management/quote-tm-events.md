---
title: Transaction events
description: Events trigger rule groups, integrations, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-events.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Transaction events

Events trigger rule groups, integrations, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.

Events are activated by buttons on the quote layout or by API calls, and typically help users transition quotes from one stage to another. When an event fires, it can run rule groupings, call integrations, and trigger stage transitions.

## Header-level system events

System events are standard behaviors provided by default. When the ServiceNow Quote Experience is embedded in CPQ, the user sees buttons on the quote interface corresponding to transaction-level events.

Transaction-level system events:

-   **Create Transaction**

    Triggered to create a new transaction.

-   **Update Transaction**

    Allows editing an updating a transaction.

-   **Copy Transaction**

    Clones a transaction and its line items.

-   **Upsert Lines**

    Manages the creation and update of transaction lines after the user browses the catalog to add new lines or reconfigures an existing line. Upsert Lines runs automatically after the user finishes selecting products from the catalog, configuring products, or reconfiguring a line. Although it works on lines, it operates at the transaction level on all lines. When pricing is enabled, this event ships with the **Reprice** action attached so that adding or reconfiguring a product automatically reprices the quote. For more information about UI effects, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md).

-   **Reprice**

    Recalculates pricing for the quote by assembling the pricing context from the header and line values and calling the pricing service. The response is mapped back onto the quote and line pricing fields. Available when pricing is enabled for the deployment. The **Reprice** action can be attached to a button on the quote layout for manual repricing and to system events, such as Upsert Lines, for automatic repricing.

-   **Delete Transaction**

    Triggered to delete an existing transaction.


Transaction line-level system events are represented as buttons on the quote lines grid:

-   **Clone Line**

    Clones a line and its children. Only top-level lines in the transaction can be cloned. Header-level rules also apply after cloning.

-   **Delete Lines**

    Deletes one or more selected lines from the transaction. Line IDs can also be passed in headless mode.

-   **Reconfigure**

    Re-configure one or more selected lines from the transaction. Line IDs can also be passed in headless mode.


## Repricing events

When Pricing is enabled, the **Reprice** action drives both manual and automatic repricing. To enable Pricing, see [Set up an external connection in CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-external-connection-logik.md)

-   Manual reprice — Attach the **Reprice** action to a button on the quote layout so users can recalculate pricing on demand.
-   Automatic reprice — Default special-event triggers, such as **upsertLines** when a configuration is added, ship with the **Reprice** action attached, so pricing runs without the user selecting **Reprice**. You can disable these default triggers per event if you don't want automatic repricing for a given event.
-   Stage-aware behavior — The effective repricing behavior can differ by stage without per-event configuration. For example, auto-pricing can be aggressive in an early stage such as Draft and suppressed in a later stage such as Order Submitted. Configure stage-specific behavior on the stage. For more information, see [Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-stages.md).

## Event APIs

Event APIs are authorized via session cookie only.

**Warning:** Avoid building a scenario in which the user initiates an event that fires an event API on the same transaction. Because both the quote interface and the APIs act on the same record simultaneously, such an implementation can result in unpredictable behavior.

## Event setting: Validate configured items

The **Validate configured items** setting on custom header events validates product configurations in the transaction when the event executes. Validation occurs before event actions, which execute regardless of the validation outcome.

The setting includes a validity period that excludes products validated within a specified time frame. For example, if the validity period is 15 days and a product was validated 7 days ago, that product is not revalidated. If a product was validated 20 days ago, it is revalidated.

Two line-level system fields support this function: **txn.line.configuration.status** \(Boolean\) and **txn.line.configuration.validatedAt** \(date\).

-   **[Create an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-custom-event.md)**  
Create a custom event in ServiceNow Quote Experience to trigger rule groupings, integrations, and stage transitions based on business-specific requirements in CPQ.

**Parent Topic:**[Configuring ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-crm-tm-quoting-configure.md)

**Related topics**  


[Create an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-custom-event.md)

