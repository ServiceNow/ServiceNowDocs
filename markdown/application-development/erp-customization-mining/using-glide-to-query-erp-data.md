---
title: Sample Glide query for ERP data in ERP Semantic Mining
description: Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ERP Semantic Mining reference, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Sample Glide query for ERP data in ERP Semantic Mining

Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[ERP Semantic Mining reference](erp-customization-mining-ref.md)

