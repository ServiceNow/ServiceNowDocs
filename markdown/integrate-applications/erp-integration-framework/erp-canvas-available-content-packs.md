---
title: Available Zero Copy Connector for ERP data products
description: The following data products are available for use in Zero Copy Connector for ERP to implement and deploy applications with less manual work.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, content, pack, content pack]
breadcrumb: [Data products, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Available Zero Copy Connector for ERP data products

The following data products are available for use in Zero Copy Connector for ERP to implement and deploy applications with less manual work.

## ERP Data Product for Enterprise Data Foundation

The ERP Data Product for Enterprise Data Foundation contains the following:

-   Master data models such as Read Cost Center, Read Customer Master, Read Vendor Data, Read Chart of Accounts, and Create/Update/Read Material Master.
-   SAP Foundation models are foundational models that may not be tied to a specific module or specific area in SAP. Some might be more related to finance or sales distribution, but foundational models commonly go across modules or areas. T
-   Enterprise Data Foundation Process Extensions such as Material Master Management, Get Material based on type, and Extend Material \(Sales\). Process extensions are small subflows that can use one or more models.

|Data Product contents|Target systems|Methods|
|---------------------|--------------|-------|
|Master data models|ECC and S/4|RFC/BAPI/OData V2|
|SAP Foundation models|ECC and S/4|RFC/BAPI/OData V2|
|Enterprise Data Foundation process extensions|ECC and S/4|RFC/BAPI/OData V2|

## ERP Data Product for Quote to Cash

The ERP Data Product for Quote to Cash contains the following:

-   Quote to Cash models including Create Sales Order, Update Sales Order, and Read Sales Order.
-   Quote to Cash process extensions including Manage Delivery &amp; Billing Block. Process extensions are small subflows that can use one or more models

|Data Product contents|Target systems|Methods|
|---------------------|--------------|-------|
|Models|ECC and S/4|RFC/BAPI/OData V2|
|Process extensions|ECC and S/4|RFC/BAPI/OData V2|

## ERP Data Product for Source to Settle

The ERP Data Product for Source to Settle contains models including Purchase Orders, Purchase Requisition, and Purchasing Info Record.

|Data Product contents|Target systems|Methods|
|---------------------|--------------|-------|
|Models|ECC and S/4|RFC/BAPI/OData V2|

**Parent Topic:**[Zero Copy Connector for ERP data products](erp-canvas-content-packs.md)

