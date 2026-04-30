---
title: Create a success blueprint template
description: Create a success blueprint template with predefined success objectives and outcomes.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customer success, Configure, Customer Success Management]
---

# Create a success blueprint template

Create a success blueprint template with predefined success objectives and outcomes.

## Before you begin

-   Role required: sn\_acct\_lc.success\_template\_owner, sn\_acct\_lc.success\_template\_approver
-   The **sn\_acct\_lc.enableApprovalForSuccessTemplate** system property must be set to **True**.

## Procedure

1.  Log in as a user with the template owner \(sn\_acct\_lc.success\_template\_owner\) role.

2.  Navigate to **All** &gt; **Customer Success** &gt; **Success Objective Templates**.

3.  Select **Create success blueprint**.

4.  In the Product drop down list, from the CMDB model list, select the product for which this success objective will be applicable.

5.  In the Objective Framework section, you can do the following:

    -   Select the `Mandatory` checkbox to set this as a mandatory objective for your engagement.
    -   Select the ![](../../../common/image/icon-lock.png) icon next to the Driver field to add the key drivers for this template. The drivers you select will be used to calculate the health and risk score for the associated product.
    **Note:** If a success objective is marked as mandatory, it is automatically be selected when you create an engagement for the associated product.

6.  Select **Save**.

    The next step is to create a success outcome template.

7.  Navigate to the **Success Outcome Templates** related list and select **New**.

8.  Enter a title and description for the outcome template.

9.  In the Outcome Measurement section, you can specify the following:

    -   Tracking method: Select `Metric` or `Manual` from the drop down list.
    -   Units: Select the measurement unit for this outcome.
    -   Mandatory: Select the `Mandatory` checkbox to set this as a mandatory outcome for your engagement.
10. Select **Save** the success outcome template.

    -   You can modify the template and change if it is in a `Draft` state. After you have made the changes, select **Update** to update and save the changes.
    -   You can follow this process to add multiple success outcome templates.
11. Select **Publish** to publish the success outcome template and select **Update**.

    -   You can’t modify a success outcome template that is in the `Published` State.
    -   Select **Cancel** to cancel a success outcome template that hasn’t been approved. You see a message indicating that all associated tasks will be canceled and any progress is lost. Select **Yes** if you no longer want to use this template.
12. After you have created and published all the success outcome templates, select **Request for approval**.

    ![Success Objective Template](../image/account-lifecycle-success-obj-temp.png)

    **Note:**

    -   The **Request for approval** option can be used to publish success objectives only if the **sn\_acct\_lc.enableApprovalForSuccessTemplate** property has been set to **True**.
    -   You must create at least one success outcome template for a success objective.
    -   You must publish all success outcome templates before you can request the success objective template to be approved.
    The State field is updated to `Waiting for approval`.


## What to do next

**Approve a success blueprint template**

To approve a success blueprint template request, follow these steps:

1.  Login as a user with the template approver \(sn\_acct\_lc.success\_template\_approver\) role.
2.  Navigate to **All** &gt; **Customer Success** &gt; **Success Objective Templates**.
3.  Open the template with the `Waiting for approval` State.

    ![Success Objective Template - Approve](../image/account-lifecycle-success-obj-temp-appr.png)

4.  Select **Approve** to approve the template. The State is updated to `Approved`.

    If you don't want to approve the template, you can select **Cancel** or **Reject** to cancel the process. The State is updated to `Draft` if canceled or rejected.

5.  After the template has been approved, select **Publish** to publish the template.

    **Note:**

    -   After a template has been published, it can longer be modified.
    -   Select **Retire** to retire a template. A retired template can no longer be used to define objectives and outcomes for an engagement.

-   **[Create a success blueprint](account-lifecycle-create-blueprint.md)**  
Use this option to create a success blueprint to add success objectives and outcomes for the engagement.

**Parent Topic:**[Customer success](../concept/account-lifecycle-config-cust-success.md)

