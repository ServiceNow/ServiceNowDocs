---
title: Government Service Case form
description: A government service agent creates a case to identify a constituent's request, and to track the activities related to resolving the issue. The Case form captures and displays detailed information about a constituent's issue or request.The Case form includes related lists that store case information and that agents can use to perform case-related tasks. Government agents are able to access a service request case, information request case, or license and permit case and view the following related lists.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Public Service Case Forms, Public Sector forms, Public Sector Digital Services reference, Public Sector Digital Services \(PSDS\)]
---

# Government Service Case form

A government service agent creates a case to identify a constituent's request, and to track the activities related to resolving the issue. The Case form captures and displays detailed information about a constituent's issue or request.

<table id="table_ut3_b5r_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated number for the case. Numbers for cases use the default prefix GOVCS.

</td></tr><tr><td>

Applicant type

</td><td>

Type of applicant:-   Individual
-   Business
-   Agency

</td></tr><tr><td>

Business

</td><td>

Name of the business. If the business does not exist, the agent can create a business record from the case.

</td></tr><tr><td>

Business contact

</td><td>

Name of the business contact. If the business contact does not exist, the agent can create a business contact record from the case.

</td></tr><tr><td>

Channel

</td><td>

Method by which the constituent initiated contact and the case was opened:-   Web \(default\)
-   Phone
-   Email
-   Chat
-   Social
-   Community
-   Alert
-   Virtual Agent
-   In Person

</td></tr><tr><td>

Constituent

</td><td>

Name of the constituent. If the constituent does not exist, the agent can create a constituent record from the case.

</td></tr><tr><td>

Requested by agency

</td><td>

Name of the agency that requested the case.

</td></tr><tr><td>

Assigned to agency

</td><td>

Name of the agency that is assigned with the case.

</td></tr><tr><td>

Service

</td><td>

The requested service indicated in the case.

</td></tr><tr><td>

Opened

</td><td>

Date and time that the case was opened.

</td></tr><tr><td>

Priority

</td><td>

The assigned priority:-   1 — Critical
-   2 — High
-   3 — Moderate
-   4 — Low \(default\)

</td></tr><tr><td>

Assignment group

</td><td>

Assigned government service agent group.

</td></tr><tr><td>

Assigned to

</td><td>

Assigned agent. If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Primary purpose

</td><td>

The reason that the constituent created the case: -   Constituent Benefits: services that constituents can apply for.
-   Governance Procedures: other types of cases such as Frauds, Appeals, Investigations, Complaints.

</td></tr><tr><td>

Partner

</td><td>

The name of the partner company.

</td></tr><tr><td>

Partner contact

</td><td>

The name of the partner contact for this case.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the question, request, or issue.

</td></tr><tr><td class="sub-head" colspan="2">

Applicant Information

</td></tr><tr><td>

Primary identification type

</td><td>

The type of document used as a constituent identification:-   Social Security Number
-   State Identification Number
-   Driver's License Number
-   Medicare ID

</td></tr><tr><td>

Identification field

</td><td>

One of the following fields based on the selection in the **Primary Identification type** field: -   Social Security Number
-   State Identification Number
-   Driver's License Number
-   Medicare ID

</td></tr><tr><td>

Email

</td><td>

The email address of the requester.

</td></tr><tr><td>

Street

</td><td>

The street name for the primary address.

</td></tr><tr><td>

City

</td><td>

The city for the primary address.

</td></tr><tr><td>

State/Province

</td><td>

The state or province for the primary address.

</td></tr><tr><td>

ZIP/Postal Code

</td><td>

The ZIP code or postal code for the primary address.

</td></tr><tr><td>

Country

</td><td>

The country of the requester.

</td></tr><tr><td class="sub-head" colspan="2">

Application Information

</td></tr><tr><td>

Reported date

</td><td>

The date that the case was submitted. This field defaults to the case creation date but can be changed.

</td></tr><tr><td>

Decision date

</td><td>

The date that a decision about the case was reached.

</td></tr><tr><td>

Application status

</td><td>

The status of the application: -   Approved
-   Declined

</td></tr><tr><td>

Description

</td><td>

A description about the case status.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this case when additional comments are added or if the state of a case is changed to **Resolved** or **Closed**. Click the add me icon to add yourself to the watch list.

</td></tr><tr><td>

Work notes list

</td><td>

Internal users who receive a notification about this case when work notes are added. You can only add internal users to the work notes list.Click the add me icon to add yourself to the watch list.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Comments for the case that are visible to the constituent.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the case or steps taken to resolve it, if applicable.

 Internal users who have been added to the Work notes list receive a notification that Case work notes have been added.

 You can configure the notification, as required. The notes are viewable by the admin, agent, and agent manager.

</td></tr><tr><td class="sub-head" colspan="2">

Contributors

</td></tr><tr><td>

Contributor Users

</td><td>

When a user with the case task agent role \(sn\_customerservice.case\_task\_agent\) is assigned to a case task, the user is added to the **Contributor Users** field.If this user is removed from the **Assigned to** field on the Case Task form, and this user is not assigned to any other tasks for the case, the user is also removed from the **Contributor Users** field.

</td></tr><tr><td>

Contributor Groups

</td><td>

When a user with the case task agent role \(sn\_customerservice.case\_task\_agent\) is assigned to a case task, the user's assignment group is added to the **Contributor Groups** field.If the user is removed from the **Assigned to** field on the Case Task form, and no other member of their assignment group is assigned to any other tasks for the case, the assignment group is removed from the **Contributor Groups** field.

 If a group is removed from the **Assignment group** field on the Case Task form, and the group is not assigned to any other tasks for the case, the assignment group is removed from the **Contributor Groups** field.

</td></tr><tr><td class="sub-head" colspan="2">

Resolution Information

</td></tr><tr><td>

Resolved by

</td><td>

Agent that the case is assigned to when the case is resolved.

</td></tr><tr><td>

Resolved

</td><td>

Date and time that the case was resolved.

</td></tr><tr><td>

Resolution code

</td><td>

List of the resolution states for the case.This field is mandatory when an agent proposes a solution for a case.

</td></tr><tr><td>

Closed by

</td><td>

Name of the user who closed the case.

</td></tr><tr><td>

Closed

</td><td>

Date and time that the case was closed.

</td></tr><tr><td>

Cause

</td><td>

Details about the cause of the resolution.

</td></tr><tr><td>

Resolution notes

</td><td>

Details about how the case was closed. This field is mandatory if a customer service agent or agent manager closes a case. If a constituent closes a case, it is not mandatory.

</td></tr></tbody>
</table>**Parent Topic:**[Public Sector Digital Services Core Case Forms](psds-case-forms.md)

## Government Service Case form related lists

The Case form includes related lists that store case information and that agents can use to perform case-related tasks. Government agents are able to access a service request case, information request case, or license and permit case and view the following related lists.

<table id="table_wlv_sab_tt"><thead><tr><th>

Related List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case Tasks

</td><td>

Tasks that have been created for this case by the government service agent or agent manager. When you create a task or change the state of a task, the information is recorded in the case **Activity** field. When you create a case task, the system generates a task number with a prefix. New and existing case tasks, regardless of state, both use the CSTASK prefix.

</td></tr><tr><td>

Related Parties

</td><td>

A list of related parties, such as contacts or constituents added to the case.

</td></tr><tr><td>

Related Cases

</td><td>

A list of cases created for the same account or contact.

</td></tr><tr><td>

Work Orders

</td><td>

A list of work orders created for this case.

</td></tr><tr><td>

Interactions

</td><td>

A comprehensive list of interactions created between constituents and government service agent for this case. Interactions use the IMS prefix.

</td></tr><tr><td>

SLAs

</td><td>

The service level agreements that are associated with this case.

</td></tr><tr><td>

Draft Emails

</td><td>

Emails that are unsent.

</td></tr><tr><td>

Emails

</td><td>

The case email log. A list of the emails that are sent or received as part of resolving this case. The government service agent or agent manager can send email from within the case, such as updates and inquiries to constituents or other agents or parties. A change in the state of the case triggers an automatic email to be sent to the constituent.

 Constituent contacts can create and update cases by email as well as receive updates from government service agents.

</td></tr><tr><td>

Blocked Tasks

</td><td>

A list of blocking tasks that have been created for this case. A blocking task is something that prevents the agent from making progress toward case resolution.

</td></tr><tr><td>

Escalations

</td><td>

A list of escalation records that are related to this case.

</td></tr><tr><td>

Attached Knowledge

</td><td>

Knowledge articles attached as a proposed solution to the case.

</td></tr><tr><td>

Knowledge Gaps

</td><td>

Feedback tasks that are created when a knowledge gap is reported.

</td></tr><tr><td>

Appointments

</td><td>

Appointments that the government agent makes with the constituent or others as part of resolving this case. When you create an appointment, an appointment creation message is recorded in the case **Activity** field. The user selected in the **To** field on the appointment form receives an email with the appointment details.

</td></tr></tbody>
</table>