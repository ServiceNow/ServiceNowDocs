---
title: Insurance Claims Core roles and properties
description: This section outlines the core roles involved in managing insurance claims and highlights their system properties.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Insurance Claims Core, Data Model, Learning and exploring, Financial Services Operations \(FSO\)]
---

# Insurance Claims Core roles and properties

This section outlines the core roles involved in managing insurance claims and highlights their system properties.

## Roles installed

The Insurance Claims Core includes access control lists \(ACLs\) and read-write user roles to restrict access to different tables.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Insurance Claims Core admin\[sn\_ins\_claim.admin\]

</td><td>

Create, read, write, and delete access to all tables including the core data.

</td></tr><tr><td>

Insurance Claims Core reserve writer\[sn\_ins\_claim.reserve\_writer\]

</td><td>

Write access to the Claim Reserve table.

</td></tr><tr><td>

Insurance Claims Core reserve reader\[sn\_ins\_claim.reserve\_reader\]

</td><td>

Read access to the Claim Reserve table.

</td></tr><tr><td>

Insurance Claims Core property writer\[sn\_ins\_claim.property\_writer\]

</td><td>

Write access to the Claim Incident table.

</td></tr><tr><td>

Insurance Claims Core property reader\[sn\_ins\_claim.property\_reader\]

</td><td>

Read access to the Claim Incident table.

</td></tr><tr><td>

Insurance Claims Core payment writer\[sn\_ins\_claim.payment\_writer\]

</td><td>

Write access to the Claim Payment table.

</td></tr><tr><td>

Insurance Claims Core payment reader\[sn\_ins\_claim.payment\_reader\]

</td><td>

Read access to the Claim Payment table.

</td></tr><tr><td>

Insurance Claims Core participant writer\[sn\_ins\_claim.participant\_writer\]

</td><td>

Write access to the Participant Role table.

</td></tr><tr><td>

Insurance Claims Core participant reader\[sn\_ins\_claim.participant\_reader\]

</td><td>

Read access to the Participant Role table.

</td></tr><tr><td>

Insurance Claims Core coverage writer\[sn\_ins\_claim.coverage\_writer\]

</td><td>

Write access to the Claim Coverage table.

</td></tr><tr><td>

Insurance Claims Core coverage reader\[sn\_ins\_claim.coverage\_reader\]

</td><td>

Read access to the Claim Coverage table.

</td></tr><tr><td>

Insurance Claims Core claim injury writer

\[sn\_ins\_claim.injury\_reader\]

</td><td>

Write access to the Claim Injury table.

</td></tr><tr><td>

Insurance Claims Core claim injury reader \[sn\_ins\_claim.injury\_writer\]

</td><td>

Read access to the Claim Injury table.

</td></tr><tr><td>

Insurance Claims Core profile reader\[sn\_ins\_claim.profile\_reader\]

</td><td>

Read access to the Claim Participant \(Profile\) table.

</td></tr><tr><td>

Insurance Claims Core profile writer\[sn\_ins\_claim.profile\_writer\]

</td><td>

Write access to the Claim Participant \(Profile\) table.

</td></tr><tr><td>

Policy Snapshot reader\[sn\_ins\_claim.policy\_snapshot\_reader\]

</td><td>

Read access to the Policy Snapshot table.

</td></tr><tr><td>

Policy Snapshot writer\[sn\_ins\_claim.policy\_snapshot\_writer\]

</td><td>

Write access to the Policy Snapshot table.

</td></tr></tbody>
</table>## Properties installed

To update the claims system properties, navigate to **Insurance claim operations** &gt; **Properties**. The following properties are available:

<table id="table_lkm_djh_ms"><thead><tr><th>

Property

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval process required for claim reserves?

</td><td>

sn\_ins\_claim.reserve\_approval

</td><td>

Determines if you want an approval process for claim reserve.

</td></tr><tr><td>

Hierarchical approval required for claim reserves?

</td><td>

sn\_ins\_claim.reserve\_approval\_is\_sequential

</td><td>

When enabled, the manager receives a notification that the adjuster has submitted a claim reserve request for review. Even if the manager doesn’t have the approval authority, the claim reserve approval request will always move a sequential order to all the next level manager for approval.

 When disabled, the approval request goes directly to a manager who has the approval authority for the amount.

</td></tr><tr><td>

Approval process required for claim payments?

</td><td>

sn\_ins\_claim.payment\_approval

</td><td>

Determines if you want an approval process for claim payment.

</td></tr><tr><td>

Hierarchical approval required for claim payments?

</td><td>

sn\_ins\_claim.payment\_approval\_is\_sequential

</td><td>

When enabled, the manager receives a notification that the adjuster has submitted a claim payment request for review. Even if the manager doesn’t have the approval authority, the claim payment approval request will always move in a sequential order to all the next level manager for approval.

 When disabled, the approval request goes directly to a manager who has the approval authority for the amount.

</td></tr></tbody>
</table>**Parent Topic:**[Insurance Claims Core](insurance-claims-core-data-model.md)

