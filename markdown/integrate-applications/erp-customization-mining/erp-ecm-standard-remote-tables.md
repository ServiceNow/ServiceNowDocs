---
title: Standard remote tables for ERP Semantic Mining
description: ERP Semantic Mining accesses several standard remote tables for ERP \(Enterprise Resource Planning\) data.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Standard tables and fields, Reference, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Standard remote tables for ERP Semantic Mining

ERP Semantic Mining accesses several standard remote tables for ERP \(Enterprise Resource Planning\) data.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

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

For more details on working with remote tables, see [Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

You can use any of the standard remote tables as data sources when building apps in ServiceNow products, such as:

-   [ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Workflow Studio flows, subflows, and actions](https://www.servicenow.com/docs/access?context=workflow-studio-flows-subflows-and-actions-landing&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Workflow Studio playbooks](https://www.servicenow.com/docs/access?context=workflow-studio-playbooks-landing&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Workspace Builder](https://www.servicenow.com/docs/access?context=workspace-builder-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)

You can also access data from the system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[ERP Semantic Mining standard tables and fields](erpcm-standard-fields-tables-reference-landing.md)

