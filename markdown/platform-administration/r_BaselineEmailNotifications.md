---
title: Baseline email notifications
description: The baseline system provides several email notifications.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Baseline email notifications

The baseline system provides several email notifications.

Some events listed in this table do not appear in a business rule and are fired by other conditions in the platform. Some events are hardcoded and are not user configurable.

**Note:** The below table list is not an exhaustive list. Products can create their own notifications.

<table id="table_pvq_dns_z4"><thead><tr><th>

Email notification

</th><th>

Description

</th><th>

Triggering event

</th><th>

Business Rule Controlling Event

</th></tr></thead><tbody><tr><td>

Appointment Invite

</td><td>

Type: Meeting Invitation

 Adds a meeting invitation to the recipient’s calendar by sending an iCalendar formatted email

</td><td>

itil\_appointment.inserted

</td><td>

Global business rule

</td></tr><tr><td>

Appointment Update

</td><td>

Type: Meeting Invitation

 Updates an existing meeting in the recipient’s calendar by sending an iCalendar formatted email

</td><td>

itil\_appointment.updated

</td><td>

Global business rule

</td></tr><tr><td>

Approval Rejected

</td><td>

Type: EMAIL

 A task-based approval has been rejected – includes the approver’s name.

</td><td>

approval.rejected

</td><td>

approver events

</td></tr><tr><td>

Approval Rejected by Other

</td><td>

Type: EMAIL

 A task-based approval has been rejected – includes the approver’s name.

</td><td>

approval.rejected.by.other

</td><td>

approval events

</td></tr><tr><td>

Approval Request

</td><td>

Type: EMAIL

 Sends an email for the recipient to reply with an approval decision. In the approval email, the recipient selects a link that builds the appropriate reply email. These emails come only from task-based approvals.

</td><td>

approval.inserted

</td><td>

approver changes

</td></tr><tr><td>

Catalog Approval Rejected

</td><td>

Type: EMAIL

 A catalog request has been rejected – includes the approver’s name.

</td><td>

request.approval.rejected

</td><td>

approval events

</td></tr><tr><td>

Catalog Approval Request

</td><td>

Type: EMAIL

 A catalog request for which you were an approver has been cancelled.

</td><td>

request.approval.cancelled

</td><td>

approver changes

</td></tr><tr><td>

Catalog Approval Request

</td><td>

Type: EMAIL

 A catalog request for which you are an approver has been made.

</td><td>

request.approval.inserted

</td><td>

approval events

</td></tr><tr><td>

Certificate Expired

</td><td>

Type: EMAIL

 Notification that the X.509 certificate has expired.

</td><td>

certificate.expired

</td><td>

certificate events

</td></tr><tr><td>

Certificate Expiring

</td><td>

Type: EMAIL

 Notification that the X.509 certificate is expiring in N days.

</td><td>

certificate.expiring

</td><td>

certificate events

</td></tr><tr><td>

Change approved

</td><td>

Type: EMAIL

 A change request has been approved.

</td><td>

change.approved

</td><td>

Change events and task events

</td></tr><tr><td>

Change assigned to me

</td><td>

Type: EMAIL

 A change request has been assigned to you.

</td><td>

change.assigned

</td><td>

Change events

</td></tr><tr><td>

Change assigned to my group

</td><td>

Type: EMAIL

 A change request has been assigned to your group.

</td><td>

change.assigned.to.group

</td><td>

Change events

</td></tr><tr><td>

Change commented \(to assignee\)

</td><td>

Type: EMAIL

 A comment has been added to a change request. The person assigned to the change request receives an email notification.

</td><td>

change.commented

</td><td>

Change events

</td></tr><tr><td>

Change commented \(unassigned\)

</td><td>

Type: EMAIL

 A comment has been added to a change request. The assignment group assigned to the change request receives an email notification.

</td><td>

change.commented

</td><td>

Change events

</td></tr><tr><td>

Change Notification

</td><td>

Type: EMAIL

 Notification of a change in the fields label in a form.

</td><td>

label.notify

</td><td>

 

</td></tr><tr><td>

Change rejected

</td><td>

Type: EMAIL

 A change request has been rejected.

</td><td>

change.rejected

</td><td>

Change events and task events

</td></tr><tr><td>

Change Task worknoted \(unassigned\)

</td><td>

Type: EMAIL

 A work note has been added to a change task. The assignment group assigned to the change task receives an email notification.

</td><td>

change\_task.worknoted

</td><td>

Change task events

</td></tr><tr><td>

Change Task worknoted \(to assignee\)

</td><td>

Type: EMAIL

 A work note has been added to a change task. The person assigned to the change task receives an email notification.

</td><td>

change\_task.worknoted

</td><td>

Change task events

</td></tr><tr><td>

Change Task assigned to my group

</td><td>

Type: EMAIL

 A change task has been assigned to your group.

</td><td>

change\_task.assigned.to.group

</td><td>

Change task events

</td></tr><tr><td>

Change Task assigned to me

</td><td>

Type: EMAIL

 A change task has been assigned to you.

</td><td>

change\_task.assigned

</td><td>

Change task events

</td></tr><tr><td>

Change worknoted \(to assignee\)

</td><td>

Type: EMAIL

 A work note has been added to a change request. The person assigned to the change request receives an email notification.

</td><td>

change.worknoted

</td><td>

Change events

</td></tr><tr><td>

Change worknoted \(unassigned\)

</td><td>

Type: EMAIL

 A work note has been added to a change request. The assignment group assigned to the change request receives an email notification.

</td><td>

change.worknoted

</td><td>

Change events

</td></tr><tr><td>

Email assigned to

</td><td>

Type: EMAIL

 An incident has been assigned to you \(the recipient of the email\).

</td><td>

incident.assigned

</td><td>

incident.events

</td></tr><tr><td>

Email assigned to \(sc\_task\)

</td><td>

Type: EMAIL

 A task has been assigned to you \(the recipient of the email\).

 **Note:** This email notification was used for the legacy Delivery Plan system of email notifications. In order to use this email notification with a workflow, the **work\_start** field needs to be set by the workflow using a Set Value activity.

</td><td>

sc\_task.assigned.to.user

</td><td>

sc\_task\_events

</td></tr><tr><td>

Email assigned To Group

</td><td>

Type: EMAIL

 An incident has been assigned to an assignment group of which you are a member \(the recipient of the email\).

</td><td>

incident.assigned.to.group

</td><td>

incident events

</td></tr><tr><td>

Email assigned to group \(sc\_task\)

</td><td>

Type: EMAIL

 A Service Catalog task has been assigned to an assignment group of which you are a member \(the recipient of the email\).

</td><td>

sc\_task.assigned.to.group

</td><td>

sc\_task\_events

</td></tr><tr><td>

Incident Closed

</td><td>

Type: EMAIL

 An incident opened by you \(the recipient of the email\), has been closed.

</td><td>

incident.updated

</td><td>

incident events

</td></tr><tr><td>

Incident Commented

</td><td>

Type: EMAIL

 An incident opened by you \(the recipient of the email\) has had comments added. This notification uses a template for an employee self-service \(ESS\) user.

</td><td>

incident.commented

</td><td>

incident events

</td></tr><tr><td>

Incident Commented

</td><td>

Type: EMAIL

 An incident assigned to you \(the recipient of the email\) has had comments added. This notification uses a template for an ITIL user.

</td><td>

incident.commented

</td><td>

incident events

</td></tr><tr><td>

Incident Opened

</td><td>

Type: EMAIL

 An incident has been opened for you \(the recipient of the email\) by someone else. This notification uses a template for an employee self-service \(ESS\) user.

</td><td>

incident.inserted

</td><td>

incident events

</td></tr><tr><td>

Incident Opened &amp; Unassigned

</td><td>

Type: EMAIL

 An incident has been opened and is unassigned. This notification uses a template for an ITIL user.

</td><td>

incident.inserted

</td><td>

incident events

</td></tr><tr><td>

Incident Resolved

</td><td>

Type: EMAIL

 An incident opened by you has been resolved, and feedback is required to determine if the incident should be closed.

</td><td>

incident.updated

</td><td>

incident events

</td></tr><tr><td>

Knowledge Closed Created

</td><td>

Type: EMAIL

 A contributor’s submission to the Knowledge Base was accepted and an article was created.

</td><td>

kb.submission.closed\_created

</td><td>

KB event

</td></tr><tr><td>

Knowledge Closed Duplicate

</td><td>

Type: EMAIL

 A contributor’s submission to the Knowledge Base was determined to be a duplicate, and no article was created.

</td><td>

kb.submission.closed\_duplicate

</td><td>

KB event

</td></tr><tr><td>

Knowledge Closed Invalid

</td><td>

Type: EMAIL

 A contributor’s submission to the Knowledge Base was determined to be invalid \(unusable\).

</td><td>

kb.submission.closed\_invalid

</td><td>

KB event

</td></tr><tr><td>

Notify Change Calendar

</td><td>

Type: Meeting Invitation

 Notifies the recipients of the schedule for a change request and exports the schedule to the Microsoft Outlook calendar. The email is in the format of iCalendar formatted email.

</td><td>

change.calendar.notify

</td><td>

change events

</td></tr><tr><td>

Notify Change Calendar Remove

</td><td>

Type: Meeting Invitation

 Notifies the recipients that a scheduled change has been closed or assigned to someone else and removes the entry from the Microsoft Outlook calendar. The email is in the format of iCalendar formatted email.

</td><td>

change.calendar.notify.remove

</td><td>

change events

</td></tr><tr><td>

Problem Task assigned to me

</td><td>

Type: EMAIL

 A problem task has been assigned to you.

</td><td>

problem\_task.assigned

</td><td>

Problem task events

</td></tr><tr><td>

Problem Task assigned to my group

</td><td>

Type: EMAIL

 A problem task has been assigned to your group.

</td><td>

problem\_task.assigned.to.group

</td><td>

Problem task events

</td></tr><tr><td>

Problem Task worknoted \(to assignee\)

</td><td>

Type: EMAIL

 A work note has been added to a problem task. The person assigned to the problem task receives an email notification.

</td><td>

problem\_task.worknoted

</td><td>

Problem task events

</td></tr><tr><td>

Problem Task worknoted \(unassigned\)

</td><td>

Type: EMAIL

 A work note has been added to a problem task. The assignment group assigned to the problem task receives an email notification.

</td><td>

problem\_task.worknoted

</td><td>

Problem task events

</td></tr><tr><td>

Problem worknoted \(to assignee\)

</td><td>

Type: EMAIL

 A work note has been added to a problem. The person assigned to the problem receives an email notification.

</td><td>

problem.worknoted

</td><td>

Problem events

</td></tr><tr><td>

Problem worknoted \(unassigned\)

</td><td>

Type: EMAIL

 A work note has been added to a problem. The assignment group assigned to the problem receives an email notification.

</td><td>

problem.worknoted

</td><td>

Problem events

</td></tr><tr><td>

Reminder Insert

</td><td>

Type: Meeting Invitation

 Creates a calendar reminder regarding an open task. The email is in the format of iCalendar formatted email.

</td><td>

reminder.notify

</td><td>

 

</td></tr><tr><td>

Reminder Insert

</td><td>

Type: Meeting Invitation

 A task has been closed or deleted. This notification removes the task reminder from Outlook. The email is in the format of iCalendar formatted email.

</td><td>

reminder.notify.delete

</td><td>

 

</td></tr><tr><td>

Reminder Insert Email

</td><td>

Type: EMAIL

 Sends the recipient a reminder email about a specific task.

</td><td>

reminder.notify.email

</td><td>

 

</td></tr><tr><td>

Request Approved

</td><td>

Type: EMAIL

 A Service Catalog request, opened by the recipient, has been approved.

</td><td>

sc\_request.approved

</td><td>

sc\_request events

</td></tr><tr><td>

Request Assigned

</td><td>

Type: EMAIL

 A Service Catalog request has been assigned to the recipient.

</td><td>

sc\_request.assigned

</td><td>

sc\_request events

</td></tr><tr><td>

Request Completed

</td><td>

Type: EMAIL

 A Service Catalog request, opened by the recipient, has been completed.

</td><td>

sc\_request.updated

</td><td>

sc\_request events

</td></tr><tr><td>

Request Item Assigned

</td><td>

Type: EMAIL

 An item requested from the Service Catalog has been assigned to you.

</td><td>

sc\_req\_item.assigned

</td><td>

sc\_request events

</td></tr><tr><td>

Request Item Delivery

</td><td>

Type: EMAIL

 An item requested from the Service Catalog by the recipient is being delivered.

</td><td>

sc\_req\_item.delivery

</td><td>

sc\_request events

</td></tr><tr><td>

Request Opened on Behalf

</td><td>

Type: EMAIL

 A Service Catalog request has been opened on behalf of the recipient.

</td><td>

sc\_request.requested\_for

</td><td>

sc\_request events

</td></tr><tr><td>

Reset Password

</td><td>

Type: EMAIL

 The recipient’s password has been reset as requested.

</td><td>

reset.password

</td><td>

 

</td></tr><tr><td>

Scheduled Import Completed

</td><td>

Type: EMAIL

 A scheduled import set has completed.

</td><td>

scheduled\_import\_set.completed

</td><td>

 

</td></tr><tr><td>

System Upgraded

</td><td>

Type: EMAIL

 The recipient’s system has been upgraded.

</td><td>

system.upgraded

</td><td>

 

</td></tr><tr><td>

Task approved

</td><td>

Type: EMAIL

 An ITIL task has been approved.

</td><td>

task.approved

</td><td>

Change events and task events

</td></tr><tr><td>

Text Index Completed

</td><td>

Type: EMAIL

 A scheduled system index has completed.

</td><td>

text\_index.complete

</td><td>

 

</td></tr><tr><td>

Unscheduled Change

</td><td>

Type: EMAIL

 A named configuration item has changed, and no active change request exists.

</td><td>

cmdb.unscheduled.change

</td><td>

 

</td></tr></tbody>
</table>**Note:**

**Parent Topic:**[Create an email notification](../../notification/task/t_CreateANotification.md)

