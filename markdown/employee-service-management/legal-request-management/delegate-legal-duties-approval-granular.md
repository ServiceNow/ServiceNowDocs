---
title: Delegate specific legal duties to another user using granular delegation
description: Delegate specific legal duties relating to your assigned legal requests, legal matters, legal matter tasks, and approvals to another user when you might not have time or are unavailable. These specific duties are derived from the pre-defined delegation rules.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Delegation of legal duties and approvals, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Delegate specific legal duties to another user using granular delegation

Delegate specific legal duties relating to your assigned legal requests, legal matters, legal matter tasks, and approvals to another user when you might not have time or are unavailable. These specific duties are derived from the pre-defined delegation rules.

## Before you begin

-   Granular Delegation plugin \(com.glide.granular\_service\_delegation\) must be activated.
-   In the Legal Counsel Workspace settings, the **My Delegate** workspace list must be configured as follows:
    -   The **My Delegate** workspace list on the Granular Delegate \[sys\_granular\_delegate\] table must be active.
    -   The **My Delegate** workspace list on the Delegate \[sys\_user\_delegate\] table must be inactive.
-   For the new experience Legal Counsel Center Workspace, open **&lt;instance&gt;/sys\_ux\_list\_list.do?sysparm\_query=titleLIKEMy%20Delegates**.

    The **My Delegate** UX list must be configured as follows:

    -   The **My Delegates** list on the Granular Delegate \[sys\_granular\_delegate\] table must be active.
    -   The **My Delegates** list on the Delegate \[sys\_user\_delegate\] table must be inactive.
-   Delegate rules must be created by the administrator. For more information, see [Create delegation rules](../../employee-service-management/granular-delegation/task/create-delegation-rules.md).

Role required: legal\_fulfiller

## About this task

You can use the granular delegation to delegate only specific requests such as Privacy Assessment requests. A delegation rule can be set on the Legal Request \[sn\_lg\_ops\_request\] table with the condition as **\[Category\] \[is\] \[Privacy\]**.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Set Delegate**, click **My Delegates**.

4.  In the My Delegates list, click **New**.

5.  On the form, fill in the fields.

<table id="table_yst_sf4_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delegate

</td><td>

User to whom you are delegating legal duties assigned to you.**Note:** The delegate must be from the assignment group of which you are a member.

</td></tr><tr><td>

Starts

</td><td>

Start date of the delegation period.

</td></tr><tr><td>

Ends

</td><td>

End date of the delegation period.

</td></tr></tbody>
</table>6.  Click **Save**.

    The delegation is created for the specified period. The **Delegation Rules** tab appears.

7.  In the **Delegation Rules** tab, assign only specific legal duties and approvals defined in the delegate rules to the delegate.

    1.  In the **Delegation Rules** tab, click **Add Duties**.

    2.  In the Add Duties dialog, select the delegation rules you want to assign to the delegate.

    3.  Click **Add**.


## Result

Setting the granular delegation has the following effects during the specified period:

-   The delegate can access and work on your assigned legal requests, legal matters, legal matter tasks, and approvals as per the assigned duties from the **Delegated to me** list.
-   Both you and the delegate receive notifications related to activities done on legal requests, legal matters, matter tasks, and approvals.

**Parent Topic:**[Delegation of legal duties and approvals](../concept/legal-services-delegation.md)

