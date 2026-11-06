---
title: Available Zero Copy Connector for ERP content packs for SAP
description: Compare the Zero Copy Connector for ERP content packs for Enterprise Data Foundation, Hire to Retire, Quote to Cash, and Source to Settle. Details include the SAP models, target systems, and methods that each pack contains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-canvas-available-content-packs.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [sap, zero copy connector for erp, erp content pack, enterprise data foundation, hire to retire, quote to cash, source to settle, sap master data model, sap ecc, sap s/4hana, bapi, odata v2]
breadcrumb: [Content packs, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Available Zero Copy Connector for ERP content packs for SAP

Compare the Zero Copy Connector for ERP content packs for Enterprise Data Foundation, Hire to Retire, Quote to Cash, and Source to Settle. Details include the SAP models, target systems, and methods that each pack contains.

## ERP Content Pack for Enterprise Data Foundation

The ERP Content Pack for Enterprise Data Foundation contains the following:

-   Master data models such as Read Cost Center, Read Customer Master, Read Vendor Data, Read Chart of Accounts, and Create/Update/Read Material Master.
-   SAP Foundation models are foundational models that may not be tied to a specific module or specific area in SAP. Some might be more related to finance or sales distribution, but foundational models commonly go across modules or areas.
-   Enterprise Data Foundation Process Extensions such as Material Master Management, Get Material based on type, and Extend Material \(Sales\). Process extensions are small subflows that can use one or more models.

|Content pack contents|Target systems|Methods|
|---------------------|--------------|-------|
|Master data models|ECC and S/4|RFC/BAPI/OData V2|
|SAP Foundation models|ECC and S/4|RFC/BAPI/OData V2|
|Enterprise Data Foundation process extensions|ECC and S/4|RFC/BAPI/OData V2|

## ERP Content Pack for Hire to Retire

The ERP Content Pack for Hire to Retire contains models including Candidate, Job Application, and Position.

|Content pack contents|Target systems|Methods|
|---------------------|--------------|-------|
|Models|ECC and S/4|OData V2|

## ERP Content Pack for Quote to Cash

The ERP Content Pack for Quote to Cash contains the following:

-   Quote to Cash models including Create Sales Order, Update Sales Order, and Read Sales Order.
-   Quote to Cash process extensions including Manage Delivery &amp; Billing Block. Process extensions are small subflows that can use one or more models.

|Content pack contents|Target systems|Methods|
|---------------------|--------------|-------|
|Models|ECC and S/4|RFC/BAPI/OData V2|
|Process extensions|ECC and S/4|RFC/BAPI/OData V2|

## ERP Content Pack for Source to Settle

The ERP Content Pack for Source to Settle contains models including Purchase Orders, Purchase Requisition, and Purchasing Info Record.

|Content pack contents|Target systems|Methods|
|---------------------|--------------|-------|
|Models|ECC and S/4|RFC/BAPI/OData V2|

