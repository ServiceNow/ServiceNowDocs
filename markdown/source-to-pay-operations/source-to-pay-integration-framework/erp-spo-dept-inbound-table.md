---
title: Department Stage inbound staging table
description: The Department Stage inbound \[sn\_fcms\_intg\_department\_stage\] staging table temporarily stores important data about departments before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-dept-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Department Stage inbound staging table

The Department Stage inbound \[sn\_fcms\_intg\_department\_stage\] staging table temporarily stores important data about departments before this data is sent to the primary table.

The following table lists the fields for the Department Stage inbound \[sn\_fcms\_intg\_department\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Category ID/ERP Department ID|String|Unique ID of the Category or ERP department.|
|Department name|String|Name of the department.|
|Department head|String|Name of the head of the department.|
|Description|String|Description of the department.|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Primary contact|String|Primary contact details of the department.|

