---
title: Quote to order flows
description: Quote to order \(Q2O\) automates the customer lifecycle from lead capture through contract acceptance to order fulfillment, reducing manual handoffs and order failures across sales and operations teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/quote-to-order-flows.html
release: brazil
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Quote to order flows

Quote to order \(Q2O\) automates the customer lifecycle from lead capture through contract acceptance to order fulfillment, reducing manual handoffs and order failures across sales and operations teams.

Q2O is part of the Unified \(USAM\) platform and integrates with catalog, billing, and fulfillment systems to manage the full customer lifecycle from lead capture through order decomposition.

Q2O produces the following outcomes:

-   Orders follow a consistent logical structure
-   Fulfillment and network operations teams receive properly formatted orders
-   Service activation requires fewer manual handoffs
-   Order failures are caught and escalated automatically

## Lead to order process flow

Q2O guides a sale through eight stages, from initial lead qualification to final order submission:

1.  Prospect identification and lead qualification: Sales identifies and qualifies a lead. A lead does not require a customer account, and lead line items are optional at this stage.
2.  Pre-order qualification: The qualified lead converts to an opportunity, which requires a customer account. The opportunity is created with product line items based on customer context.
3.  Sales agreement creation: A sales agreement establishes the commercial terms and conditions, including global SLAs, for the account.
4.  Quote configuration and pricing: A quote is created against the account. Service, site, and offer feasibility are evaluated for eligibility, compatibility, and pricing. Any required approvals, repricing, or sales solution design are triggered before the commercial configuration of the quote is confirmed.
5.  Sales contract creation: The confirmed quote, with its line items and summary, is captured in a sales contract.
6.  Service contract creation: A service contract defines entitlements and line-item-level SLAs for the account.
7.  Non-commercial order configuration: The quote converts to an order, order capture begins against the confirmed order, the billing account and profile are set up, and supporting documentation and references are created.
8.  Order submission: The completed order is validated and submitted for fulfillment.

## Order to fulfill process flow

After an order is submitted, Q2O decomposes the order and hands it off to fulfillment. The following diagram shows the conceptual order to fulfill process:

-   **Order Approval**

    Product Inventory is created in inactive state.

-   **Order Decomposition**
    -   Order Line Items are created for the Product Offerings and Product Specs.
    -   Domain Orders are created for the Product Specs, CFSS, RS, and RFSS \(if defined\).
-   **Instantiate Sub Flows and tasks**
    -   Sub Flows against every Domain order are instantiated.
    -   Sub Flow tasks are triggered.
    -   Processing can be in parallel, with task-level dependencies, or staggered.
-   **Instantiate special project**

    Project with tasks for fulfillment.

-   **Fall Out Management**

    Fall Out Task Management.

-   **Order Closure**
    -   Product Inventory is activated and populated with response params.
    -   Customer Order is closed as success.

\[Omitted image "mmasset0022311-1.png"\] Alt text: Infographic showing the order to fulfill process flow from order approval through order closure. Details are described in the surrounding text.\[Omitted image "mmasset0022312-92.png"\] Alt text: Infographic showing the quote to order process flow. Details are described in the surrounding text.

## Benefits

-   Automated order decomposition reduces time to activation and reduces manual order construction.
-   Catalog embedded decomposition rules promote consistent order structure and escalate failed orders automatically.
-   Consistent order structure reduces manual errors, rework, and missed SLAs.
-   Fulfillment systems receive properly formatted orders automatically, removing manual handoffs between sales and fulfillment teams.
-   Dynamic decomposition rules handle variant products and complex bundles without additional catalog entries.
-   End-to-end tracking across decomposition, assignment, and execution stages gives sales and operations shared visibility.

