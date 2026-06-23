---
title: Standard remote tables for ERP-CM
description: ERP Semantic Mining \(ERP-CM\) accesses several standard remote tables for ERP \(Enterprise Resource Planning\) data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-customization-mining/erp-ecm-standard-remote-tables.html
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ERP-CM standard tables and fields, ERP Semantic Mining reference, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Standard remote tables for ERP-CM

ERP Semantic Mining \(ERP-CM\) accesses several standard remote tables for ERP \(Enterprise Resource Planning\) data.

The following remote tables are available through Zero Copy Connector for ERP and ERP-CM.

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

For more details on working with remote tables, see [Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/remote-tables/remote-tables.md).

You can use any of the standard remote tables as data sources when building apps in ServiceNow products, such as:

-   [App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/app-engine-studio/aes-overview.md)
-   [Flows in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/exploring-flows.md)
-   [Playbooks in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/exploring-process-automation-designer.md)
-   [Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/form-builder-glide-family-release/tb-landing-page.md)
-   [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/ui-builder/ui-builder-overview.md)
-   [Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/workspace-builder/add-workspace.md)

You can also access data from the system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[ERP-CM standard tables and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-customization-mining/erpcm-standard-fields-tables-reference-landing.md)

