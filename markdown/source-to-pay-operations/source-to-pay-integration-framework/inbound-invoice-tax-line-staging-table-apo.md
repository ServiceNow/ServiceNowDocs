---
title: Invoice tax line staging table
description: The invoice tax line inbound \[sn\_spend\_intg\_imp\_invoice\_tax\_line\] staging table temporarily stores important data about the invoice tax line before this data is sent to the \[sn\_shop\_invoice\_tax\_line\] primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-tax-line-staging-table-apo.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
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

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table]()

[Import error staging table]()

[Invoice line import inbound staging table]()

[Invoice payment detail import inbound table]()

[Organization tax details inbound staging table]()

[Invoice staging table]()

[Invoice line stage table]()

