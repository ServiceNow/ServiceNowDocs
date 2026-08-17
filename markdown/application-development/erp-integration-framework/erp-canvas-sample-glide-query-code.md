---
title: Sample Glide query for ERP data in ERP Canvas
description: Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-canvas-sample-glide-query-code.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ERP Canvas reference, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# Sample Glide query for ERP data in ERP Canvas

Access data from the ERP \(Enterprise Resource Planning\) system of record through the Glide API.

The following is an example of a Glide query that fetches a customer name.

```

var sap_customer_gr = new GlideRecord('sn_erp_integration_st_sap_sales_customer');
sap_customer_gr.get('customer_number', '100032');
sap_customer_gr.getValue('name');

```

**Parent Topic:**[ERP Canvas reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-integration-reference.md)

