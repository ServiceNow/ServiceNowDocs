---
title: Email notifications in Regulatory Change Management
description: Email notifications are sent by the Regulatory Change Management \(RCM\) application at different stages of the regulatory alert workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/regulatory-change-management-service-portal/email-notifications-in-rcm.html
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Reference, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Email notifications in Regulatory Change Management

Email notifications are sent by the Regulatory Change Management \(RCM\) application at different stages of the regulatory alert workflow.

## Email notifications

An admin can modify email notifications to change when to send it, who receives it, and what it contains. For more information, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_CreateANotification.md).

The following table describes the notifications, recipients, and the associated conditions provisioned in the RCM application.

-   **Workflow-driven notifications**

    Sent at different stages of the regulatory alert and action task lifecycle.

<table id="table_workflow_notifications_rcm"><thead><tr><th>

Notification

</th><th>

Purpose

</th><th>

Triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td>

Assign Regulatory Feed

</td><td>

Informs the coordinator that a regulatory alert has been assigned to them for triage.

</td><td>

Sent when a record is inserted or updated.Condition: Coordinator is set or changed.

</td><td>

Recipient: coordinator.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Assign Regulatory Change Task

</td><td>

Informs the assignee that a regulatory change task has been assigned, with its due date.

</td><td>

Sent when a record is inserted or updated.Condition: Assigned to is set or changed.

</td><td>

Recipient: assigned\_to.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Assign Source Document Import Task

</td><td>

Informs the assignee that a source document import task has been assigned, with its due date.

</td><td>

Sent when a record is inserted or updated.Condition: Assigned to is set or changed.

</td><td>

Recipient: assigned\_to.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Assign Regulatory Action Task

</td><td>

Informs the assignee that an action task has been assigned, with its due date.

</td><td>

Sent when a record is inserted or updated.Condition: Assigned to is set or changed.

</td><td>

Recipient: assigned\_to.email

 Roles: Compliance manager \(sn\_compliance.manager\), risk manager \(sn\_risk.manager\), compliance analyst \(sn\_compliance.user\), or risk analyst \(sn\_risk.user\)

</td></tr><tr><td>

Review Regulatory Change Task

</td><td>

Informs the approver that a regulatory change task is awaiting their review and approval.

</td><td>

Sent when a record is inserted or updated.Condition: Approval is for a regulatory change task and its state is Requested.

</td><td>

Recipient: approver.email

 Roles: RCM manager with sn\_grc\_reg\_change.manager role

</td></tr><tr><td>

Review Import Document Task

</td><td>

Informs the approver that a source document import task is awaiting their review and approval.

</td><td>

Sent when a record is inserted or updated.Condition: Approval is for an import document task and its state is Requested.

</td><td>

Recipient: approver.email

 Roles: RCM manager with sn\_grc\_reg\_change.manager role

</td></tr><tr><td>

Regulatory Change Task approved

</td><td>

Informs the assignee that the regulatory change task has been approved.

</td><td>

Sent when a record is updated.Condition: Approval state changes to Approved for a regulatory change task.

</td><td>

Recipient: sysapproval.assigned\_to

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Source Import Document Task approved

</td><td>

Informs the assignee that the source document import task has been approved.

</td><td>

Sent when a record is updated.Condition: Approval state changes to Approved for a source document import task.

</td><td>

Recipient: sysapproval.assigned\_to

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Reject Regulatory Change Task

</td><td>

Informs the assignee that the regulatory change task has been rejected.

</td><td>

Sent when a record is updated.Condition: Task is rejected.

</td><td>

Recipient: assigned\_to.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Reject Source Import Document Task

</td><td>

Informs the assignee that the source document import task has been rejected.

</td><td>

Sent when a record is updated.Condition: Task is rejected.

</td><td>

Recipient: assigned\_to.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Cancel Regulatory Change Task

</td><td>

Informs the assignee that the regulatory change task has been cancelled.

</td><td>

Sent when a record is updated. Condition: Task is cancelled.

</td><td>

Recipient: assigned\_to.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Source Import Document Task cancelled

</td><td>

Informs the assignee that the source document import task has been cancelled.

</td><td>

Sent when a record is updated. Condition: Task is cancelled.

</td><td>

Recipient: assigned\_to.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Regulatory Change Task request cancelled

</td><td>

Informs the assignee that the approval request for a regulatory change task has been cancelled.

</td><td>

Sent when a record is updated. Condition: Approval state changes to Cancelled for a regulatory change task.

</td><td>

Recipient: sysapproval.assigned\_to

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Import Document Task request cancelled

</td><td>

Informs the assignee that the approval request for a source document import task has been cancelled.

</td><td>

Sent when a record is updated. Condition: Approval state changes to Cancelled for a source document import task.

</td><td>

Recipient: sysapproval.assigned\_to

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr><tr><td>

Regulatory feed closed

</td><td>

Informs the coordinator that a regulatory alert has been closed.

</td><td>

Sent when a record is updated. Condition: Regulatory alert state changes to Closed.

</td><td>

Recipient: coordinator.email

 Roles: RCM user with sn\_grc\_reg\_change.user role

</td></tr></tbody>
</table>-   **Smart assessment notifications**

    Sent to notify users about regulatory assessments created, cancelled, or reassigned.

<table id="table_smart_assessment_notifications_rcm"><thead><tr><th>

Notification

</th><th>

Purpose

</th><th>

Triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td>

Smart assessment created

</td><td>

Informs the assessor that a smart assessment has been created from a regulatory alert.

</td><td>

Sent when a smart assessment creation event is fired from a regulatory alert.

</td><td>

Recipient: Assessment respondent

 Roles: Business user with sn\_grc.business\_user role

</td></tr><tr><td>

Smart assessment completed

</td><td>

Informs the requester that a smart assessment has been completed.

</td><td>

Sent when a smart assessment completion event is fired.

</td><td>

Recipient: Assessment requester

 Roles: Business user with sn\_grc.business\_user role

</td></tr><tr><td>

Smart assessment cancelled

</td><td>

Informs the assessor that a smart assessment has been cancelled.

</td><td>

Sent when a smart assessment cancellation event is fired, or when an alert is marked not applicable or cancelled.

</td><td>

Recipient: Assessment respondent

 Roles: Business user with sn\_grc.business\_user role

</td></tr><tr><td>

Smart assessment reassigned

</td><td>

Informs users that a smart assessment has been reassigned.

</td><td>

Sent when an assessment reassigned event is fired for an assessment scoped to a regulatory alert.

</td><td>

Recipient: Users

 Roles: Business user with sn\_grc.business\_user role

</td></tr></tbody>
</table>-   **Risk assessment notifications**

    Sent to notify users about risk assessments created, cancelled, or reassigned.

<table id="table_risk_assessment_notifications_rcm"><thead><tr><th>

Notification

</th><th>

Purpose

</th><th>

Triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td>

Notify assessor

</td><td>

Informs the assessor that a risk assessment is assigned to them.

</td><td>

Sent when a record is inserted or updated. Condition: State changes to In progress for an assessment scoped to a source record.

</td><td>

Recipient: assessor\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_assessor roles

</td></tr><tr><td>

Assessor changed

</td><td>

Informs the assessor that a risk assessment has been reassigned.

</td><td>

Sent when a record is inserted or updated. Condition: Assessor user changes while the assessment is in progress, for an assessment scoped to a source record.

</td><td>

Recipient: assessor\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_assessor roles

</td></tr><tr><td>

Approver changed

</td><td>

Informs the approver that a risk assessment has been reassigned for approval.

</td><td>

Sent when a record is inserted or updated. Condition: Approver user changes without a state change for an assessment scoped to a source record.

</td><td>

Recipient: approver\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_approver roles

</td></tr><tr><td>

Notify Approver to Approve Assessment

</td><td>

Informs the approver that a submitted risk assessment is awaiting their approval.

</td><td>

Sent when a record is inserted or updated.Condition: The approval state is Requested for a risk assessment.

</td><td>

Recipient: approver

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_approver roles

</td></tr><tr><td>

Notify assessor asmt cancellation

</td><td>

Informs the assessor that a risk assessment has been cancelled because the risk assessment methodology was retired.

</td><td>

Sent when a record is inserted or updated. Condition: State changes to Cancelled because the associated risk assessment methodology is retired, for an assessment scoped to a source record.

</td><td>

Recipient: assessor\_user, approver\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_assessor, sn\_risk\_advanced.ara\_approver roles

</td></tr><tr><td>

Request reassessment

</td><td>

Informs the assessor that a completed risk assessment needs to be reassessed by them.

</td><td>

Sent when a record is inserted or updated. Condition: State changes from Completed to an active assessment state for an assessment scoped to a source record.

</td><td>

Recipient: assessor\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_assessor roles

</td></tr></tbody>
</table>-   **Reminder notifications**

    Sent to notify users of regulatory alerts, action tasks, risk assessments and regulatory assessments nearing or past their due date.

<table id="table_reminder_notifications_rcm"><thead><tr><th>

Notification

</th><th>

Purpose

</th><th>

Triggering conditions

</th><th>

Recipient and roles

</th></tr></thead><tbody><tr><td>

Regulatory Change Task reminder

</td><td>

Informs the assignee that the regulatory change task assigned is due today.

</td><td>

Sent by the daily flow **Schedule notifications: Regulatory change task** on the due date.

</td><td>

Recipient: assigned\_to.email

 Roles: Business user with sn\_grc.business\_user role

</td></tr><tr><td>

Import Document Task reminder

</td><td>

Informs the assignee that the source document import task assigned is due today.

</td><td>

Sent by the daily flow **Schedule notifications: Source import document task** on the due date.

</td><td>

Recipient: assigned\_to.email

 Roles: Business user with sn\_grc.business\_user role

</td></tr><tr><td>

Regulatory Action Task last day

</td><td>

Informs the assignee that the action task assigned is due today.

</td><td>

Sent by the daily flow **Schedule notifications: Regulatory action task** on the due date.

</td><td>

Recipient: assigned\_to.email

 Roles: Compliance manager \(sn\_compliance.manager\), risk manager \(sn\_risk.manager\), compliance analyst \(sn\_compliance.user\), or risk analyst \(sn\_risk.user\)

</td></tr><tr><td>

Deferred Regulatory Feed reminder

</td><td>

Sends a review reminder to the coordinator of a deferred regulatory alert.

</td><td>

Sent when the coordinator on the deferred alert is set or changed.Sent by the daily flow **Schedule Notifications: Reminder for Deferred Regulatory Feed** on the reminder date set on the deferred alert.

</td><td>

Recipient: coordinator.email

 Roles: Business user with sn\_grc.business\_user role

</td></tr><tr><td>

Notify about Due Date Passed

</td><td>

Informs the assessor that a risk assessment has passed its due date.

</td><td>

Sent when a risk assessment past due date event is fired.

</td><td>

Recipient: assessor\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_assessor roles

</td></tr><tr><td>

Final Notification for Due Date passed

</td><td>

Sends a final reminder to the assessor that a risk assessment has passed its due date.

</td><td>

Sent when a final due date event is fired.

</td><td>

Recipient: assessor\_user

 Roles: Business user with sn\_grc.business\_user, sn\_risk\_advanced.ara\_assessor roles

</td></tr><tr><td>

Smart assessment overdue

</td><td>

Informs the assessor that a smart assessment is overdue.

</td><td>

Sent when a smart assessment overdue event is fired.

</td><td>

Recipient: Assessment respondent

 Roles: Business user with sn\_grc.business\_user role

</td></tr></tbody>
</table>
**Parent Topic:**[Regulatory Change Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/regulatory-change-management-service-portal/rcm-reference.md)

