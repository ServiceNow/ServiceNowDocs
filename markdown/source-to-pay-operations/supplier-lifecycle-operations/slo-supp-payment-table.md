---
title: Supplier Payment Information table
description: The Supplier Payment Information \[sn\_fin\_supplier\_payment\] table stores important information about the payment information of a supplier.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary data tables for Supplier Lifecycle Operations, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Payment Information table

The Supplier Payment Information \[sn\_fin\_supplier\_payment\] table stores important information about the payment information of a supplier.

## Supplier Payment Information \[sn\_fin\_supplier\_payment\] table

The Supplier Payment Information \[sn\_fin\_supplier\_payment\] table contains the following fields.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Supplier

</td><td>

Reference

</td><td>

The supplier that the payment information is for.

</td></tr><tr><td>

Active

</td><td>

Boolean

</td><td>

Indicates whether the supplier payment record is active.

</td></tr><tr><td>

Currency

</td><td>

Reference

</td><td>

The three-digit ISO currency code used for a given country.

</td></tr><tr><td>

Primary

</td><td>

Boolean

</td><td>

Option that indicates whether this account is the primary account.**Note:** A supplier can have only one primary payment record at a given time.

</td></tr><tr><td>

Bank name

</td><td>

String

</td><td>

Name of the bank.

</td></tr><tr><td>

ABA routing number

</td><td>

String

</td><td>

Unique, nine-digit number used to identify banks and financial institutions.

</td></tr><tr><td>

BSB code

</td><td>

String

</td><td>

Bank State Branch is a six-digit number that is used to identify a bank code and its associated branch in Australia.

</td></tr><tr><td>

IFSC code

</td><td>

String

</td><td>

Indian Financial System Code \(IFSC\) is a unique 11-digit alphanumeric code that is used for online fund transfer transactions in India.

</td></tr><tr><td>

Country

</td><td>

Reference

</td><td>

Country the bank is located in.

</td></tr><tr><td>

SWIFT Code

</td><td>

String

</td><td>

Bank Identifier Code \(also known as SWIFT code\) of the bank.

</td></tr><tr><td>

IBAN

</td><td>

String

</td><td>

International Bank Account Number used for international payments.

</td></tr><tr><td>

Bank identification number

</td><td>

String

</td><td>

Number that uniquely identifies the supplier payment record in an ERP system.

</td></tr><tr><td>

Beneficiary name on account

</td><td>

String

</td><td>

Name of the beneficiary.

</td></tr><tr><td>

Account number

</td><td>

Password2

</td><td>

Account number of the beneficiary.

</td></tr></tbody>
</table>For more information, see [Supplier Lifecycle Operations data model](slo-data-model.md).

**Parent Topic:**[Primary data tables for Supplier Lifecycle Operations](slo-primary-data-tables.md)

