---
title: Configure granular delegation rules for an approver
description: Set up delegation rules that enable an approver in Advanced Approval Management to assign a delegate who can accept or reject approval requests on behalf of the approver.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-approval-delegation.html
release: australia
topic_type: task
last_updated: "2026-06-27"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure granular delegation rules for an approver

Set up delegation rules that enable an approver in Advanced Approval Management to assign a delegate who can accept or reject approval requests on behalf of the approver.

## Before you begin

The Granular Delegation \(com.glide.granular\_service\_delegation\) application must be installed and configured on your instance.

Set the application scope in your instance to Advanced Approval Management.

Role required: admin or delegation\_admin

## About this task

As an admin, setting up granular delegation involves identifying the advanced approval records to which a delegation rule applies. You then specify the conditions that identify the type of approvals that can be delegated and the users who can approve or reject delegated approval tasks.

## Procedure

1.  Navigate to **All** &gt; **Granular Delegation** &gt; **Delegation Rule Tables**.

2.  Select **New** to specify the Advanced Approval Management table that defines the approval steps for which the delegate will be an approver.

    Fill in the form.

    1.  In the **Table** field, select the Approval Step \[sn\_adv\_appr\_mgmt\_approval\_step\] table.

    2.  Turn on the **Active** field.

    3.  Select **Submit**.

3.  Navigate to **All** &gt; **Granular Delegation** &gt; **Delegation Rules**.

4.  Select **New** to define the delegation rule that identifies the approver for whom the delegate will replace.

    1.  In the **Name** field, enter the functional role, for example `Sales manager`.

    2.  Enter the conditions that determine the role for which delegation occurs in the Approval Step \[sn\_adv\_appr\_mgmt\_approval\_step\] table.

        For example, you can specify delegation for the Sales Manager by specifying the condition **\[Approval rule\] \[is\] \[Sales Manager\]**.

    3.  Turn on the **Approvals** field and the **Assignments** field.

    4.  Select **Submit**.

        The **Short description** field is automatically populated, identifying the delegation for the Approval Step table and the conditions you entered.

5.  Create the new delegate to define the employee who will be the delegate for the approver.

    For details on defining the delegate see, [Create a delegate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/create-delegation-admin.md). You specify the employee who will serve as the delegate, the start and end dates for delegation, and other options, such as the option to send the delegate a copy of the notifications that the approver receives.


## Result

After setting up the delegation capability for an approver, the approver can delegate advanced approval requests to another employee by using Employee Center, if both the approver and delegate use Employee Center. For information on delegating tasks to another employee, see [Delegate on-demand tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/granular-delegation-use.md).

