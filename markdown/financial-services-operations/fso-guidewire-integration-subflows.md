---
title: Financial Services Operations Integration with Guidewire subflows
description: The Financial Services Operations Integration with Guidewire provides these subflows to automate Guidewire tasks. These subflows can be customized as per business needs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Guidewire, Integrate, Financial Services Operations \(FSO\)]
---

# Financial Services Operations Integration with Guidewire subflows

The Financial Services Operations Integration with Guidewire provides these subflows to automate Guidewire tasks. These subflows can be customized as per business needs.

## Subflows

A sample list of subflows is given below:

<table id="table_xh5_54p_tyb"><thead><tr><th>

Category

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="9">

Policy Snapshot for Claim Case

</td><td>

Create Insured Vehicle for Policy Snapshot

</td><td>

Creates an insured vehicle for the policy snapshot.

</td></tr><tr><td>

Create Policy Coverage for Policy Snapshot

</td><td>

Creates policy and vehicle coverage for a policy.

</td></tr><tr><td>

Create Policy Participant for Policy Snapshot

</td><td>

Creates policy participants for insured contacts on a policy.

</td></tr><tr><td>

Create Policy Participants for Policy Snapshot

</td><td>

Iterate through the Input Claim Contacts IDs list, look up the contact details from Guidewire, and create policy participant records.

</td></tr><tr><td>

Create Policy Scoped Coverages for Policy Snapshot

</td><td>

Iterate through the coverages of the policy for this claim and create policy coverage records for each participant.

</td></tr><tr><td>

Create Policy Snapshot

</td><td>

Creates Policy Snapshot header record and routes to relevant granular subflows for creating the following:-   Insurance policy related coverage
-   Insurance properties
-   Policy participants
-   Associated tables

</td></tr><tr><td>

Create Vehicles and Vehicle Coverages for Policy Snapshot

</td><td>

Iterate through the vehicles covered by the policy for this claim and create customer property, insured property and policy coverages for each vehicle.

</td></tr><tr><td>

Match Consumer or Account for Participant

</td><td>

Search for an existing consumer or account by Guidewire Policy System ID.

</td></tr><tr><td>

Match Consumer or Account for Participant by ID

</td><td>

Search for an existing consumer or account by Guidewire Policy System ID.

</td></tr><tr><td>

Send Claim

</td><td>

Create Minimal Draft Claim

</td><td>

Creates a new draft claim in Guidewire using the Incident Date and Policy Number from the Claim Case.

</td></tr><tr><td rowspan="16">

Get Claim

</td><td>

Create Claim Coverages

</td><td>

Retrieves all the exposures from Guidewire and maps them to the Claim Coverages table.

</td></tr><tr><td>

Create Claim Documents

</td><td>

Download claim documents and attach them to the case record.

</td></tr><tr><td>

Create Claim Participant for Claim

</td><td>

Creates a Claim Participant for a specific claim contact.

</td></tr><tr><td>

Create Claim Participants for Claim

</td><td>

Creates new claim participant records for a given claim.

</td></tr><tr><td>

Create Commercial Auto Claim Case

</td><td>

Used to create a Commercial Auto Claim Case.

</td></tr><tr><td>

Create Injury Incidents for Claim

</td><td>

Creates injury incidents and claim participants.

</td></tr><tr><td>

Create Other Property Incidents for Commercial Auto

</td><td>

Retrieves all the fixed properties incident associated with the claim case. It creates the auto property record for the commercial auto case for each of the fixed property incidents.

</td></tr><tr><td>

Create Other Property Incidents for Personal Auto

</td><td>

Retrieves all the fixed property incidents associated with the claim case and creates the relevant auto property record.

</td></tr><tr><td>

Create Personal Auto Claim Case

</td><td>

Helps create a Personal Auto Claim Case.

</td></tr><tr><td>

Create Role for Claim Participant

</td><td>

Creates a Participant Role record by associating a Role to a Claim Participant on a Case.

</td></tr><tr><td>

Create Vehicle Property Incidents for Commercial Auto

</td><td>

Retrieves all the vehicle incidents from a given claim case and creates corresponding commercial auto property incidents.

</td></tr><tr><td>

Create Vehicle Property Incidents for Personal Auto

</td><td>

Retrieves all the vehicle incidents from a given claim case and creates corresponding personal auto property incidents.

</td></tr><tr><td>

Create Work Notes for Claim

</td><td>

Retrieves all notes from claim and adds them as work notes to the case.

</td></tr><tr><td>

Extract Name from Claim Contact

</td><td>

Extracts the First Name, Last Name for Person, or Company Name for Company.

</td></tr><tr><td>

Get Commercial Auto Claim

</td><td>

Based on the Claim ID, this subflow retrieves a specific commercial claim from Guidewire.

</td></tr><tr><td>

Get Personal Auto Claim

</td><td>

Based on the Claim ID, this subflow retrieves a specific personal claim from Guidewire.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations Integration with Guidewire](../concept/fso-integration-with-guidewire-landing-page.md)

