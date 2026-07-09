---
title: Cost Center Stage inbound staging table
description: The Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table temporarily stores important data about cost centers before this data is sent to the primary table. You can use this table to lookup all the cost center details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-cost-center-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Cost Center Stage inbound staging table

The Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table temporarily stores important data about cost centers before this data is sent to the primary table. You can use this table to lookup all the cost center details.

The following table lists the fields for the Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Account number|String|Account number of the cost center|
|Available for user|String|Users that are applicable to the cost center|
|Code|String|Code of the cost center|
|Cost center type|String|Type of cost center|
|Controlling area|String|Controlling area of the cost center|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Legal entity|String|Detailed information about individual suppliers, including banking details, payment methods, and credit terms.|
|Manager|String|Name of the manager of the cost center|
|Name|String|Name of the cost center|
|Profit center|String|Profit centers within the organization, enabling financial reporting and analysis by business units or operational segments.|
|Valid from|String|Date the cost center is valid from|
|Valid to|String|Date the cost center is valid to|

