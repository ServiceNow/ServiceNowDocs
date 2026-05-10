---
title: Sales CRM Pricing API
description: The Sales CRM Pricing API provides methods to calculate prices for transaction lines containing products.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-09-26"
reading_time_minutes: 2
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Sales CRM Pricing API

The Sales CRM Pricing API provides methods to calculate prices for transaction lines containing products.

The Sales CRM Pricing is used to calculate prices for transaction lines containing products. It also supports computing rollups at the transaction header level by aggregating values from all lines. In addition, the Pricing Engine can be used within a configurator to determine the price of products as they are selected or configured.

The caller has flexibility through various controls to specify whether the engine should compute:

-   Prices only
-   Costs
-   Adjustments \(discounts, markup\)
-   Rollups at line and/or header level

This API belongs to the sn\_csm\_pricing namespace and requires the \[sn\_csm\_pricing.pricing\_integrator\] role.

Prerequisite: You need to set up a product offering that consists of these properties:

-   Required:
    -   Product offering characteristics
    -   Unit of measure
    -   Price list
    -   Price list lines
    -   Attribute adjustments
-   Optional
    -   Context variables
    -   Rule matrices

## External ID support

With external ID resolution, you can use your own identifiers or codes for selected reference fields instead of a ServiceNow sys\_id. For example, you might be integrating with other CRM or ERP systems that do not have a ServiceNow sys\_id for its objects. You can use external codes for the following reference fields, including but not limited to:

-   Product offering
-   Price list
-   Unit of measure

**Note:** External ID resolution applies to REST API pricing requests only and does not affect UI-based flows. Pricing execution can use internal system IDs, external IDs, or a combination of both IDs in pricing requests as configured in the context variable mapping.

Context variable configuration and mapping

As an admin, before submitting a REST API pricing request, create the context variables that define the reference fields for external IDs or codes that are participating in external ID resolution. You also add the external IDs or codes to the reference tables called by pricing requests. For details on defining context variables, see [External ID support in Sales CRM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/external-ids-pricingapi.md).

How external IDs work in pricing requests

**Request intake**

The caller sends a Pricing REST API request that can include:

-   External IDs or codes
-   ServiceNow sys\_ids
-   A combination of both

Requests must include \(`"use_external_code": true`\) in the settings object to enable external code resolution.

-   **[Sales CRM Pricing - DELETE - /api/sn\_csm\_pricing/v1/pricingengine/pricing\_context/\{pricing\_context\_id\}](../reference/sales_crm_pricing-DELETE-pricing-context-id.md)**  
Terminate a session with a given ID that was established during a configurator session.
-   **[Sales CRM Pricing - POST /api/sn\_csm\_pricing/\{api\_version\}/pricingengine/computePrice](../reference/sales_crm_pricing-POST-compute-price.md)**  
Enables callers to compute the price of products specified in the request payload. The pricing settings included in the payload determine and control the execution flow of the Pricing Engine, such as whether to apply validations, adjustments, or rollups.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

