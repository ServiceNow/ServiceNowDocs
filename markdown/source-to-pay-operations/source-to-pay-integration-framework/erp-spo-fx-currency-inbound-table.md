---
title: FX Currency Stage inbound staging table
description: The FX Currency Stage inbound \[sn\_fcms\_intg\_fx\_currency\_stage\] staging table temporarily stores important data about FX currencies before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-fx-currency-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# FX Currency Stage inbound staging table

The FX Currency Stage inbound \[sn\_fcms\_intg\_fx\_currency\_stage\] staging table temporarily stores important data about FX currencies before this data is sent to the primary table.

The following table lists the fields for the FX Currency Stage inbound \[sn\_fcms\_intg\_fx\_currency\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|ISO currency code|String|Unique three-letter currency code as defined by the International Organization for Standardization \(ISO\).|
|Name|String|Name of the currency.|

