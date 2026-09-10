---
title: SpendInt APIs
description: SpendInt APIs allow external procurement systems to send catalog, pricing, order, shipment, and invoice data to ServiceNow, synchronizing procurement data from third-party systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spendint-api-spo.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-02-26"
reading_time_minutes: 4
keywords: [SpendInt API, inbound REST API, procurement integration, Source-to-Pay Integration Framework, catalog ingestion, price updates, order acknowledgements, shipment updates, invoice ingestion, sn\_spend\_intg]
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SpendInt APIs

SpendInt APIs allow external procurement systems to send catalog, pricing, order, shipment, and invoice data to ServiceNow, synchronizing procurement data from third-party systems.

The Source-to-Pay Integration Framework provides the SpendInt API in the **sn\_spend\_intg** namespace. The API supports data-level, asynchronous integrations where external systems send updates to ServiceNow after the source system changes data.

## Purpose and usage

SpendInt APIs are appropriate when procurement data is created or managed outside ServiceNow and must be pushed into ServiceNow to support purchasing, fulfillment, and financial workflows.

## Supported data scenarios

A dedicated SpendInt endpoint under the `/api/**sn\_spend\_intg**/spendint` path handles each inbound procurement scenario.

|Data scenario|Purpose|SpendInt API|
|-------------|-------|------------|
|Catalog ingestion|Create or update supplier products, product models, categories, and related attributes|`POST /**sn\_spend\_intg**/spendint/catalog`|
|Price updates|Update pricing for existing supplier product records|`POST /**sn\_spend\_intg**/spendint/price`|
|Availability updates|Update product availability or stock information|`POST /**sn\_spend\_intg**/spendint/availability`|
|Order acknowledgements|Send order confirmation details after a purchase is submitted|`POST /**sn\_spend\_intg**/spendint/orderack`|
|Shipment updates|Send shipping and delivery status for orders|`POST /**sn\_spend\_intg**/spendint/shipment`|
|Invoice ingestion|Send invoice data generated in external systems into ServiceNow|`POST /**sn\_spend\_intg**/spendint/invoice`|

For details about individual APIs, request payloads, and field mappings, see the SpendInt API reference documentation.

## Data processing

SpendInt endpoints receive inbound payloads and write them to integration staging tables managed by the Source-to-Pay Integration Framework. The framework then validates and transforms the data into the appropriate procurement records, such as products, orders, shipments, or invoices.

This design separates data ingestion from record creation, allowing consistent handling of supplier data across integration scenarios.

## Model matching during catalog ingestion

During catalog ingestion, the framework determines a supplier product's model through two paths. By default, the framework uses manufacturer part number matching. When a Software Product Definition is found, SAM Pro uses that definition instead.

-   **Hardware Asset Management \(HAM\), Enterprise Asset Management \(EAM\), Software Asset Management \(SAM\) without Pro, and SAM Pro when no Software Product Definition is found**
    -   The system searches for a model using the manufacturer part number and manufacturer.
    -   If found, the model is assigned to the supplier product. Otherwise, a new model is created.
    -   If the manufacturer part number is empty, the supplier part number is used as the model number.
    -   Supplier part number is mandatory and determines whether the supplier product is created or updated.
-   **SAM Pro when Software Product Definition is found**
    -   The manufacturer part number is matched to the publisher part number on the Software Product Definition.
    -   SAM Pro uses that definition to find or create the canonical software model.
    -   The imported manufacturer is not used in this path.
    -   The canonical model is assigned to the supplier product.

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with Asset Management]()

[Sourcing and Procurement Operations integration with Employee Center]()

[Sourcing and Procurement Operations integration with third-party sourcing solutions]()

[Sourcing and Procurement Operations integration with Third-party Risk Management]()

[Sourcing and Procurement Operations integration with Project Management]()

[Sourcing and Procurement Operations integration with Celonis]()

[Sourcing and Procurement Operations integration with Field Service Management]()

[Source-to-Pay Operations integration with Contract Management Pro]()

[ERP source validation on Sourcing and Procurement Operations objects]()

[Procurement File Transfer Framework]()

