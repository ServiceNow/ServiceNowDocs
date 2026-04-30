---
title: Service Request case form
description: A government service agent can create a case using the Service Request case form to capture detailed information about questions, requests, and issues that constituents, business stakeholders, or agents have. Constituents, business stakeholders, or agents can also view the form to see the status of their requests and service cases.Service Request case form displays detailed information about a service request cae task.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Public Service Case Forms, Public Sector forms, Public Sector Digital Services reference, Public Sector Digital Services \(PSDS\)]
---

# Service Request case form

A government service agent can create a case using the Service Request case form to capture detailed information about questions, requests, and issues that constituents, business stakeholders, or agents have. Constituents, business stakeholders, or agents can also view the form to see the status of their requests and service cases.

A government service agent creates a case to identify a constituent's question or issue and to track the activities related to resolving the issue. An agent also uses a case to track communication to and from the constituent, including the communication channels being used.

Case activities include any action that is taken to resolve an issue. This can include phone calls or emails, knowledge base research, conversations with subject matter experts, and dispatch requests to field service agents, as well as other activities.

From the Case form, an agent can associate and store the related information, such as the constituent's name, phone number, and company; account information; product and asset information; service contract and entitlement details, and any associated service level agreements \(SLAs\).

There are several key features to a case.

-   Communication between an agent and the constituent or an agent and other employees within the organization. Details of all internal and external communication are recorded on the Case form.
-   Any additional tasks that result from a case, such as a work order. Tasks are tracked from a related list on the Case form. These tasks may be internal to the organization or they may involve the constituent.
-   Information from the case that can be included in the knowledge base and used to help resolve other cases.

There are two different Case form views: a detailed view that is available to agents and agent managers in the Public Sector Digital Services application and a simplified view that is available to external constituents from the Government Service Portal.

## Agent view

The agent view of the Case form includes the following components:

-   A timeline that provides a visual display of case activities.
-   Referenced entities for the case including account and contact information, product and asset information, service contract and service entitlement details, and any pertinent SLAs. Except for SLAs, this information exists in the system and can be associated with the case by the agent or agent manager.
-   All communication about the case, both external and internal. This information is stored in the **Additional comments** field \(external communication\), the **Work notes** field \(internal communication\), the **Resolution notes** field. The **Resolution notes** field stores details about the case resolution, and the **Activity** field, which stores all communication in a chronological list.

Agents and managers can view a Case form in the Public Sector Digital Services application by navigating to **Lists** &gt; **Service Requests** and selecting one of the following menu options:

-   **All**
-   **My Cases**
-   **My Open**
-   **Unassigned for my group**

From the Case list, click a case number to display the Case form.

<table id="table_ut3_b5r_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated number for the case. Numbers for cases use the default prefix GOVCS.

</td></tr><tr><td>

Opened

</td><td>

Date and time that the case was opened.

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

Constituent

</td><td>

Name of the constituent. If the constituent does not exist, the agent can create a constituent record from the case.

</td></tr><tr><td>

Priority

</td><td>

How quickly the agent should address the service request. Priority ranking is as follows:-   1 — Critical
-   2 — High
-   3 — Moderate
-   4 — Low \(default\)

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

Primary purpose

</td><td>

The reason that the constituent created the case: -   **Constituent Benefits**: services that constituents can apply for.
-   **Governance Procedures**: other types of cases such as Frauds, Appeals, Investigations, Complaints.

 Defaults to **Constituent Benefits**.

</td></tr><tr><td>

Service

</td><td>

The requested service indicated in the case. By default, this field will show public services with ‘Service type’ = Service Requests.

</td></tr><tr><td>

Assigned to agency

</td><td>

Name of the agency that is assigned with the case.

</td></tr><tr><td>

Requested by agency

</td><td>

Name of the agency that requested the case.

</td></tr><tr><td>

Assignment group

</td><td>

Assigned government service agent group.

</td></tr><tr><td>

Assigned to

</td><td>

Agent\(s\) the case is assigned to. If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Service

</td><td>

Requested service that is indicated in the case.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the question, request, or issue. Users can use the related search results to find a list of knowledge base articles with a possible solution.

</td></tr><tr><td class="sub-head" colspan="2">

Request Location

</td></tr><tr><td>

Address Type

</td><td>

The type of location where the issue is being reported. **Address** or **Intersection**

</td></tr><tr><td>

Street

</td><td>

The address where the issue is located. This field is only required if **Address**is selected as the Address type.

</td></tr><tr><td>

First Cross Street, Second Cross Street

</td><td>

The cross streets where the issue is located. This field is only required if **Intersection**is selected as the Address type.

</td></tr><tr><td>

City

</td><td>

The city where the issue is located.

</td></tr><tr><td>

State/Province

</td><td>

The state or province where the issue is located.

</td></tr><tr><td>

ZIP/Postal Code

</td><td>

The ZIP code or postal code where the issue is located.

</td></tr><tr><td>

Country

</td><td>

The country where the issue is located.

</td></tr><tr><td>

Latitude, Longitude

</td><td>

The coordinates where the issue is located. This field is required for either address type, and auto-populates based on the address data entered.

</td></tr><tr><td class="sub-head" colspan="2">

Request Details

</td></tr><tr><td>

Reported date

</td><td>

The date that the case was submitted. This field defaults to the case creation date but can be changed.

</td></tr><tr><td>

Description

</td><td>

A description about the case status.

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

Notes

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this case when additional comments are added or if the state of a case is changed to **Resolved** or **Closed**. Click the add me icon to add yourself to the watch list.

</td></tr><tr><td>

Work notes list

</td><td>

Internal users who receive a notification about this case when work notes are added. You can only add internal users to the work notes list.Click the **add me** icon to add yourself to the watch list.

</td></tr><tr><td>

Additional comments \(Constituent visible\)

</td><td>

More information about the issue as needed. All users who can view incidents can also see additional comments.

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

The agent to whom the case is assigned when the case is resolved.

</td></tr><tr><td>

Resolved

</td><td>

Date and time that the case was resolved.

</td></tr><tr><td>

Closed by

</td><td>

Name of the user who closed the case.

</td></tr><tr><td>

Closed

</td><td>

Date and time that the case was closed.

</td></tr><tr><td>

Resolution code

</td><td>

List of the resolution states for the case.This field is mandatory when an agent proposes a solution for a case.

 By default, this field is set to **Resources Not Approved**.

</td></tr><tr><td>

Cause

</td><td>

Details about the cause of the resolution.

</td></tr><tr><td>

Resolution notes

</td><td>

Details about how the case was closed. This field is mandatory if a government service agent or agent manager closes a case. If a constituent closes a case, it is not mandatory.

</td></tr><tr><td class="sub-head" colspan="2">

Related Records

</td></tr><tr><td>

Parent

</td><td>

Associated parent incident that makes the current incident a child incident. **Note:** When the parent incident is resolved, the child incident is also marked as resolved.

</td></tr><tr><td>

Problem

</td><td>

Any related problem record.

</td></tr><tr><td>

Change Request

</td><td>

Any related change request.

</td></tr><tr><td>

Caused by Change

</td><td>

Associated change request that prompted the creation of the incident.

</td></tr></tbody>
</table>## Constituent view

Users with the constituent or business contact role can view Case forms by selecting **Your Cases** in the government service portal header, then selecting the case number from the Case list.

The constituent or business contact view of the Case form includes the following components:

-   A process flow formatter that indicates the current state of the case.
-   The related entity information, including agency and contact information, pending service case task information, and service request information.
-   An **Activity** field that stores all communication for the case in a chronological list.

**Parent Topic:**[Public Sector Digital Services Core Case Forms](psds-case-forms.md)

## Service Request Case Task form

Service Request case form displays detailed information about a service request cae task.

The Service Request Case Task form displays information about service request case tasks, which are created and assigned to agents to complete the work to resolve service request cases.

The case task form includes the following fields.

<table id="table_case_tasks_form_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically assigned case task number.

</td></tr><tr><td>

Priority

</td><td>

Assigned priority:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)

</td></tr><tr><td>

Parent

</td><td>

Case that this case task was created for. This can be a case from the Case table \(sn\_gsm\_government\_service\_case\) or any child tables of the Case table.

</td></tr><tr><td>

State

</td><td>

Current state of the case task:-   Open
-   Awaiting Info
-   In Progress
-   Closed

</td></tr><tr><td>

Associated Table

</td><td>

Table associated with this task.

</td></tr><tr><td>

Associated Record

</td><td>

Records that are associated with this task.

</td></tr><tr><td>

Assigned to

</td><td>

Assigned user.

</td></tr><tr><td>

Subject

</td><td>

Subject of the case task.

</td></tr><tr><td>

Description

</td><td>

Description of the work that needs to be done in order to complete the case task.

</td></tr><tr><td>

Work Notes List

</td><td>

Customizable list of agents that can view the work notes.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Free-form private work note text viewable to assigned agents only.

</td></tr><tr><td>

Additional comments

</td><td>

Notes that are visible to the constituent. Agents can use this field to request more information from the constituent.

</td></tr></tbody>
</table>