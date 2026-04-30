---
title: Configure Business hours operations
description: You can choose to use or to disable Business Hours features and specify the amount of non-business hour spend that triggers notifications to users or groups. Controlling unnecessary resource use can help reduce costs.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Improve resource usage with Business hours, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Configure Business hours operations

You can choose to use or to disable Business Hours features and specify the amount of non-business hour spend that triggers notifications to users or groups. Controlling unnecessary resource use can help reduce costs.

## Before you begin

A cloud account \(parent account\) that has at least one service account and associated datacenters is required.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\] for owned service accounts.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Business hours**.

2.  Select **Settings**.

3.  On the form, fill in the fields.

<table id="table_qnq_v3t_tgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable business hours

</td><td>

Option for enabling the Business hours feature. All active policies are applied when data becomes available.

 Deselect the check box to disable the Business hours feature. No policies are applied regardless of the **Active** setting for a policy.

**Note:** When you disable the Business hours feature, all schedules that were applied by policies are deactivated and resources return to their original schedules.

</td></tr><tr><td>

Precedence

</td><td>

The role that should have precedence when policies are applied. Select one of the following:

 -   Admin Policies
-   Owner Policies
 Precedence determines the order in which batches of policies are applied. Each batch is based on the role of the user who created the policy — insights\_admin or insights\_owner. After a match, no other policy is applied to the resource.

 Default: **Admin Policies** \(The set of policies that were created by users with the insights\_admin role.\)

 ![Precedence process](../image/precedence-diagram.png)

</td></tr><tr><td>

Advanced

</td><td>

Option to generate a single change request that applies to all CIs that match a policy \(default setting\) or a separate change request for each CI.Some attributes of the change request template have static/constant values that cannot be changed. Some attributes \(for example, risk and work\_notes\) have dynamic values that you can set using a script include.

</td></tr><tr class="sub-head"><td>

Auto-approval \(Standard Change\)

</td><td>

 

</td></tr><tr><td>

Single change request

</td><td>

Option for enabling the system to generate a single change request, which applies to all CIs that match the policy.

</td></tr><tr><td>

Script include

</td><td>

This field appears only when the **Advanced** check box is selected.

`CLINBHStandardChangeRequestUtil`The Change group is derived from the Standard Change template and cannot be overridden.

</td></tr><tr class="sub-head"><td>

Manual approval \(Normal Change\)

</td><td>

 

</td></tr><tr><td>

Single change request

</td><td>

Option for enabling the system to generate a single change request, which applies to all CIs that match the policy.

</td></tr><tr><td>

Script include

</td><td>

This field appears only when the **Advanced** check box is selected.

`CLINBHNormalChangeRequestUtil`

</td></tr><tr><td>

Notify when non-business hour spend exceeds \(%\) of total spend

</td><td>

Percentage of overall cloud spend on resources during business hours that triggers email notification to the users or groups that you specify.

Default: 15The value is calculated using the amount that could be saved if all Business hours recommendations are applied. The default value of 15 means that notifications are sent only when the cost of operation during non-business hours is greater than 15% of total costs.

</td></tr><tr><td>

Notify when unassigned resources exceed \(%\) of total CIs

</td><td>

The percentage of overall cloud spend for non-business hour usage that triggers email notification of the users or groups that you specify.The default value of **15** means that notifications are sent only when the cost of operation during non-business hours is greater than 15% of total costs.

</td></tr><tr><td>

Notify users / Notify groups

</td><td>

The users or groups to notify by email when the non-business hour spend exceeds the specified percentage of overall cloud spend. If you do not specify users or groups, then no notification is sent.

</td></tr><tr><td>

Maximum CIs per change

</td><td>

This field appears only when the **Single change request** check box is selected in the **Manual approval \(Normal Change\)** section.Maximum number of resources to associate with a single change request. If the maximum is reached, the system generates a new change request.

Default value: 1000

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Improve resource usage with Business hours](../concept/improve-res-use-business.md)

**Related topics**  


[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

