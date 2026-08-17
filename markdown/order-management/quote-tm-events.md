---
title: Transaction events
description: Events trigger rule groups, integrations, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-events.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Transaction events

Events trigger rule groups, integrations, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.

Events are activated by buttons on the Quote layout or API calls on the quote layout and typically helpuserscan transition quotes from one stage to another. When an event fires, it can run rule groupings, call integrations, and trigger stage transitions.

## Header-level system events

System events are standard behaviors provided by default. When Transaction Manager is embedded in Sales CRM, the user sees buttons on the quote interface corresponding to transaction-level events.

Transaction-level system events:

-   **Create Transaction**

    Triggered to create a new transaction.

-   **Update Transaction**

    Allows editing an updating a transaction.

-   **Copy Transaction**

    Clones a transaction and its line items.

-   **Upsert Lines**

    Manages the creation and update of transaction lines after the user browses the catalog to add new lines or reconfigures an existing line. Upsert Lines runs automatically after the user finishes selecting products from the catalog, configuring products, or reconfiguring a line. Although it works on lines, it operates at the transaction level on all lines. For more information about UI effects, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md).

-   **Delete Transaction**

    Triggered to delete an existing transaction.


Transaction line-level system events are represented as buttons on the quote lines grid:

-   **Clone Line**

    Clones a line and its children. Only top-level lines in the transaction can be cloned. Header-level rules also apply after cloning.

-   **Delete Lines**

    Deletes one or more selected lines from the transaction. Line IDs can also be passed in headless mode.


-   **Reconfigure**

    Re-configure one or more selected lines from the transaction. Line IDs can also be passed in headless mode.


## Event APIs

Event APIs are authorized via session cookie only.

**Warning:** Avoid building a scenario in which the user initiates an event that fires an event API on the same transaction. Because both the quote interface and the APIs act on the same record simultaneously, such an implementation can result in unpredictable behavior.

## Event setting: Validate configured items

The **Validate configured items** setting on custom header events validates product configurations in the transaction when the event executes. Validation occurs before event actions, which execute regardless of the validation outcome.

The setting includes a validity period that excludes products validated within a specified time frame. For example, if the validity period is 15 days and a product was validated 7 days ago, that product is not revalidated. If a product was validated 20 days ago, it is revalidated.

Two line-level system fields support this function: **txn.line.configuration.status** \(Boolean\) and **txn.line.configuration.validatedAt** \(date\).

**Related topics**  


[Create an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-custom-event.md)

