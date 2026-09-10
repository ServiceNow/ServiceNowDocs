---
title: Email notifications in Business Continuity Management
description: Email notifications are sent by the Business Continuity Management \(BCM\) application at different points in the Business Impact Analysis, planning, exercise, and crisis management lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/email-notifications-in-bcm.html
release: zurich
topic_type: reference
last_updated: "2026-07-24"
reading_time_minutes: 3
keywords: [BCM, email, notifications]
breadcrumb: [Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# Email notifications in Business Continuity Management

Email notifications are sent by the Business Continuity Management \(BCM\) application at different points in the Business Impact Analysis, planning, exercise, and crisis management lifecycle.

## Email notifications

An admin can modify email notifications to change when to send it, who receives it, and what it contains. For more information, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_CreateANotification.md).

The following tables describe the notifications, recipients, roles, and the associated conditions provisioned in the BCM application.

-   **Event-based notifications**

    Trigger automatically off a registered system event when qualifying data changes.

<table id="table_event_based_notifications_bcm"><thead><tr><th>

Purpose

</th><th>

Triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td colspan="3">

Notify BIA Updated

</td></tr><tr><td>

Notifies plan stakeholders of BIA changes.

</td><td>

A Business Impact Analysis record is updated.The system finds every plan that uses that BIA as a primary-scope asset and triggers once per matching plan.

</td><td>

Recipient: plan\_owner \(sn\_bcp\_plan\)Roles: sn\_bcp.plan\_manager \(can set or change plan\_owner\), sn\_bcp.plan\_admin \(can also write plan\_owner while the plan is in Draft, Review, or Returned state\)

</td></tr><tr><td colspan="3">

BIA Dependency Update Notification

</td></tr><tr><td>

Notifies reviewers of BIA dependency changes.

</td><td>

Triggers from the same BIA-update chain, routed through the shared DependencyUpdateContextBase helper.Condition: The matching sn\_bia\_dependency\_update\_config record has Send notification enabled.

</td><td>

Recipient: User or group fields listed in the User fields property of the matching sn\_bia\_dependency\_update\_config record, resolved per snapshot.Roles depend on which field the config points to. Plan owner: sn\_bcp.plan\_manager, sn\_bcp.plan\_admin. sn\_bia\_analysis.bcm\_lead: sn\_bia.bia\_manager or sn\_bia.bia\_planner \(BIA in Draft\), sn\_bia.bia\_admin \(BIA in Draft or Review\).

</td></tr><tr><td colspan="3">

BCP Dependency Update Notification

</td></tr><tr><td>

Notifies reviewers of plan dependency changes.

</td><td>

Same mechanism as the BIA Dependency Update Notification.Condition: The matching sn\_bcp\_dependency\_update\_config record has Send notification enabled, triggered on the plan rather than the BIA.

</td><td>

Recipient: User or group fields listed in the matching sn\_bcp\_dependency\_update\_config record's User fields property, resolved like the BIA Dependency Update Notification.Roles depend on which field the config points to. sn\_bcp\_plan.plan\_owner: sn\_bcp.plan\_manager, sn\_bcp.plan\_admin. sn\_bcp\_plan.bcm\_lead: sn\_bcp.plan\_contributor or sn\_bcp.plan\_manager \(plan in Draft\), sn\_bcp.plan\_admin \(plan in Draft or Review\).

</td></tr></tbody>
</table>-   **Workflow-driven notifications**

    Trigger directly from a record update condition or a Flow Designer state change, with no separate event registration involved.

<table id="table_workflow_driven_notifications_bcm"><thead><tr><th>

Notification

</th><th>

Purpose and triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td>

Notification for subscribed alert

</td><td>

Notifies people watching a crisis or threat alert that it changed.Triggered when an alert record is updated while it has one or more people on its watch list.

</td><td>

Recipient: watch\_list \(sn\_fam\_alert\)Roles: None. watch\_list carries no field-level ACL; any user with access to the alert record can add themselves or others as a watcher.

</td></tr><tr><td>

Send action email when an event task fails

</td><td>

Informs the task owner that their recovery event task failed.Triggered when an Event Task's state field changes to value 9 while it has an assigned owner.

Flow Designer trigger condition: `state CHANGES TO assigned_to IS NOT EMPTY` on sn\_recovery\_event\_task.

</td><td>

Recipient: assigned\_to \(sn\_recovery\_event\_task\)Roles: sn\_recovery.event\_user \(write access while the task is open or pending\), sn\_recovery.event\_manager \(write access whenever the user can edit the parent record\)

</td></tr></tbody>
</table>-   **Ad-hoc notifications**

    Started manually by a user, not triggered automatically by any record condition.

<table id="table_adhoc_notifications_bcm"><thead><tr><th>

Notification

</th><th>

Purpose

</th><th>

Triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td>

BCM Crisis Map Notification \("Notify Stakeholders"\)

</td><td>

Sends an alert notification to stakeholders during a crisis.

</td><td>

A user manually runs the Notify Stakeholders action on a Crisis Map alert \(sn\_fam\_alert\).There is no automatic condition on this action.

</td><td>

Recipient: Not a stored field. Recipients are computed at send time: either the specific users the sender picks, or contacts pulled from whichever resource records are marked as impacted.Roles: None. There is no role restriction on who can trigger the action; recipients are computed dynamically rather than role-gated.

</td></tr></tbody>
</table>
**Parent Topic:**[BCM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/bcm-reference.md)

