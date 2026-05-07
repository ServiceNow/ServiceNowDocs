---
title: Zero Copy Connector for ERP Source to Settle content pack models
description: The Zero Copy Connector for ERP \(Enterprise Resource Planning\) Source to Settle content pack contains models that you may need when interacting with an SAP system.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, content, pack, content pack, source, settle, model, integration, data hub, zero, copy, connector, sap]
breadcrumb: [Source to Settle content pack, Available content packs, Content packs, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP Source to Settle content pack models

The Zero Copy Connector for ERP \(Enterprise Resource Planning\) Source to Settle content pack contains models that you may need when interacting with an SAP system.

## Source to Settle content pack models

|Model name|Short description|Model type|Methods|
|----------|-----------------|----------|-------|
|Purchase Order|Retrieve information about a purchase order based on a purchase order number.|ERP|RFC/BAPI|
|Purchase Order - Header|Retrieve purchase order header information such as vendor, currency, and payment terms, based on a purchase order number.|Platform|OData V2|
|Purchase Order - Header|Retrieve purchase order header information such as vendor, currency, and payment terms, based on a purchase order number.|Platform|RFC/BAPI|
|Purchase Order Item - Item|Retrieve details about a specific line item on a purchase order based on a purchase order number and line item number.|Platform|OData V2|
|Purchase Order - Item|Retrieve details about a specific line item on a purchase order based on a purchase order number and line item number.|Platform|RFC/BAPI|
|Purchase Order - List|Retrieve a list of all items \(along with their item numbers and details\) on a purchase order based on a purchase order number.|ERP|RFC/BAPI|
|Purchase Requisition|Retrieve information about a specific purchase requisition, such as the quantity of a material or service and the date needed.|ERP|RFC/BAPI|
|Purchase Requisitions - List|Retrieve a list of purchase requisitions.|ERP|RFC/BAPI|
|Purchasing Info Record|Retrieve details about a specific purchasing info record, such as prices, conditions, and sources for materials.|ERP|RFC/BAPI|

**Parent Topic:**[Zero Copy Connector for ERP Source to Settle content pack](../concept/erp-source-to-settle-data-product.md)

