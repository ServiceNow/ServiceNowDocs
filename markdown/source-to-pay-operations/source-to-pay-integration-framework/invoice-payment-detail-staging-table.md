---
title: Invoice payment detail import inbound table
description: The Invoice Payment detail import inbound \[sn\_spend\_intg\_imp\_invoice\_payment\_detail\] staging table temporarily stores important data about supplier before this data is sent to the \[sn\_shop\_invoice\_payment\_detail\] primary table.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice payment detail import inbound table

The Invoice Payment detail import inbound \[sn\_spend\_intg\_imp\_invoice\_payment\_detail\] staging table temporarily stores important data about supplier before this data is sent to the \[sn\_shop\_invoice\_payment\_detail\] primary table.

## Invoice payment detail import inbound staging table

The following table lists the fields for the Invoice payment detail import inbound \[sn\_spend\_intg\_imp\_invoice\_payment\_detail\] staging table.

<table id="table_nwp_byw_rbc"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Currency

</td><td>

String

</td><td>

Currency used in the invoice.This is a mandatory field.

</td></tr><tr><td>

ERP invoice number

</td><td>

String

</td><td>

Unique identifier for invoices in the ERP system.This is a mandatory field.

</td></tr><tr><td>

ERP Source

</td><td>

String

</td><td>

Specifies the original source of ERP.This is a mandatory field.

</td></tr><tr><td>

ERP supplier code

</td><td>

String

</td><td>

ERP supplier code from the external supplier.This is a mandatory field.

</td></tr><tr><td>

Payment amount

</td><td>

Decimal number

</td><td>

Total amount to be paid.This is a mandatory field.

</td></tr><tr><td>

Payment date

</td><td>

String \(yyy-mm-dd\)

</td><td>

Date by which payment is to be completed.This is a mandatory field.

</td></tr><tr><td>

Payment method

</td><td>

Choice Example: bank\_transfer/ cash\_payment/ cheque /credit\_card /debit\_card /wire\_transfer

</td><td>

Mode through which the payment is done.This is a mandatory field.

</td></tr><tr><td>

Payment reference ID

</td><td>

Alphanumeric

</td><td>

A unique ID to track the payment details.This is a mandatory field.

</td></tr><tr><td>

Remit to city

</td><td>

String

</td><td>

City to which the payment is made.This is a mandatory field.

</td></tr><tr><td>

Remit to country

</td><td>

String

</td><td>

Country to which the payment is made in ISO 3166 format. Example:USThis is a mandatory field.

</td></tr><tr><td>

Remit to state/province

</td><td>

String

</td><td>

State or province to which the payment is made.This is a mandatory field.

</td></tr><tr><td>

Remit to street

</td><td>

String

</td><td>

Street address to which the payment is made.This is a mandatory field.

</td></tr><tr><td>

Remit to ZIP/postal code

</td><td>

String

</td><td>

Zip or postal code address to which the payment is made.This is a mandatory field.

</td></tr><tr><td>

Scheduled payment date

</td><td>

String \(yyyy-mm-dd\)

</td><td>

Date at which the payment will be made.This is a mandatory field.

</td></tr><tr><td>

Third party import ID

</td><td>

String

</td><td>

Unique identifier for imported data set.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](../concept/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table](../../source-to-pay-integrations/reference/inbound-invoice-import-staging-table.md)

[Import error staging table](import-error-staging-table.md)

[Invoice line import inbound staging table](../../source-to-pay-integrations/reference/inbound-invoice-line-staging-table.md)

[Organization tax details inbound staging table](../../source-to-pay-integrations/reference/slo-org-tax-details-inbound-table.md)

[Invoice tax line staging table](../../source-to-pay-operations/reference/inbound-invoice-tax-line-staging-table-apo.md)

[Invoice staging table](invoice-staging-table.md)

[Invoice line stage table](invoice-line-staging-table.md)

