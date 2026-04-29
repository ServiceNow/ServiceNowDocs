---
title: Sample Glide query for ERP data in Zero Copy Connector for ERP
description: Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, sample, example, snippit, glide, query, code]
breadcrumb: [Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Sample Glide query for ERP data in Zero Copy Connector for ERP

Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[Zero Copy Connector for ERP reference](erp-integration-reference.md)

