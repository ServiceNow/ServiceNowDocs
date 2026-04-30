---
title: Import error staging table
description: The Import error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Import error staging table

The Import error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.

|Field|Data type|Description|
|-----|---------|-----------|
|Error message|String|A message that describes the error encountered.|
|Outbound status|Reference|Indicates the status of outgoing transactions.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](../concept/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-import-staging-table.md)

[Invoice line import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-line-staging-table.md)

[Invoice payment detail import inbound table](invoice-payment-detail-staging-table.md)

[Organization tax details inbound staging table](../../supplier-lifecycle-operations/reference/slo-org-tax-details-inbound-table.md)

[Invoice tax line staging table](../../source-to-pay-operations/reference/inbound-invoice-tax-line-staging-table-apo.md)

[Invoice staging table](invoice-staging-table.md)

[Invoice line stage table](invoice-line-staging-table.md)

