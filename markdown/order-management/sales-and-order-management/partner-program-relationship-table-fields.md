---
title: Partner program relationship table fields
description: Establish a relationship between channel partners and partner programs with the Partner Program Relationship \[sn\_prm\_partner\_program\_relationship\] table.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Partner Relationship Management reference, Reference, Sales Customer Relationship Management]
---

# Partner program relationship table fields

Establish a relationship between channel partners and partner programs with the Partner Program Relationship \[sn\_prm\_partner\_program\_relationship\] table.

<table id="table_dn4_xgx_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the relationship.

</td></tr><tr><td>

Channel partner

</td><td>

Channel partner associated with this relationship. **Note:** This field is populated from the Channel partner \[sn\_prm\_channel\_partner\] table.

</td></tr><tr><td>

Program

</td><td>

Program associated with this relationship.**Note:** This field is populated from the Partner program Program \[sn\_prm\_partner\_program\] table.

</td></tr><tr><td>

Active

</td><td>

State of the program, whether active or not.

</td></tr><tr><td>

Status

</td><td>

Status of the partner program relationship.

</td></tr><tr><td>

Onboarded date

</td><td>

Onboarding date of a partner into the program.

</td></tr><tr><td>

Off-boarded date

</td><td>

Offboarding date of a partner from the program.

</td></tr><tr><td>

Activity

</td><td>

Updates and information related to the partner program relationship.

</td></tr><tr><td>

Segment

</td><td>

Reference to the segment that a partner is associated or part of.**Note:** The relationship between a channel partner and the enterprise is always determined through a single segment record.

</td></tr></tbody>
</table>**Parent Topic:**[Partner Relationship Management reference](partner-relationship-management-reference.md)

**Related topics**  


[Configure Partner Program Relationship table](../task/configure-partner-program-relationship-table.md)

