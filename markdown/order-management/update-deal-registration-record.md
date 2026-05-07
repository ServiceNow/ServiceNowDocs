---
title: Update deal registration record
description: Create a deal registration record or perform actions on an existing record on the CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Partner Workspace, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Update deal registration record

Create a deal registration record or perform actions on an existing record on the CSM Configurable Workspace.

## Before you begin

Role required: sn\_prm\_dr.deal\_reg\_ui

## About this task

After a deal is created on the Partner portal and is in the **Submitted** state, an agent on the **CSM/FSM Configurable Workspace** can see the same deal. The information in the fields is automatically populated from the Partner portal.

## Procedure

1.  Navigate to the **CSM/FSM Configurable Workspace** and select the list ![](../../tmt-assurance-workflows/image/lists_icon-proactive.png) view.

2.  Select **Deal Registration** &gt; **Submitted** to see a list of submitted deals.

    To learn how to create a deal and submit it, see [Register a deal on Partner portal](register-a-deal-partner-portal.md). The details in the deal registration form are auto-filled based on the selections made in the Partner portal by the B2B deal registration initiator \(sn\_prm\_dr.partner \_b2b\_deal\_reg\_initiator\), B2C deal registration initiator \(sn\_prm\_dr.partner \_b2c\_deal\_reg\_initiator\), deal registration initiator \(sn\_prm\_dr-partner\_deal\_reg\_initiator\), and deal registration manager \(sn\_prm\_dr.partner\_deal\_reg\_manager\).

3.  Perform one of the following actions based to update the status of the deal.

    -   Select **Assign to me** to assign the deal to yourself. This option is available only to agent personas.

        This changes the state of the deal to **Under Review**. In this state, you can perform one of the following actions on the deal.

        -   **Reject** the deal and fill in the **Closure notes**.
        -   **Mark as Duplicate** and fill in the **Closure notes**.
        -   **Cancel Deal Registration** to cancel the deal.
    -   Select **Submit for approval** to submit the deal.

        The deal registration is moved to the **Approvals** related list. The state of the deal registration changes to **Pending Approval** and an approval request is sent to the deal registration relationship contributor \(dn\_prm\_dr.enterprise\_deal\_reg\_rel\_contributor\) and the deal registration relationship manager \(sn\_prm\_dr.enterprise\_deal\_reg\_rel\_manager\) for the channel partner associated with the deal registration. After the deal registration is approved, the state changes to **Approved**.

        ![Different states of a submitted deal registration record before it is converted to an opportunity.](../image/workspace-deal-reg.png)

4.  After a deal is approved, you can perform one of the following actions on the approved deal.

    -   Select **Cancel Deal Registration**

        Enter the closure notes on the deal registration. This changes the closure code to **Rejected**.

    -   Select **Close** if there’s inactivity.
    -   Select **Convert to Opportunity** to associate the deal to an opportunity.

        The state of the deal changes to **Closed** and the closure code is updated to **Converted**.

    The deal registration is successfully converted to an opportunity.

    All line items from the deal registration form are transferred to opportunity line items with the help of Primitives. To learn more about Primitives, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).


**Parent Topic:**[Partner Workspace](../concept/partner-workspace.md)

**Related topics**  


[Register a deal on Partner portal](register-a-deal-partner-portal.md)

