---
title: Zero Copy Connector for ERP Source to Settle data product models
description: The Zero Copy Connector for ERP Source to Settle data product contains models that you may need when interacting with an SAP system.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Source to Settle data product, Data products, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP Source to Settle data product models

The Zero Copy Connector for ERP Source to Settle data product contains models that you may need when interacting with an SAP system.

## Source to Settle data product models

|Model name|Short description|Model type|Protocol|
|----------|-----------------|----------|--------|
|Purchase Order Item List \(available starting in the Zurich Patch 4 release\)|Retrieve details about a specific line item on a purchase order based on a purchase order number and line item number.|Platform|OData V2|
|Purchase Order Item List \(available starting in the Zurich Patch 4 release\)|Retrieve details about a specific line item on a purchase order based on a purchase order number and line item number.|Platform|RFC/BAPI|
|Purchase Order List \(available starting in the Zurich Patch 4 release\)|Retrieve a list of all items \(along with their item numbers and details\) on a purchase order based on a purchase order number.|Platform|OData V2|
|Purchase Order List \(available starting in the Zurich Patch 4 release\)|Retrieve a list of all items \(along with their item numbers and details\) on a purchase order based on a purchase order number.|Platform|RFC/BAPI|
|Purchase Orders|Retrieve information about a specific purchase order, such as the supplier and the quantity of goods or services.|ERP|RFC/BAPI|
|Purchase Orders - List|Retrieve a list of purchase orders.|ERP|RFC/BAPI|
|Purchase Requisition|Retrieve information about a specific purchase requisition, such as the quantity of a material or service and the date needed.|ERP|RFC/BAPI|
|Purchase Requisitions - List|Retrieve a list of purchase requisitions.|ERP|RFC/BAPI|
|Purchasing Info Record|Retrieve details about a specific purchasing info record, such as prices, conditions, and sources for materials.|ERP|RFC/BAPI|

**Parent Topic:**[Zero Copy Connector for ERP Source to Settle data product](../concept/erp-source-to-settle-data-product.md)

