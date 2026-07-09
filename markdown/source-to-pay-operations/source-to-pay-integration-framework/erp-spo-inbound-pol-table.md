---
title: Purchase Order Line inbound staging table
description: The Purchase Order Line inbound \[sn\_fcms\_intg\_imp\_order\_line\] staging table temporarily stores important data about purchase order lines before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-inbound-pol-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Line inbound staging table

The Purchase Order Line inbound \[sn\_fcms\_intg\_imp\_order\_line\] staging table temporarily stores important data about purchase order lines before this data is sent to the primary table.

The following table lists the fields for the Purchase Order Line inbound \[sn\_fcms\_intg\_imp\_order\_line\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|ERP PO number|String|Purchase order number from the ERP system.|
|ERP PO line number|String|Purchase order line number from the ERP system.|

