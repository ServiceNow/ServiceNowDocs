---
title: Sample Glide query for ERP data in ERP Data Hub
description: Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Sample Glide query for ERP data in ERP Data Hub

Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[ERP Data Hub reference](erp-integration-reference.md)

