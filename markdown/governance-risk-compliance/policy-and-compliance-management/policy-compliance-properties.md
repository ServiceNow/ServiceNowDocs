---
title: Set notification properties
description: After an acknowledgement request has been sent to an audience, different reminder notifications are sent based on the timeliness and state of the response. Properties allow you to configure the notifications.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Policy and Compliance Management enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Set notification properties

After an acknowledgement request has been sent to an audience, different reminder notifications are sent based on the timeliness and state of the response. Properties allow you to configure the notifications.

These properties are available for Policy and Compliance Management.

**Note:** Navigate to **Policy and Compliance &gt; Administration &gt; Properties**.

<table id="table_dhr_rjk_3jb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specify how many days after due date to send Policy Acknowledge summary notification.

</td><td>

The number of days after an acknowledgement due date has passed before a Policy Acknowledge summary notification is sent.

</td></tr><tr><td>

States for which the control is active \(the first state is the default active state\)

</td><td>

States of the control in which it is considered active. The first state in the list is the default active state.

</td></tr><tr><td>

Number of days after Policy Acknowledgement Due Date to send overdue notification.

</td><td>

The number of days after an acknowledgement due date has passed before an overdue notification is sent.

</td></tr><tr><td>

Send a summary of the Policy Acknowledge after its due date. Use property sn\_compliance.policy\_ack\_after\_due\_summary\_timer to specify how many days after due date to send notification.

</td><td>

Select Yes to send a Policy Acknowledge summary notification after the days specified in the **Specify how many days after due date to send Policy Acknowledge summary notification** property has elapsed. For example, if the property is set to 1 day, the notification is sent when the acknowledgement is 1 day late.

</td></tr><tr><td>

Send a summary of the Policy Acknowledge before its due date. Use property sn\_compliance.policy\_ack\_before\_due\_summary\_timer to specify how many days before due date to send notification.

</td><td>

Select Yes to send a Policy Acknowledge summary notification prior to the number of days specified in the **Specify how many days after due date to send Policy Acknowledge summary notification** property is reached.For example, if the property is set to 1 day, the notification is sent 1 day before the due date.

</td></tr><tr><td>

Repeat the Policy Acknowledgement overdue notification daily

</td><td>

Select Yes to repeat the overdue notification on a daily basis until it is completed.

</td></tr><tr><td>

Number of days before Policy Acknowledgement Due Date to send reminder notification.

</td><td>

The number of days prior to the acknowledgement due date to begin sending reminder notifications.

</td></tr><tr><td>

Repeat the Policy Acknowledgement Due Date reminder daily until Policy Acknowledgement is due

</td><td>

Select Yes to send reminder notifications on a daily basis starting on the day determined by your setting in the **Number of days before Policy Acknowledgement Due Date** to send reminder notification property.For example, if you select Yes in this property and the due date occurs in 7 days, and you specified 3 days in the previous property, reminder notifications begin in 3 days and repeat daily.

</td></tr><tr><td>

Specify how many days before due date to send Policy Acknowledge summary notification.

</td><td>

The number of days prior to the due date to send the Policy Acknowledge summary notification.

</td></tr></tbody>
</table>**Parent Topic:**[Policy and Compliance Management enhancement steps](../../grc-policy-compliance-implementation/concept/policy-compliance-optional-steps.md)

