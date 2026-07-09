---
title: CMDB Service Model Stage inbound staging table
description: The CMDB Service Model Stage inbound \[sn\_fcms\_intg\_cmdb\_service\_model\_stage\] staging table temporarily stores important data about service models before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-serv-mod-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# CMDB Service Model Stage inbound staging table

The CMDB Service Model Stage inbound \[sn\_fcms\_intg\_cmdb\_service\_model\_stage\] staging table temporarily stores important data about service models before this data is sent to the primary table.

The following table lists the fields for the CMDB Service Model Stage inbound \[sn\_fcms\_intg\_cmdb\_service\_model\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Model number|String|Unique identifier for the service model.|

