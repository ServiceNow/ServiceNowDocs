---
title: Invoice error staging table
description: The Invoice error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Accounts Payable Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice error staging table

The Invoice error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier invoice number|String|Unique invoice number created by the supplier.|
|Supplier invoice line number|String|Unique identifier for each line item on a supplier invoice.|
|Sales order number|String|Unique identifier for a customer's purchase.|
|Sales order line number|String|Unique identifier for each item on a sales order.|

