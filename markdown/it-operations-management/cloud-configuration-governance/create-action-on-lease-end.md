---
title: Create an action for an 'on Lease end' policy
description: A policy that is triggered by the on Lease end trigger can send a notification or perform a Start, Stop, or Deprovision life cycle operation.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an action for an 'on Lease end' policy

A policy that is triggered by the on Lease end trigger can send a notification or perform a Start, Stop, or Deprovision life cycle operation.

## Before you begin

-   Role required: sn\_cmp.cloud\_governor or admin
-   Optional: [Create one or more cloud policy groups](create-cloud-policy-group-1.md).
-   [Configure a cloud policy rule](configure-cloud-policy-rule-1.md) and associated conditions.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  Open the rule that should perform the action and then click **New** on the Policy Rule Actions related list.

4.  On the popup, click **Create** for the type of action to perform, enter a unique and meaningful **Action Name**, and then fill in the form for the action.

    ![Create Action popup](../image/action-on-lease-end-cloud-mgt.png)

    |Field|Description|
    |-----|-----------|
    |Blueprint Operation|Specify **Start**, **Stop**, or **Deprovision**.|

<table id="table_g3t_twp_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification

</td><td>

Select the text for the notification: -   Lease End Date Reached
-   Stack Decommissioned \(Lease End\)
-   Upcoming Lease End


</td></tr></tbody>
</table>
