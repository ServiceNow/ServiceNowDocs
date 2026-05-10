---
title: Deal registration table fields
description: Store the main details related to a deal submitted by a partner and track the life cycle of the deal through its stages on the deal registration \(sn\_prm\_dr\_deal\_registration\) table.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Partner Relationship Management reference, Reference, Sales Customer Relationship Management]
---

# Deal registration table fields

Store the main details related to a deal submitted by a partner and track the life cycle of the deal through its stages on the deal registration \(sn\_prm\_dr\_deal\_registration\) table.

<table id="table_j4s_gct_ghc"><thead><tr><th>

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

Number assigned to the deal registration

</td></tr><tr><td>

Channel partner

</td><td>

Reference

</td><td>

Reference to the channel partner \(sn\_prm\_channel\_partner\) table

</td></tr><tr><td>

Submitted by

</td><td>

Reference

</td><td>

Reference to the user and the initiator of the channel partner

</td></tr><tr><td>

Partner program

</td><td>

Reference

</td><td>

Reference to partner program \(sn\_prm\_partner\_program\) table

</td></tr><tr><td>

Deal registration type

</td><td>

Reference

</td><td>

Reference to deal registration type \(sn\_prm\_dr\_deal\_registration\_type\) table

</td></tr><tr><td>

Account

</td><td>

Reference

</td><td>

Reference to account \(customer\_account\)

</td></tr><tr><td>

Contact

</td><td>

Reference

</td><td>

Reference to contact \(customer\_contact\)

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Summary of the details of the deal

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Detailed information about the deal

</td></tr><tr><td>

State

</td><td>

Choice

</td><td>

Current state of the deal registration-   Draft
-   Pending approval
-   Approved
-   Submitted
-   Closed
-   Under-review
-   Canceled

</td></tr><tr><td>

Sales cycle type

</td><td>

Reference

</td><td>

Choice of sales cycle type field in the Opportunity \(sn\_opty\_mgmt\_core\_opportunity\) table

</td></tr><tr><td>

Estimated deal size

</td><td>

Currency

</td><td>

Estimated size of the deal

</td></tr><tr><td>

Estimated close date

</td><td>

Date/Time

</td><td>

Estimated end date of the deal

</td></tr><tr><td>

Assignment group

</td><td>

Reference

</td><td>

Reference to the user group

</td></tr><tr><td>

Assigned to

</td><td>

Reference

</td><td>

Reference to the user \(sys\_user\) that the deal is assigned to.If the deal registration is a B2B deal, only B2B agents are visible in this list. If the deal registration is a B2C deal, only B2C agents are visible in this list.

</td></tr><tr><td>

Consumer

</td><td>

Reference

</td><td>

Reference to consumer \(csm\_consumer\)

</td></tr><tr><td>

Account name

</td><td>

String

</td><td>

Name of the account

</td></tr><tr><td>

First name

</td><td>

String

</td><td>

First name of the contact or consumer

</td></tr><tr><td>

Last name

</td><td>

String

</td><td>

Last name of the contact or consumer

</td></tr><tr><td>

Email

</td><td>

String

</td><td>

Email of the contact or consumer

</td></tr><tr><td>

Opportunity

</td><td>

Reference

</td><td>

Reference to the Opportunity \(sn\_oppty\_mgmt\_core\_opportunity\)

</td></tr><tr><td>

Closure code

</td><td>

Choice

</td><td>

State of the closure code.-   Rejected
-   Duplicate
-   Converted
-   Incomplete

</td></tr><tr><td>

Active

</td><td>

Boolean

</td><td>

Determines whether the deal registration is active or not

</td></tr><tr><td>

Comments

</td><td>

Journal input

</td><td>

Comments and important information related to the deal, visible to channel partner and enterprise personas

</td></tr><tr><td>

Work notes

</td><td>

Journal input

</td><td>

Comments and important information related to the deal, only visible to enterprise personas

</td></tr><tr><td>

Domain

</td><td>

Domain id

</td><td>

Domain to which the deal registration belongs

</td></tr></tbody>
</table>**Parent Topic:**[Partner Relationship Management reference](partner-relationship-management-reference.md)

