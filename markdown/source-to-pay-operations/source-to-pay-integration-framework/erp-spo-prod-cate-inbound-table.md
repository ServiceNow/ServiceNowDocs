---
title: CMDB Model Category Stage inbound staging table
description: The CMDB Model Category Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_category\_stage\] staging table temporarily stores important data about product model categories before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-prod-cate-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# CMDB Model Category Stage inbound staging table

The CMDB Model Category Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_category\_stage\] staging table temporarily stores important data about product model categories before this data is sent to the primary table.

The following table lists the fields for the CMDB Model Category Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_category\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Name|String|Name of the CMDB model category.|

