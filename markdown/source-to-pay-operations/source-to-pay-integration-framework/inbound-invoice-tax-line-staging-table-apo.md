---
title: Invoice tax line staging table
description: The invoice tax line inbound \[sn\_spend\_intg\_imp\_invoice\_tax\_line\] staging table temporarily stores important data about the invoice tax line before this data is sent to the \[sn\_shop\_invoice\_tax\_line\] primary table.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice tax line staging table

The invoice tax line inbound \[sn\_spend\_intg\_imp\_invoice\_tax\_line\] staging table temporarily stores important data about the invoice tax line before this data is sent to the \[sn\_shop\_invoice\_tax\_line\] primary table.

## Invoice tax line inbound staging table

The following table lists the fields for the invoice tax line inbound \[sn\_shop\_invoice\_tax\_line\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Tax Type|String|Type of the tax applicable on the invoice.|
|Taxable Amount|FX Currency|The amount of tax applicable on an invoice.|
|Supplier Tax|String|The amount charged by the supplier.|
|Supplier Tax Rate|Decimal|The tax rate calculated by the third-party tax calculation engine.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](../../accounts-payable-operations/concept/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-import-staging-table.md)

[Import error staging table](../../accounts-payable-operations/reference/import-error-staging-table.md)

[Invoice line import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-line-staging-table.md)

[Invoice payment detail import inbound table](../../accounts-payable-operations/reference/invoice-payment-detail-staging-table.md)

[Organization tax details inbound staging table](../../supplier-lifecycle-operations/reference/slo-org-tax-details-inbound-table.md)

