---
title: Organization tax details inbound staging table
description: The Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table temporarily stores important data about an organization's tax information before this data is sent to the Organization Tax Details \[sn\_fin\_org\_tax\_detail\] primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Organization tax details inbound staging table

The Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table temporarily stores important data about an organization's tax information before this data is sent to the Organization Tax Details \[sn\_fin\_org\_tax\_detail\] primary table.

## Organization tax details inbound staging table

The following table lists the mandatory fields for the Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Organization|String|Name of the organization.|
|Tax ID|String|Tax ID of the organization.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](../../accounts-payable-operations/concept/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-import-staging-table.md)

[Import error staging table](../../accounts-payable-operations/reference/import-error-staging-table.md)

[Invoice line import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-line-staging-table.md)

[Invoice payment detail import inbound table](../../accounts-payable-operations/reference/invoice-payment-detail-staging-table.md)

[Invoice tax line staging table](../../source-to-pay-operations/reference/inbound-invoice-tax-line-staging-table-apo.md)

