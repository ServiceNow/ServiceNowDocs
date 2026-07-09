---
title: GL Account Stage inbound staging table
description: The GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table temporarily stores important data about General Ledger \(GL\) accounts before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-gl-account-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# GL Account Stage inbound staging table

The GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table temporarily stores important data about General Ledger \(GL\) accounts before this data is sent to the primary table.

The following table lists the fields for the GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Account currency|String|Currency name of the GL account.|
|Account name|String|Name of the GL account.|
|Alternate currency|String|Alternate currency name of the GL account.|
|Category|String|Category of the GL account.|
|Entity|String|Name of the entity.|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|GL Account|String|Name of the general ledger account.|
|Inactive|String|Status of the GL account. By default the checkbox is inactive.|
|Ledger type|String|Type of ledger account.|
|Local currency|String|Local currency that corresponds to the entity's operating location.|
|Number|String|General ledger account number.|
|Short description|String|Description of the GL account.|
|Sub-ledger account|String|Sub-ledger account number.|
|Type|String|Type of GL account.|

