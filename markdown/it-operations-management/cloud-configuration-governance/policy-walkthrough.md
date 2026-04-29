---
title: Cloud policy example
description: A base system cloud policy, Lease End ServiceNow, uses the on Lease end trigger that fires when a virtual resource is near the lease end date. If the conditions in the policy rule are met, the policy engine sends a notification to the owner of the resource and performs operations on the resource.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud policy example

A base system cloud policy, Lease End ServiceNow, uses the on Lease end trigger that fires when a virtual resource is near the lease end date. If the conditions in the policy rule are met, the policy engine sends a notification to the owner of the resource and performs operations on the resource.

## Before you begin

Role required: sn\_cmp.cloud\_governor or admin

## About this task

In this example, you work with the Lease End ServiceNow policy. The policy performs the following actions when the conditions in the policy rule are met:

-   Send a notification to the owner of a cloud resource when the resource lease is about to expire.
-   Run a Stop operation on the resource.
-   Run a Deprovision operation on the resource.

You can change any base-system policy by modifying settings or making the policy active or inactive.

**Note:** Scheduled Start/Stop operations are not supported on the Terraform template and the Google Deployment Manager \(GDM\) stacks.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Search for and open the **Lease End ServiceNow** policy.

3.  Notice that the trigger is **on Lease end**, which means that the policy is triggered when the lease for the resource is near expiration.

    ![on Lease End trigger](../image/policy-lease-end-date.png)

4.  Sort the Rules related list by **Order of Execution**.

    The rule with the lowest number runs first.

    ![Rules for the policy](../image/policy-lease-end-date-rules.png)

    Notice that a notification rule runs first, followed by the Stop and Deprovision operations on the resource.

5.  Click the **Notify about upcoming lease end** rule.

6.  Notice that the rule specifies a condition: If it is one day before the end date, return `true`.

    ![Condition in the policy rule](../image/policy-lease-end-date-condition.png)

7.  In the Policy Rule Actions related list, click the \(empty\) **Name** of the action.

8.  On the Update Action pop-up window, enter an **Action Name** \(the value is required\), notice the value of the **Notification** \(you will use it in the next step\), and then close the pop-up window.

    ![Sending a notification](../image/policy-lease-end-action.png)

9.  Review the notification message other settings:

    1.  On the instance \(not the Cloud Admin Portal\), navigate to **System Notification** &gt; **Email** &gt; **Notifications**.

    2.  Search for and open the notification that is specified in the action by entering the filter text `*Upcoming lease end` for **Name**:

        ![Searching for the notification](../image/policy-lease-end-notification-search.png)

    3.  Click **Upcoming lease end** to open the notification form.

        Notice that the **Scheduled Operations \[sn\_cmp\_scheduled\_operation\]** table is specified.

        **Note:** You base all notifications for Cloud Provisioning and Governance on this table.

        ![Scheduled Operations table](../image/policy-lease-end-notification-table.png)

    4.  On the **When to send** tab, notice the conditions that apply:

        ![When to send the notification](../image/policy-lease-end-notification-send.png)

        |Condition|Description|
        |---------|-----------|
        |Operation Type is Notification|Specifies that the **Operation Type** field on the Scheduled Operations table must be **Notification**.|
        |Status|Specifies that the system should trigger the notification when the status of the scheduled operation record is in progress, rather than waiting until it is complete.|
        |Notification|Specifies that the **Upcoming lease end** notification must be specified.|

        **Note:** When you create a custom notification, use the default conditions, but change the **Notification** condition to the name of your notification.

    5.  Click the **Who will receive** tab.

        Notice that the **Users/Groups in fields** value is set to `Target.Assigned to`, `Target.Owned by`. You should use these settings to send the notification to the owner of the virtual resource.

10. In the Cloud Admin Portal, open the Lease End ServiceNow policy again, and then open the **Stop on lease end** rule.

    ![Stop on lease end rule](../image/policy-lease-end-stop-rule.png)

    The rule has two actions — one action to send a notification and the other action to run the Stop operation on the virtual resource.

11. Click the \(empty\) **Action Name** of the action for the Stop operation.

    ![Open the Stop operation action](../image/policy-lease-end-action-stop.png)

12. On the Update Action pop-up window, notice the settings:

    ![Stop operation](../image/policy-lease-end-action-operation.png)

    |Field|Description|
    |-----|-----------|
    |Policy and Rule Name|The policy and the rule to which this action belongs are specified in these fields by default.|
    |Action Type|**Run An Operation** tells the policy engine to trigger a standard operation \(Start, Stop, Deprovision, and so on\) on the resource.|
    |Blueprint Operation|The system runs the STOP operation on the resource.|

    The other rule, **Deprovision after lease end**, performs the Deprovision operation on the resource so that it does not stay active after the lease end date.


## What to do next

This example uses the settings available through the form configuration. To see example scripts that you could use in addition, see [Create a policy action script](create-policy-script.md).

**Parent Topic:**[Policies for Cloud Provisioning](../concept/cloud-policy.md)

