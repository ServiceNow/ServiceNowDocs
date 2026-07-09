---
title: Office Location Stage inbound staging table
description: The Office Location Stage inbound \[sn\_fcms\_intg\_office\_location\_stage\] staging table temporarily stores important data about office locations before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-office-loc-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Office Location Stage inbound staging table

The Office Location Stage inbound \[sn\_fcms\_intg\_office\_location\_stage\] staging table temporarily stores important data about office locations before this data is sent to the primary table.

The following table lists the fields for the Office Location Stage inbound \[sn\_fcms\_intg\_office\_location\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Country|String|Name of the country where the office location belongs.|

