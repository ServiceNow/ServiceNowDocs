---
title: Purchase Entity Stage inbound staging table
description: The Purchase Entity Stage inbound \[sn\_fcms\_intg\_imp\_purchase\_entity\] staging table temporarily stores important data about purchase entities before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-purch-entity-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Entity Stage inbound staging table

The Purchase Entity Stage inbound \[sn\_fcms\_intg\_imp\_purchase\_entity\] staging table temporarily stores important data about purchase entities before this data is sent to the primary table.

The following table lists the fields for the Purchase Entity Stage inbound \[sn\_fcms\_intg\_imp\_purchase\_entity\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|ERP number|String|Unique identifier for the ERP system from which data is imported.|
|Legal entity|String|Detailed information about individual suppliers, including banking details, payment methods, and credit terms.|
|Name|String|Name of the purchase entity.|

