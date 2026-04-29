---
title: Add an error budget policy form
description: Learn about the available fields for setting up error budget policies.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Add an error budget policy form

Learn about the available fields for setting up error budget policies.

## Fields in the Add an error budget policy form

The following table describes the available options in the Add an error budget policy form. For step-by-step instructions, see [Create SLOs, SLIs, and error budget policies](../task/sr-create-slo-sli.md).

<table id="table_rqy_bnq_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Display name of the error budget policy.

</td></tr><tr><td>

Threshold type

</td><td>

Select how you want to track your error budget.-   **Burn rate \(count\)**: Tracks how quickly the error budget is being consumed. A higher burn rate means faster consumption.
-   **Error budget remaining \(%\)**: Tracks the percentage of the error budget that’s still available during the specified period.

**Note:** You can add multiple thresholds to a policy, but each must be unique. If you try to add a duplicate threshold, an error message appears.

</td></tr><tr><td>

Threshold value

</td><td>

The point at which you get notified based on the selected SLO indicator.-   Burn rate: Set a value that indicates the burn rate is too high.

For example, to be notified when your service or configuration item is burning through its error budget twice as fast as expected, set the threshold to 2.

-   Error budget remaining: Set a value that indicates the remaining error budget is too low.

For example, to be notified when only 25% or less of the error budget remains, set the threshold to 25%.


**Note:** The threshold values support up to 4 decimal places and then round up.

</td></tr><tr><td>

Policy action

</td><td>

\[Optional\] If a breach occurs, select the action that you want to take:-   Create incident.
-   Send an email.
-   Notify Microsoft Teams.

If you select this option, you must also select a relevant notification destination. To set up a notification destination for your team, see [Create a notification destination in SRM](../task/create-notification-destination.md).

**Note:** To learn about the notifications that teams receive for breached error budget policies, see [Notifications for breached error budgets](srm-notifications-messages.md).


</td></tr></tbody>
</table>**Parent Topic:**[SLO Management reference](service-level-objective-management-reference.md)

