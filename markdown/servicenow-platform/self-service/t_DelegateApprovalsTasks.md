---
title: Delegate approvals and tasks to another user
description: If you're out of the office, you can delegate responsibilities to another active user for a period of time.
locale: en-US
release: australia
product: Self-service
classification: self-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Delegation, Self-Service, Self-service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delegate approvals and tasks to another user

If you're out of the office, you can delegate responsibilities to another active user for a period of time.

## Before you begin

Role required: none to delegate approvals to another user

Ensure that the Delegates related list displays on the form. If the Delegates related list is not visible, do one of the following:

-   Select a different view, such as the ITIL or Default view, by selecting the **Additional actions menu** &gt; **View** &gt; **\(name of view\)**.

    ![The Additional actions menu highlighted](../image/Additional_actions_menu.jpg)

-   Configure the form to add the Delegates related list. For more information, see Configuring the form layout.

## Procedure

1.  Navigate to **All** &gt; **Self Service** &gt; **My Profile**.

2.  In the **Delegates** related list, click **New**.

3.  Select an active user as your delegate.

    **Note:** For a delegate to approve on your behalf from a Service Portal, they must have the approval\_admin or approver\_user role.

4.  Select date values from the **Starts** and **Ends** fields to set the period of time during which a delegate can work on your behalf.

5.  Specify the responsibilities the delegate will assume by selecting the following check boxes.

    You can delegate:

    -   **Approvals**: The delegate can approve items on your behalf.
    -   **Assignments**: The delegate can view and work on tasks assigned to you.
    -   **All notifications**: The delegate receives a copy of email notifications sent to you, except those marked as Meeting Invitation.

        **Note:**

        -   If the **Approvals** check box is selected but **All notifications** is not, the delegate does not receive approvals.
        -   If your delegate gets email notifications, they will be the same email notifications sent to you. The delegate may be confused to see "Incident assigned to you" emails, so make sure they know they are a delegate.
    -   **Meeting invitations**: The delegate receives a copy of email notifications sent of the type Meeting Invitation.

**Parent Topic:**[Service Delegation](../concept/c_ServiceDelegation.md)

