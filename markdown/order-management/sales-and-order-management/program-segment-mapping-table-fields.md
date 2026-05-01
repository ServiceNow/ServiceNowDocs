---
title: Program segment mapping table fields
description: Establish a mapping between a program and a segment on the program segment mapping \(sn\_prm\_program\_segment\_mapping\) table to determine whether a segment belongs to the appropriate partner program.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Partner Relationship Management reference, Reference, Sales Customer Relationship Management]
---

# Program segment mapping table fields

Establish a mapping between a program and a segment on the program segment mapping \(sn\_prm\_program\_segment\_mapping\) table to determine whether a segment belongs to the appropriate partner program.

<table id="table_uck_cmb_fhc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

String

</td><td>

Number of the programThe **Number** field is auto-generated and is read-only.

</td></tr><tr><td>

Program

</td><td>

Reference

</td><td>

Reference to the program configured in the partner program \(sn\_prn\_partner\_program\) table

</td></tr><tr><td>

Segment

</td><td>

Reference

</td><td>

Reference to the segment configured in the segment \(sn\_seg\_segment\) table

</td></tr><tr><td>

Active

</td><td>

True/False

</td><td>

Current state of the program segment mapping, whether active or not

</td></tr><tr><td>

Is Default

</td><td>

True/False

</td><td>

Determines if a segment is marked as default for a program.**Note:** At any given time, there can be only one **is\_default** entry for a program and segment relationship record.

</td></tr></tbody>
</table>**Parent Topic:**[Partner Relationship Management reference](partner-relationship-management-reference.md)

**Related topics**  


[Program segment criteria table fields](program-segment-criteria-table-fields.md)

[Program criteria table fields](program-criteria-table-fields.md)

