---
title: Email notifications in Operational Resilience
description: Email notifications are sent by the Operational Resilience application at different points in the service impact analysis, importance and impact tolerance assessment, vulnerability, and scenario analysis lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/email-notifications-in-opres.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Operational Resilience, email, notifications]
breadcrumb: [Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Email notifications in Operational Resilience

Email notifications are sent by the Operational Resilience application at different points in the service impact analysis, importance and impact tolerance assessment, vulnerability, and scenario analysis lifecycle.

## Email notifications

An admin can modify email notifications to change when to send it, who receives it, and what it contains. For more information, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateANotification.md).

The following tables describe the notifications, recipients, roles, and the associated conditions provisioned in the Operational Resilience application.

-   **Event-based notifications**

    Fire automatically off a registered system event when qualifying data changes.

<table id="table_event_based_notifications_opres"><thead><tr><th>

Notification and recipient

</th><th>

When sent

</th></tr></thead><tbody><tr><td colspan="2">

sn\_oper\_res.manager

</td></tr><tr><td>

Email assigned\_toRecipient: assigned\_to \(sn\_oper\_res\_service\_impact\_analysis\)

</td><td>

Service Impact Analysis is assigned

</td></tr><tr><td>

Questionnaire assignmentRecipient: assessor \(sn\_oper\_res\_importance\_impact\_tolerance\_assessment\)

</td><td>

State changes from Draft to Pending Response for legacy assessments with questionnaire template

</td></tr><tr><td>

Adding participantRecipient: participant \(sn\_oper\_res\_m2m\_analysis\_participant\)

</td><td>

Participant record is inserted or when re-notifying existing participants

</td></tr><tr><td>

Vulnerability assignmentRecipient: assigned\_to \(sn\_oper\_res\_vulnerability\)

</td><td>

assigned\_to is set on vulnerability

</td></tr><tr><td>

Vulnerability re-assignmentRecipient: assigned\_to \(sn\_oper\_res\_vulnerability\)

</td><td>

assigned\_to changes value

</td></tr><tr><td>

Vulnerability approved/rejectedRecipient: assigned\_to \(sn\_oper\_res\_vulnerability\)

</td><td>

State changes from Pending Approval to Approved, Treatment, or Assessment

</td></tr><tr><td>

sn\_oper\_res.manager, sn\_oper\_res.admin

</td><td>

 

</td></tr><tr><td>

Assessment assignmentRecipient: assigned\_to \(sn\_oper\_res\_importance\_impact\_tolerance\_assessment\)

</td><td>

Importance and Impact Tolerance Assessment is first assigned

</td></tr><tr><td>

Assessment re-assignmentRecipient: assigned\_to \(sn\_oper\_res\_importance\_impact\_tolerance\_assessment\)

</td><td>

assigned\_to changes

</td></tr><tr><td>

Assessment approved/rejectedRecipient: assigned\_to \(sn\_oper\_res\_importance\_impact\_tolerance\_assessment\)

</td><td>

State changes from Pending Approval to Approved or Analyze

</td></tr><tr><td>

Assessment canceledRecipient: assigned\_to, assessor, approver \(sn\_oper\_res\_importance\_impact\_tolerance\_assessment\)

</td><td>

State changes to Cancelled

</td></tr><tr><td>

Smart Assessment assignmentRecipient: assessor \(sn\_oper\_res\_importance\_impact\_tolerance\_assessment\)

</td><td>

Smart Assessment becomes ready \(state is Pending Response and assessor changes or state changes from Draft\)

</td></tr><tr><td>

Assignment notificationRecipient: assigned\_to \(sn\_oper\_res\_scenario\_analysis\)

</td><td>

Scenario Analysis is first assigned

</td></tr><tr><td>

Re-assigned notificationRecipient: assigned\_to \(sn\_oper\_res\_scenario\_analysis\)

</td><td>

assigned\_to changes value and is not empty

</td></tr><tr><td>

Approval/Reject notificationRecipient: assigned\_to \(sn\_oper\_res\_scenario\_analysis\)

</td><td>

State changes from Pending Plan Approval to Draft or Analyze

</td></tr><tr><td>

Approval/Reject notification - ResultRecipient: assigned\_to \(sn\_oper\_res\_scenario\_analysis\)

</td><td>

State changes from Pending Result Approval to Approved or Analyze

</td></tr><tr><td>

Canceled notificationRecipient: assigned\_to \(sn\_oper\_res\_scenario\_analysis\), participant \(sn\_oper\_res\_m2m\_analysis\_participant\)

</td><td>

State changes to Cancelled

</td></tr><tr><td>

Removing scenario eventRecipient: participant or assigned\_to \(sn\_oper\_res\_m2m\_analysis\_participant, sn\_oper\_res\_scenario\_analysis\)

</td><td>

Participant is swapped, response task is cancelled or deleted, or scenario event link is deleted

</td></tr><tr><td>

Sending response taskRecipient: response task's participant \(sn\_oper\_res\_response\_task\)

</td><td>

Response task is inserted \(typically when analysis state changes to Analyze\)

</td></tr><tr><td>

Receiving complete response taskRecipient: assigned\_to \(sn\_oper\_res\_scenario\_analysis\)

</td><td>

Response task state changes to Closed Complete

</td></tr><tr><td colspan="2">

sn\_oper\_res.manager, sn\_oper\_res.operational\_resilience\_business\_user, sn\_oper\_res.admin

</td></tr><tr><td>

Vulnerability canceledRecipient: assigned\_to, opened\_by, approvers, watch\_list \(sn\_oper\_res\_vulnerability\)

</td><td>

State changes to Cancelled

</td></tr><tr><td colspan="2">

Not gated by an Operational Resilience role anyone added to the case's watch list or set as analyst receives it.

</td></tr><tr><td>

DRI Source Record Change - Email NotificationRecipient: watch\_list, analyst \(sn\_grc\_inc\_rptg\_case\_task\)

</td><td>

Tracked field changes on an incident linked to a DRIR case \(beginning with version 23.0.4\). A banner also displays on the case.

</td></tr></tbody>
</table>-   **Workflow-driven notifications**

    None. Operational Resilience has five Flow Designer flows for approvals \(Scenario Analysis Plan Approval, Scenario Analysis Result Approval, Vulnerability approval, and Importance and Impact Tolerance Assessment Approval\). All five use the built-in Ask For Approval action rather than an app-owned Send Email step. They rely on the platform's Approval Requested, Approved, and Rejected notifications instead.

-   **Ad-hoc notifications**

    Started manually by a user, not fired automatically by any record condition.

<table id="table_adhoc_notifications_opres"><thead><tr><th>

Notification

</th><th>

Description

</th><th>

Recipient

</th><th>

Roles

</th></tr></thead><tbody><tr><td>

Smart Assessment contributors added

</td><td>

Sent when contributors are manually added to a Smart Assessment in the UI.

</td><td>

Contributors added by the user

</td><td>

Governed by Smart Assessment Engine contributor-management accessFor Digital resilience incident reporting assessments, see [Roles installed with Digital resilience incident reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/roles-with-drir.md).

</td></tr><tr><td>

Smart Assessment reassignment

</td><td>

Sent when a contributor is manually reassigned in the Smart Assessment UI.

</td><td>

Newly assigned contributor

</td><td>

Governed by Smart Assessment Engine contributor-management access

</td></tr></tbody>
</table>
## Example: DRI Source Record Change notification

The following example shows a generated "DRI Source Record Change - Email Notification," sent after tracked fields changed on the incident linked to a DRIR case.

Subject: `DRIR Case DRI0001014: Source Record Updated`

Body: `The source record linked to your DRIR case has been updated.`, followed by the case number, the source record number, who made the change and when, and each changed field with its old and new value. The email includes a link to view the case, but not a link to the source record itself.

\[Omitted image "incident-preview-email.png"\] Alt text: Preview of the DRI Source Record Change email, showing the case number, source record number, changed fields, and a link to view the case.

The underlying notification record shows the same subject, recipients \(the case's watch list and analyst, listed as individual email addresses\), and body content.

\[Omitted image "incident-email-notification.png"\] Alt text: Notification record for the DRI Source Record Change email, showing the subject, recipients, and body.

