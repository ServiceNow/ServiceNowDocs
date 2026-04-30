---
title: Set up escalation policies form in SRM
description: Escalation policies define the order and conditions in which members or devices receive notifications.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Reliability Management reference, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Set up escalation policies form in SRM

Escalation policies define the order and conditions in which members or devices receive notifications.

## Escalation policy form

<table id="table_escalation_policy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the escalation policy.

</td></tr><tr><td>

Active on shift

</td><td>

Team that receives the notifications on their shift..

</td></tr><tr><td>

Create from scratch

</td><td>

Option to create your own policy.

</td></tr><tr><td>

Create from template

</td><td>

Option to create a policy by using a template created by your admin.

</td></tr><tr><td>

Description

</td><td>

Text describing the policy.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the policy.

</td></tr><tr><td>

Use as default

</td><td>

Option to use this team as the default

</td></tr><tr><td>

Order

</td><td>

Order of execution. This is the hierarchy or chain of command. When there are multiple escalation policies with the same conditions for a team, the escalation policy with the smaller order number is executed first.

</td></tr><tr><td>

Conditions

</td><td>

Conditions for the policy. The table and conditions that define the escalation policy These conditions are checked after the escalation is started by an escalation trigger. If the conditions are met, the policy is run.

</td></tr><tr><td>

Escalation steps

</td><td>

Escalation steps to add. See the Escalation steps form for more information about the fields.

</td></tr><tr><td>

Escalation notifications

</td><td>

Notification conditions for the policy. **Note:** When user preference override is on, your escalation policy overrides any policy that the on-call agents set for their own notification preferences. When user preference override is off, the on-call agents' notification preferences take priority over this escalation policy.

</td></tr><tr><td>

Add notification step

</td><td>

Additional notification steps to add. You can select email, call, or SMS. You can add as many attempts as you like.

</td></tr></tbody>
</table>## Escalation steps form

|Field|Description|
|-----|-----------|
|Escalation step name|Name of the escalation step.|
|Order|Order of execution. This is the hierarchy or chain of command.|
|Responder level|Level of authority or expertise needed to respond to the incident.|
|Rotate through members|Option to notify all members, one by one, until one of them acknowledges the incident or until all of them are notified.|
|Additional audience|Specific users, teams, groups, or devices that you want to notify.|
|Time to next step after last notification|The maximum amount of time that will pass before the issue is escalated to the next step. For example, if a responder can't resolve the issue within 30 minutes of the notification, the issue is escalated to the manager.|

**Parent Topic:**[Service Reliability Management reference](service-reliability-management-reference.md)

