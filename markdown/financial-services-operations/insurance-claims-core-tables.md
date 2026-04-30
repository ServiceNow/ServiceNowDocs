---
title: Insurance Claims Core tables
description: This section explains the insurance tables in Insurance Claims Core and how they handle insurance data.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Insurance Claims Core, Data Model, Learning and exploring, Financial Services Operations \(FSO\)]
---

# Insurance Claims Core tables

This section explains the insurance tables in Insurance Claims Core and how they handle insurance data.

## Tables installed

The following table lists the tables that are installed with Insurance Claims Core.

<table id="table_i4g_j1j_2vb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Claim Coverage\[sn\_ins\_claim\_coverage\]

</td><td>

Stores coverage of an insurance policy for a claim.

</td></tr><tr><td>

Claim Incident\[sn\_ins\_claim\_property\]

</td><td>

Stores details about the insured properties or details about the other properties that are involved in the loss incident that is reported in the claim.

</td></tr><tr><td>

Claim Participant\[sn\_ins\_claim\_profile\]

</td><td>

Stores details about all the participants involved in the claim process. It can be a person or company. For example, the insured driver, the driver of another vehicle, or any external experts involved in the evaluation and so on. These details can be used as an involved entity to make a claim against a coverage or as a payee to whom a payment is made.

</td></tr><tr><td>

Participant Role\[sn\_ins\_claim\_participant\]

</td><td>

Stores information about a claim participant's role, such as the injured party, the insured, the reporting party, or another role related to the claim. Extends the Customer Service table Related Party \[sn\_customerservice\_related\_party\].

</td></tr><tr><td>

Claim Reserve\[sn\_ins\_claim\_reserve\]

</td><td>

Stores the reserve amounts that are created against a coverage and entity combination.

</td></tr><tr><td>

Claim Payment\[sn\_ins\_claim\_payment\]

</td><td>

Stores details about the payment amount that is created against a reserve for settling a claim.**Note:** For both claim reserve and payment, depending on the system properties, the claims approval engine for approval process might be invoked for a reserve record or payment.

</td></tr><tr><td>

Injury Incident\[sn\_ins\_claim\_injury\]

</td><td>

Stores participant injury details for a claim.

</td></tr><tr><td>

Policy Snapshot\[sn\_ins\_claim\_policy\_snapshot\]

</td><td>

Stores policy information specific to the time of an incident date, including Policy Number, Effective Date, Expiry Date, and other details.

</td></tr><tr><td>

Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\]

</td><td>

Defines the configuration for claim incidents that can be created as part of the Insurance claims application. Use this table to define the following:-   Name and short description of the claim incident
-   Claim incident table name
-   The icon that is shown
-   Adjuster task service definition
-   Parent service definition
-   Whether the loss can be itemized
-   Whether an adjuster task is created per incident or per incident type \(for example, a single task for all baggage claim incidents\)
-   Display order of the service definitions in the playbook
-   Whether the service definition is shown in the UI or not

For more information, see [Claim Incident Configuration table](../../fso-insurance-claims-flow/concept/claim-incident-configuration-table.md).

</td></tr><tr><td>

Itemized Loss/Expense \[sn\_ins\_claim\_incident\_item\]

</td><td>

Stores information about the itemized losses and expenses for a claim.

</td></tr><tr><td>

Baggage Incident \[sn\_ins\_claim\_baggage\]

</td><td>

Stores information about a baggage loss incident, such as a description of the baggage, the associated flight details, and the claimant.

</td></tr><tr><td>

Trip Incident \[sn\_ins\_claim\_trip\]

</td><td>

Stores information about a trip loss incident, such as a description of the incident, reservation numbers, and other supporting questions.

</td></tr></tbody>
</table>**Parent Topic:**[Insurance Claims Core](insurance-claims-core-data-model.md)

