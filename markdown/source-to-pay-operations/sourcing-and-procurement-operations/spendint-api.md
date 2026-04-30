---
title: SpendInt APIs
description: SpendInt APIs are inbound REST APIs that enable external procurement systems to send catalog, pricing, order, shipment, and invoice data into ServiceNow Sourcing and Procurement Operations, synchronizing structured procurement data from third-party systems.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-02-25"
reading_time_minutes: 3
keywords: [SpendInt API, inbound REST API, procurement integration, Source-to-Pay Integration Framework, catalog ingestion, price updates, order acknowledgements, shipment updates, invoice ingestion, sn\_spend\_intg]
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SpendInt APIs

SpendInt APIs are inbound REST APIs that enable external procurement systems to send catalog, pricing, order, shipment, and invoice data into ServiceNow Sourcing and Procurement Operations, synchronizing structured procurement data from third-party systems.

The SpendInt API is part of the Source-to-Pay Integration Framework and is provided in the `sn_spend_intg` namespace. It supports data-level, asynchronous integrations where third-party external systems send updates to ServiceNow after data changes occur in the source system.

## SpendInt API purpose and usage

SpendInt APIs are appropriate when procurement data is created or managed outside ServiceNow and must be pushed into ServiceNow to support purchasing, fulfillment, and financial workflows.

## Supported inbound data scenarios and APIs

Each inbound procurement scenario is handled by a dedicated SpendInt endpoint under the `/api/sn_spend_intg/spendint` path.

|Data scenario|Purpose|SpendInt API|
|-------------|-------|------------|
|Catalog ingestion|Create or update supplier products, product models, categories, and related attributes|`POST /sn_spend_intg/spendint/catalog`|
|Price updates|Update pricing for existing supplier product records|`POST /sn_spend_intg/spendint/price`|
|Availability updates|Update product availability or stock information|`POST /sn_spend_intg/spendint/availability`|
|Order acknowledgements|Send order confirmation details after a purchase is submitted|`POST /sn_spend_intg/spendint/orderack`|
|Shipment updates|Send shipping and delivery status for orders|`POST /sn_spend_intg/spendint/shipment`|
|Invoice ingestion|Send invoice data generated in third-party external systems into ServiceNow|`POST /sn_spend_intg/spendint/invoice`|

For details about individual APIs, request payloads, and field mappings, see [SpendInt APIs](https://www.servicenow.com/docs/access?context=spendint-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## How SpendInt APIs process data

SpendInt endpoints receive inbound payloads and write them to integration staging tables managed by the Source-to-Pay Integration Framework. The framework then validates and transforms the data into the appropriate procurement records, such as products, orders, shipments, or invoices.

This design separates data ingestion from record creation, allowing consistent handling of supplier data across integration scenarios.

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](../../../product/sourcing-procurement-operations/concept/integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management](../../../product/sourcing-procurement-operations/concept/spo-itam-better-together.md)

[Sourcing and Procurement Operations integration with Employee Center](../../../product/sourcing-procurement-operations/concept/employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](../../../product/sourcing-procurement-operations/concept/psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](../../../product/sourcing-procurement-operations/concept/better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](../../../product/sourcing-procurement-operations/concept/integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](../../../product/sourcing-procurement-operations/concept/integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](../../../product/sourcing-procurement-operations/concept/integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](../../../product/sourcing-procurement-operations/concept/integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../../../product/sourcing-procurement-operations/reference/erp-source-val-spo-objects.md)

[Procurement File Transfer Framework](../../../product/sourcing-procurement-operations/concept/procurement-file-transfer-framework.md)

