---
title: Standard remote tables for Zero Copy Connector for ERP
description: Zero Copy Connector for ERP \(Enterprise Resource Planning\) accesses several standard remote tables for ERP models.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, standard, remote, table, model]
breadcrumb: [Standard tables, fields, and models, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Standard remote tables for Zero Copy Connector for ERP

Zero Copy Connector for ERP \(Enterprise Resource Planning\) accesses several standard remote tables for ERP models.

The following remote tables are available through Zero Copy Connector for ERP and ERP Semantic Mining.

|Label|Name|ERP module|
|-----|----|----------|
|SAP Company Code|sn\_erp\_integration\_st\_sap\_company\_code|Basis|
|SAP Country|sn\_erp\_integration\_st\_sap\_country|Basis|
|SAP Currency|sn\_erp\_integration\_st\_sap\_currency|Basis|
|SAP Language|sn\_erp\_integration\_st\_sap\_language|Basis|
|SAP Material Stock|sn\_erp\_integration\_st\_sap\_material\_stock|Procurement|
|SAP Purchase Document|sn\_erp\_integration\_st\_sap\_purchase\_document|Procurement|
|SAP Purchasing Organization|sn\_erp\_integration\_st\_sap\_purchasing\_organization|Procurement|
|SAP Customer Invoice|sn\_erp\_integration\_st\_sap\_customer\_invoice|Sales|
|SAP Distribution Channel|sn\_erp\_integration\_st\_sap\_distribution\_channel|Sales|
|SAP Division|sn\_erp\_integration\_st\_sap\_division|Sales|
|SAP Sales Customer|sn\_erp\_integration\_st\_sap\_sales\_customer|Sales|
|SAP Sales Delivery|sn\_erp\_integration\_st\_sap\_sales\_delivery|Sales|
|SAP Sales Document|sn\_erp\_integration\_st\_sap\_sales\_document|Sales|
|SAP Sales Organization|sn\_erp\_integration\_st\_sap\_sales\_organization|Sales|
|SAP Sales Revenue Recognition|sn\_erp\_integration\_st\_sap\_sales\_revenue\_recognition|Sales|
|SAP Vendor|sn\_erp\_integration\_st\_sap\_vendor|Sales|
|SAP Vendor Invoice|sn\_erp\_integration\_st\_sap\_vendor\_invoice|Sales|
|SAP Transport|sn\_erp\_integration\_st\_sap\_transport|Transport|

For more details on working with remote tables, see Remote tables.

You can use any of the standard remote tables as data sources when building apps in ServiceNow products, such as:

-   ServiceNow Studio
-   Workflow Studio flows, subflows, and actions
-   Workflow Studio playbooks
-   Table Builder
-   UI Builder
-   Workspace Builder

You can also access data from the system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[Zero Copy Connector for ERP standard tables, fields, and models](erp-canvas-standard-tables-and-fields-landing.md)

