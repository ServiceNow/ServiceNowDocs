---
title: Transaction events
description: Events trigger rule groups, integrations, repricing, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-events.html
release: brazil
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Transaction events

Events trigger rule groups, integrations, repricing, and stage transitions on a quote. ServiceNow Quote Experience provides system events and supports custom events in CPQ.

Events are activated by buttons on the quote layout or by API calls.

## Header-level system events

System events are standard behaviors provided by default.

Transaction-level system events:

-   **Create Transaction**

    Triggered to create a new transaction.

-   **Update Transaction**

    Allows editing an updating a transaction.

-   **Copy Transaction**

    Clones a transaction and its line items.

-   **Upsert Lines**

    Manages the creation and update of transaction lines after the user browses the catalog to add new lines or reconfigures an existing line. Upsert Lines runs automatically after the user finishes selecting products from the catalog, configuring products, or reconfiguring a line. Although it works on lines, it operates at the transaction level on all lines. When pricing is enabled, this event ships with the **Reprice** action attached so that adding or reconfiguring a product automatically reprices the quote. For more information about UI effects, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-layouts.md).

-   **Delete Transaction**

    Triggered to delete an existing transaction.


Transaction line-level system events are represented as buttons on the quote lines grid:

-   **Clone Line**

    Clones a line and its children. Only top-level lines in the transaction can be cloned. Header-level rules also apply after cloning.

    By default, cloning a line creates a single copy and no dialog appears.

    To let runtime users create multiple copies of a line in a single action, submit a support request to have the tenant setting **transaction.events.cloneLine.multiCopy.enabled** to `true`. With the setting enabled, selecting a single line and cloning it opens a dialog in which the user specifies the number of copies to create. The line and its children are cloned that many times, for both standard and configurable products.

    Multiple copies apply to a single selected line only. If the user selects more than one line, each selected line is cloned once and no dialog appears. The max number of copies is 10.

-   **Delete Lines**

    Deletes one or more selected lines from the transaction. Line IDs can also be passed in headless mode.

-   **Reconfigure**

    Re-configure one or more selected lines from the transaction. Line IDs can also be passed in headless mode.


## Repricing event actions

When Pricing is enabled, the **Reprice** action can be added to an event. The Reprice action includes a call to the Pricing Management service during the execution of an event, enabling explicit **Reprices** by a user or via API. To enable Pricing, see [Pricing in the ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-in-quote-experience.md)

## Event APIs

Event APIs are authorized via session cookie only.

**Warning:** Avoid building a scenario in which the user initiates an event that fires an event API on the same transaction. Because both the quote interface and the APIs act on the same record simultaneously, such an implementation can result in unpredictable behavior.

## Event setting: Validate configured items

The **Validate configured items** setting on custom header events validates product configurations in the transaction when the event executes. Validation occurs before event actions, which execute regardless of the validation outcome.

The setting includes a validity period that excludes products validated within a specified time frame. For example, if the validity period is 15 days and a product was validated 7 days ago, that product is not revalidated. If a product was validated 20 days ago, it is revalidated.

Two line-level system fields support this function: **txn.line.configuration.status** \(Boolean\) and **txn.line.configuration.validatedAt** \(date\).

**Related topics**  


[Create an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-create-custom-event.md)

