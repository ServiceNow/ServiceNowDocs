---
title: Register a deal on Partner portal
description: Register a deal on the Partner portal to update its state and trigger the end-to-end life cycle of the deal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Partner Relationship Management, Use, Sales Customer Relationship Management]
---

# Register a deal on Partner portal

Register a deal on the Partner portal to update its state and trigger the end-to-end life cycle of the deal.

## Before you begin

Role required: sn\_prm\_dr.deal\_reg\_ui

## Procedure

1.  Navigate to the Partner portal.

2.  From the portal header, select **Requests**.

3.  From the drop-down, select **Submit a request** &gt; **Register a deal**.![Deal registration playbook on partner portal](../image/portal-playbook-deal-reg.png)

4.  On the **Create New Deal Registration** screen, enter the required information on the **Deal registration information** form.

    To learn more about the fields on this form, see [Deal registration table fields](../reference/deal-registration-table-fields.md).

5.  On the **Deal registration type** screen, select the preferred deal registration type.

    The deal registration types are listed based on the channel partner and partner programs selected in the Partner Program deal type relationship \(sn\_prm\_dr\_pp\_deal\_type\) table.

6.  On the **Customer information** screen, select an existing account or create an account or consumer.

    To create an account, select **Can't find account details?** and fill in the fields. To learn more about the fields, see [Deal registration table fields](../reference/deal-registration-table-fields.md).

7.  On the **Product offerings** screen, select the list of product offerings that the customer is interested in.

    This is an optional step and can be skipped.

8.  On the **Additional information** screen, provide a description of the deal registration.

    You can also add attachments to support additional information.

9.  Select **Review** to review all the details and select **Submit**.

    As an agent you can update the status of the field on the **CSM/FSM Configurable Workspace**. To learn more, see [Update deal registration record](update-deal-registration-record.md).


## Result

A deal registration is created with an associated account, a channel partner, and a partner program. The state of the deal registration is **Submitted**. Multiple deal lines with an associated product offering are also created. You can also view the list of all deal registrations, along with the deals in **Draft** and **Approved** states on the Partner portal home page.

**Note:** Select **Actions** from the details page to edit or delete the deal registration. You can only delete deal registrations that are in the **Draft** state.

**Parent Topic:**[Using Partner Relationship Management](../concept/using-partner-relationship-management.md)

**Related topics**  


[Update deal registration record](update-deal-registration-record.md)

