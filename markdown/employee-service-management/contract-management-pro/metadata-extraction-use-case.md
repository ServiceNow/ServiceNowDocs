---
title: Contract metadata extraction use cases
description: In contract metadata extraction, use cases specify the information that you want Now Assist to detect in a document.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Use cases for contract metadata extraction, Now Assist use cases, Contract metadata extraction, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro]
breadcrumb: [Create use cases, Configure metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract metadata extraction use cases

In contract metadata extraction, use cases specify the information that you want Now Assist to detect in a document.

The CM Pro-Contract Metadata Extraction use case is available with the Now Assist in the Contract Management base system. This use case is not editable.

**Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to verify accuracy.

The following fields are configured in the CM Pro-Contract Metadata Extraction use case for metadata extraction.

<table id="table_otw_54f_xcc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default Target Field

</th></tr></thead><tbody><tr><td>

Other party name

</td><td>

The name of the company selling services or goods.

</td><td>

None

</td></tr><tr><td>

Internal party name

</td><td>

The name of the company buying services or goods.

</td><td>

vendor

</td></tr><tr><td>

Effective date

</td><td>

The date from which the contract becomes effective.

</td><td>

starts

</td></tr><tr><td>

End date

</td><td>

The date when the contract is set to expire.

</td><td>

ends

</td></tr><tr><td>

Contract number

</td><td>

A unique identifier for the contract.

</td><td>

vendor\_contract

</td></tr><tr><td>

Payment terms

</td><td>

The conditions under which payments are to be made.

</td><td>

invoice\_payment\_terms

</td></tr><tr><td>

Governing law

</td><td>

The jurisdiction under which the contract will be governed.

</td><td>

governing\_law

</td></tr><tr><td>

Contract duration

</td><td>

The duration for which a contract is valid.

</td><td>

contract\_duration

</td></tr><tr><td>

Currency

</td><td>

The currency in which the contract is denominated.

</td><td>

None

</td></tr><tr><td>

Contract value

</td><td>

The total value of the contract.

</td><td>

payment\_amount

</td></tr><tr><td>

Termination notice period

</td><td>

The notice period required to inform the other party prior to contract termination.

</td><td>

termination\_notice\_days

</td></tr><tr><td>

Termination fees

</td><td>

The fees payable if the contract is explicitly terminated for convenience and the contract mentions that such termination includes a payment.

</td><td>

termination\_fees

</td></tr><tr><td>

Payment frequency

</td><td>

The time interval for making a payment or generating invoice.

</td><td>

payment\_schedule

</td></tr><tr><td>

Late payment fees

</td><td>

The fees payable for late payment.

</td><td>

late\_payment\_fees

</td></tr><tr><td>

Most favored nation available

</td><td>

Availability of clause that covers the most favored nations in the contract document.

</td><td>

most\_favorite\_nation\_applicable

</td></tr><tr><td>

Renewal limit

</td><td>

The maximum percentage increase allowed on a contract’s fee during an annual automatic renewal.

</td><td>

renewal\_cap

</td></tr><tr><td>

Liability limit

</td><td>

The maximum amount that a party is obligated to pay in the event of a claim, loss, or breach under a contract.

</td><td>

liability\_cap

</td></tr><tr><td>

Includes affiliates

</td><td>

Availability of clause that specifies whether the terms and conditions also extend to the affiliated companies \(in other words, Entities controlled by, controlling, or under common control with a party\) of the primary contracting party.

</td><td>

affiliates\_included

</td></tr><tr><td>

Termination for convenience applicable

</td><td>

Availability of clause that indicates whether a party has the right to end a contract at any time, without reason.

</td><td>

termination\_for\_convience\_rights

</td></tr><tr><td>

Publicity restriction applicable

</td><td>

Availability of clause that restricts either party from publicly disclosing the existence, terms, or details of the agreement without prior written consent.

</td><td>

is\_publicity\_restricted

</td></tr><tr><td>

Termination for cause

</td><td>

The clause that specifies the reason for termination of contract by a party if the other party fails to meet key obligations.

</td><td>

termination\_for\_cause

</td></tr><tr><td>

Force Majeure applicable

</td><td>

Availability of clause that protects parties from liability if they are unable to meet obligations due to extraordinary events beyond their control.

</td><td>

is\_force\_majeure\_applicable

</td></tr><tr><td>

Renewal notice period

</td><td>

The notice period to renew a contract.

</td><td>

renewal\_notice\_period

</td></tr><tr><td>

Renewal termination notice period

</td><td>

The notice period to terminate the renewal of a contract.

</td><td>

termination\_notice\_period

</td></tr><tr><td>

Auto renewal clause available

</td><td>

Availability of clause that indicates if the contract renews by default unless someone takes an action to terminate it.

</td><td>

has\_auto\_renewal\_clause

</td></tr></tbody>
</table>**Parent Topic:**[Create use cases for contract metadata extraction](../task/cmpro-na-usecase-me.md)

