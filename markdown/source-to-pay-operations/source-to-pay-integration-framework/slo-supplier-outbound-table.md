---
title: Supplier outbound staging table
description: The Supplier outbound \[sn\_spend\_intg\_outbound\_supplier​\] staging table stores important data about the supplier so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Supplier Lifecycle Operations, Outbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier outbound staging table

The Supplier outbound \[sn\_spend\_intg\_outbound\_supplier​\] staging table stores important data about the supplier so that an ERP integrator can export this data to a third-party ERP system.

## Supplier outbound staging table

The following table lists the fields for the Supplier outbound \[sn\_spend\_intg\_outbound\_supplier​\] staging table.

<table id="table_e4l_dr5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ABA routing number

</td><td>

string

</td><td>

Unique, nine-digit number used to identify banks and financial institutions.

</td></tr><tr><td>

Account number

</td><td>

string

</td><td>

Account number of the supplier.

</td></tr><tr><td>

Active

</td><td>

string

</td><td>

Indicates whether the supplier payment record is active.

</td></tr><tr><td>

Beneficiary name on account

</td><td>

string

</td><td>

Name of the beneficiary on the supplier's account.

</td></tr><tr><td>

BSB code

</td><td>

string

</td><td>

Bank State Branch is a six-digit number that is used to identify a bank code and its associated branch in Australia.

</td></tr><tr><td>

City

</td><td>

string

</td><td>

City where the supplier is located.

</td></tr><tr><td>

Country

</td><td>

string

</td><td>

Country where the supplier is located.

</td></tr><tr><td>

ERP company code

</td><td>

string

</td><td>

Company code of the supplier in the ERP system.

</td></tr><tr><td>

ERP Source

</td><td>

string

</td><td>

ERP source used by the organization.

</td></tr><tr><td>

Fax number

</td><td>

ph\_number

</td><td>

Fax number of the supplier that can be used for sending documents.

</td></tr><tr><td>

General ledger account

</td><td>

string

</td><td>

Accounts payable reconciliation account for the supplier.

</td></tr><tr><td>

IFSC code

</td><td>

string

</td><td>

IFSC code of supplier's account number.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Status of the integration process.The outbound integration is considered successful only when the integrating status is **New**.

This is a mandatory field.

</td></tr><tr><td>

Legal entity

</td><td>

string

</td><td>

Name of the legal entity of the supplier.

</td></tr><tr><td>

Legal Name

</td><td>

String

</td><td>

Legal name of the supplier.This is a mandatory field.

</td></tr><tr><td>

Off-boarded date

</td><td>

glide\_date

</td><td>

Date of the supplier's termination from the organization.

</td></tr><tr><td>

On-boarded

</td><td>

string

</td><td>

Indicates whether the supplier is on-boarded into the ERP system.

</td></tr><tr><td>

Payment term

</td><td>

string

</td><td>

Agreed time and conditions for payment to the supplier.

</td></tr><tr><td>

Phone number

</td><td>

String

</td><td>

Phone number of the supplier.This is a mandatory field.

</td></tr><tr><td>

Primary phone number

</td><td>

ph\_number

</td><td>

Phone number of the primary contact at the supplier organization.

</td></tr><tr><td>

Processing message

</td><td>

string

</td><td>

A message that describes the current processing status.

</td></tr><tr><td>

State / Province

</td><td>

string

</td><td>

State or province where the supplier is located.

</td></tr><tr><td>

Street address

</td><td>

string

</td><td>

Street where the supplier is located.

</td></tr><tr><td>

Zip / Postal code

</td><td>

string

</td><td>

Zip code or postal code where the supplier is located.

</td></tr></tbody>
</table>