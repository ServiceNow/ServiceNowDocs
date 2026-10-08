---
title: Register a deal on Partner portal
description: Register a deal on the Partner portal to update its state and trigger the end-to-end life cycle of the deal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/register-a-deal-partner-portal.html
release: brazil
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Partner Relationship Management, Use, Sales Customer Relationship Management]
---

# Register a deal on Partner portal

Register a deal on the Partner portal to update its state and trigger the end-to-end life cycle of the deal.

## Before you begin

Role required: sn\_prm\_dr.deal\_reg\_ui

## Procedure

1.  Navigate to the Partner portal.

2.  From the portal header, select **Create &gt; Create Deal Registration**.

3.  On the **Create New Deal Registration** screen, enter the required information on the **Deal registration information** form.\[Omitted image "create-deal-reg-partnerprtl.png"\] Alt text: Deal registration playbook on partner portal

<table id="id_j1r_k1j_tkc"><thead><tr><th>

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
</table>4.  On the **Deal registration type** screen, select the preferred deal registration type.

    The deal registration types are listed based on the channel partner and partner programs selected in the Partner Program deal type relationship \(sn\_prm\_dr\_pp\_deal\_type\) table.

5.  On the **Customer information** screen, select an existing account or create an account or consumer.

    To create an account, select **Can't find account details?** and fill in the fields. To learn more about the fields, see [Deal registration table fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/deal-registration-table-fields.md).

6.  On the **Product offerings** screen, select the list of product offerings that the customer is interested in.

    This is an optional step and can be skipped.

7.  On the **Additional information** screen, provide a description of the deal registration.

    You can also add attachments to support additional information.

8.  Select **Review** to review all the details and select **Submit**.

    As an agent you can update the status of the field on the **CRM Workspace**. To learn more, see [Update deal registration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/update-deal-registration-record.md).


## Result

A deal registration is created with an associated account, a channel partner, and a partner program. The state of the deal registration is **Submitted**. Multiple deal lines with an associated product offering are also created. You can also view the list of all deal registrations, along with the deals in **Draft** and **Approved** states on the Partner portal home page.

**Note:** Select **Actions** from the details page to edit or delete the deal registration. You can only delete deal registrations that are in the **Draft** state.

**Parent Topic:**[Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-partner-relationship-management.md)

**Related topics**  


[Configure Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configure-partner-relationship-management.md)

[Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/partner-relationship-management.md)

