---
title: External ID support in Sales CRM Pricing API
description: The Sales CRM Pricing API supports external IDs in pricing requests. You can use your own custom identifiers or codes for selected reference fields instead of a ServiceNow sys\_id.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 3
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# External ID support in Sales CRM Pricing API

The Sales CRM Pricing API supports external IDs in pricing requests. You can use your own custom identifiers or codes for selected reference fields instead of a ServiceNow sys\_id.

For example, a pricing call can originate from other CRM or ERP systems that may have different identifiers for certain objects. You can map these unique identifiers to ServiceNow reference fields using an external ID, code, or other custom field. A pricing call can then be made using these unique identifiers available on the external system.

You can use external codes for the following reference fields \(objects\), including but not limited to:

-   Product offering
-   Top-level product offering
-   Unit of measure
-   Price list
-   Cost book
-   Characteristics and characteristic options
-   Pricing adjustment type
-   Account

**Note:** External IDs apply to REST API pricing requests and do not affect UI‑based flows. Pricing execution can use internal system IDs, external IDs, or a combination of both IDs in pricing requests. For more information on the pricing API, see Sales CRM Pricing API.

## How external IDs work in pricing requests

External IDs map to reference fields in ServiceNow reference tables. As an admin, before submitting a pricing request, create the context variables that define the reference fields for external IDs or codes that map to a column in a specified reference table. For more information, see [Configure context variables for external IDs](../task/configure-external-ids-pricing-requests.md).

Processing of a pricing request with external IDs involves the following phases:

-   **Request intake**

    The caller sends a Pricing REST API request that can include:

    -   External IDs or codes
    -   sys\_ids
    -   A combination of both external IDs and sys\_ids
    In your request, you set a request flag \(`"use_external_code:true"`\) that enables external ID support.

-   **Resolution**

    For each configured reference field, the system attempts to resolve the external value to an internal sys\_id.

    -   Resolution is driven by context variable configuration.
    -   If resolution fails and no sys\_id is provided, the request fails.
-   **Account resolution using external identifiers**

    Accounts are resolved using context variables rather than request payload fields.

    -   External account identifiers are resolved before pricing execution.
    -   Resolved account sys\_ids are used internally for pricing execution.
    -   Original external identifiers are retained for response construction.
-   **Pricing execution**

    All downstream pricing logic runs only on resolved sys\_ids. Pricing logic is unaware of whether the original value was an external code or a sys\_id.

-   **Response construction**

    The response reflects the identifiers provided in the request \(external codes or sys\_ids\). Resolved sys\_ids are not exposed to the caller.

-   **Error handling**

    The system validates all reference identifiers during request processing. Common errors include the following scenarios:

    -   External identifier does not exist in the reference table.
    -   External code usage is enabled but no context variable mapping exists for an enabled field.
    -   Neither a sys\_id nor external code is provided.
    -   Identifier value is not valid.
    Errors are reported at the line level and identify the failed line item. Error messages may vary depending on the configuration and validation context.

    If errors occur, verify the following items:

    -   Context variable mappings
    -   External identifier values
    -   Request flag usage

## Context variable configuration and mapping

As an admin, before submitting a REST API pricing request that uses external IDs, create the context variables that map to columns in selected ServiceNow reference tables. For more information, see [Configure context variables for external IDs](../task/configure-external-ids-pricing-requests.md).

