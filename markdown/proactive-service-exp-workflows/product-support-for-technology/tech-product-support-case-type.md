---
title: Technology Product Support case type
description: The Technology Product Support case type enables technology companies to provide support for digital products and services.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Technology Product Support Case, Explore, Product Support for Technology]
---

# Technology Product Support case type

The Technology Product Support case type enables technology companies to provide support for digital products and services.

A case types represents the processes and the data that are needed to resolve a specific type of customer issue. The Technology Product Support case type includes the table, roles, SLAs, email notifications, and other items needed to resolve technology issues.

The Technology Product Support Case application \(sn\_tech\_product\_support\) includes the Technology Product Support case type. To view a list of available case types, navigate to **Customer Service** &gt; **Case Types** &gt; **Manage Case Types**.

The Technology Product Support case type includes the following items.

<table id="table_r3g_bvl_y1c"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tables

</td><td>

The Technology Product Support Case application includes the Tech Product Support Case \[sn\_tech\_product\_support\_case\] table. This table extends the Case table and can be extended.For a detailed description of the Tech Product Support Case table, including field descriptions, see [Tech Product Support Case table](../reference/tech-product-support-case-table.md).

</td></tr><tr><td>

[Roles](tech-product-support-case-type.md#section_fwf_mlg_n1c)

</td><td>

Roles control access to features and capabilities in the Technology Product Support Case application, menu, and modules.

</td></tr><tr><td>

[Case states](tech-product-support-case-type.md#section_jtm_rjs_y1c)

</td><td>

Technology product support cases follow a specific life cycle and move through a series of states from creation to closure.

</td></tr><tr><td>

[State flows](tech-product-support-case-type.md#section_zmc_ptf_n1c)

</td><td>

State flows are customized transitions from one state to another, such as when an agent moves a technology product support case from Work in Progress to Awaiting Info.

</td></tr><tr><td>

[List views](tech-product-support-case-type.md#section_sh1_l3g_n1c)

</td><td>

The Technology Product Support Case application includes list views for CSM/FSM Configurable Workspace and for Core UI that appear in the application navigator.

</td></tr><tr><td>

[Special handling notes](tech-product-support-case-type.md#section_h4k_rvg_n1c)

</td><td>

Special handling notes bring important information to an agent's attention.

</td></tr><tr><td>

[Service definitions](tech-product-support-case-type.md#section_hjj_5jd_y1c)

</td><td>

Service definitions enable customers to quickly discover and request the services they need and agents to create cases of the right type to support those requests.

</td></tr><tr><td>

[Email notifications and email templates](tech-product-support-case-type.md#section_dwg_242_y1c)

</td><td>

Email notifications are sent to the contact and, in some cases, to users on the case watch list for specific actions. The system uses email templates to create these notifications.

</td></tr><tr><td>

[Provider notifications](tech-product-support-case-type.md#section_ahk_lyj_y1c)

</td><td>

Provider notifications for agents are sent following updates to technology product support cases.

</td></tr><tr><td>

[Service level agreement \(SLA\) definitions](tech-product-support-case-type.md#section_vvh_sbl_y1c)

</td><td>

An SLA definition includes the timing, conditions, workflows, and other information required to create and progress task SLAs.

</td></tr><tr><td>

[Record producer](tech-product-support-case-type.md#section_y4c_hgy_1bc)

</td><td>

A record producer is a specific type of catalog item that allows end users to create task-based records from a service catalog. The Technology Product Support Case application includes the following record producer: **Create a Technology Product Case**.

</td></tr><tr><td>

[Case action status](tech-product-support-case-type.md#section_fvz_mrg_n1c)

</td><td>

The case action status feature enables agents to easily identify cases that need attention.

</td></tr><tr><td>

[Field indicators and highlights](tech-product-support-case-type.md#section_xsn_gwd_y1c)

</td><td>

The Technology Product Support case type uses field indicators and field highlights to indicate information about cases.

</td></tr><tr><td>

[Auto close cases](tech-product-support-case-type.md#section_j3p_rsg_n1c)

</td><td>

Cases in the Resolved state can be closed automatically if customers do not take any action.

</td></tr></tbody>
</table>## Roles

User roles available with the Technology Product Support Case application address the diverse skill sets needed to resolve complex technical issues. These roles enable users to research technical issues, collaborate with development teams, and implement advanced troubleshooting techniques.

<table id="table_zp1_plg_n1c"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Customer \[sn\_tech\_support.customer\]

</td><td>

Users with this role:-   Can view technology product support cases in the Customer Service Portal.
-   Have write access to the **Steps to reproduce** field.

</td><td>

-   sn\_customerservice.customer
-   sn\_tech\_support.creator
-   sn\_tech\_support.writer

</td></tr><tr><td>

Customer admin\[sn\_tech\_support.customer\_admin\]

</td><td>

Users with this role:-   Can view technology product support cases in the Customer Service Portal.
-   Have write access to the **Steps to reproduce** field.

</td><td>

-   sn\_customerservice.customer\_admin
-   sn\_tech\_support.creator
-   sn\_tech\_support.writer

</td></tr><tr><td>

Partner \[sn\_tech\_support.partner\]

</td><td>

Users with this role:-   Can view technology product support cases in the Customer Service Portal.
-   Have write access to the **Steps to reproduce** field.

</td><td>

-   sn\_customerservice.partner
-   sn\_tech\_support.creator
-   sn\_tech\_support.writer

</td></tr><tr><td>

Partner admin\[sn\_tech\_support.partner\_admin\]

</td><td>

Users with this role:-   Can view technology product support cases in the Customer Service Portal.
-   Have write access to the **Steps to reproduce** field.

</td><td>

-   sn\_customerservice.partner\_admin
-   sn\_tech\_support.creator
-   sn\_tech\_support.writer

</td></tr><tr><td>

Agent\[sn\_tech\_support.agent\]

</td><td>

An agent role for the Technology Product Support Case application.

</td><td>

-   sn\_customerservice\_agent
-   sn\_incident\_write
-   sn\_problem\_write
-   sn\_request\_write
-   sn\_change\_write
-   sn\_tech\_support.writer
-   sn\_tech\_support.creator
-   sn\_tech\_support.navigation\_menu

</td></tr><tr><td>

Creator\[sn\_tech\_support.creator\]

</td><td>

Users with this role can create technology product support cases.

</td><td>

 

</td></tr><tr><td>

Developer\[sn\_tech\_support.developer\]

</td><td>

A developer role for the Technology Product Support Case application.

</td><td>

-   sn\_customerservice.case\_task\_agent
-   sn\_incident\_write
-   sn\_problem\_write
-   sn\_request\_write
-   sn\_change\_write
-   sn\_tech\_support.viewer
-   sn\_tech\_support.navigation\_menu

</td></tr><tr><td>

Report viewer\[sn\_tech\_support.report\_viewer\]

</td><td>

Provides report viewer access to Technology Product Support cases.

</td><td>

 

</td></tr><tr><td>

Viewer\[sn\_tech\_support.viewer\]

</td><td>

Provides read-only access to technology product support cases.

</td><td>

 

</td></tr><tr><td>

Writer\[sn\_tech\_support.writer\]

</td><td>

Provides write access to technology product support cases.

</td><td>

sn\_tech\_support.viewer

</td></tr><tr><td>

Major case manager\[sn\_tech\_support.major\_case\_manager\]

</td><td>

Users with the major case manager role can:-   Create major cases
-   Approve or reject major case candidates
-   Add or remove child cases from major cases
-   Add or remove impacted accounts or consumers

For more information, see Major issue management overview.

</td><td>

-   sn\_majorissue\_mgt.major\_issue\_manager
-   sn\_incident\_write
-   sn\_problem\_write
-   sn\_request\_write
-   sn\_change\_write
-   sn\_tech\_support.writer
-   sn\_tech\_support.creator
-   sn\_tech\_support.navigation\_menu

</td></tr><tr><td>

Resource manager\[sn\_tech\_support.resource\_manager\]

</td><td>

Users with this role can assign technology product support cases to agents.

</td><td>

-   sn\_customerservice\_agent
-   sn\_incident\_write
-   sn\_problem\_write
-   sn\_request\_write
-   sn\_change\_write
-   sn\_tech\_support.writer
-   sn\_tech\_support.creator
-   sn\_tech\_support.navigation\_menu

</td></tr><tr><td>

Navigation menu\[sn\_tech\_support.navigation\_menu\]

</td><td>

Provides access to the Technology Product Support Cases menu and modules in the application navigator.

</td><td>

 

</td></tr></tbody>
</table>## Case states

A Technology Product Support case can be in any of the following case states.

<table id="table_nyz_jg2_y1c"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

A case that is being created but is not yet submitted.

</td></tr><tr><td>

New

</td><td>

A case moves from Draft to New when it is submitted or when the case intake is completed.

</td></tr><tr><td>

Work in Progress

</td><td>

An agent accepts an assigned case or selects the **Assign to me** action and sets the state to Work in Progress.If a customer rejects a proposed solution, the case returns to the Work in Progress state.

</td></tr><tr><td>

Awaiting Info

</td><td>

The agent requests additional information from the customer.

</td></tr><tr><td>

Solution Proposed

</td><td>

The agent proposes a solution to the customer.

</td></tr><tr><td>

Closed

</td><td>

The customer accepts the proposed solution or the agent selects the **Close case** action. The case can also be auto closed if there is no response from the customer within a specified about of time.The case record is read-only when the state is Closed.

</td></tr><tr><td>

Cancelled

</td><td>

A case that has been cancelled by a user.

</td></tr></tbody>
</table>## State flows

State flows are customized transitions from one state to another. State flows include triggers and can be configured to perform different actions during transitions to specific states.

<table id="table_vrn_vxf_n1c"><thead><tr><th>

From state

</th><th>

To state

</th><th>

Trigger

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

New

</td><td>

Agent actions:-   **Submit Case**
-   **Finish case intake**

</td></tr><tr><td>

New

</td><td>

Work in Progress

</td><td>

Agent actions:-   **Assign to me**: assigns the case to the logged in user.
-   **Accept**: AWA - assigns the case to the user who accepts.

</td></tr><tr><td>

New / Work in Progress

</td><td>

Awaiting Info

</td><td>

Selecting the **Request Information** action changes the state from New or Work in Progress to Awaiting Info.

</td></tr><tr><td>

Awaiting Info

</td><td>

Work in Progress

</td><td>

The agent selects **Information Received** or the customer updates the case comments.

</td></tr><tr><td>

Work in Progress

</td><td>

Solution Proposed

</td><td>

The agent selects **Propose Solution**.

</td></tr><tr><td>

Solution Proposed

</td><td>

Work in Progress

</td><td>

The agent or customer selects **Reject solution**.

</td></tr><tr><td>

Solution Proposed

</td><td>

Closed

</td><td>

The agent or customer selects **Accept Solution** or the case is auto closed.

</td></tr></tbody>
</table>## List views

The Technology Product Support Case application includes list views for CSM/FSM Configurable Workspace and for Core UI. These views are displayed in the application navigator.

<table id="table_yph_xks_y1c"><thead><tr><th>

User interface

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSM/FSM Configurable Workspace

</td><td>

Technology Product Support Cases-   Assigned to me
-   Work in Progress
-   Solution Proposed
-   Closed
-   Unassigned
-   Escalated
-   All

</td></tr><tr><td>

Core UI

</td><td>

Technology Product Support Cases-   Draft
-   Work in Progress
-   Solution Proposed
-   Unassigned
-   Escalated
-   All

</td></tr></tbody>
</table>## Special handling notes

Special handling notes bring important information to an agent's attention. You can configure special handling notes to appear based on one or more conditions, such as a specific account, contact, or product.

The Technology Product Support Case application includes a configuration for special handling notes. Navigate to **Special Handling Notes** &gt; **Configuration** to view the configuration for the Tech Product Support Case table \[sn\_tech\_product\_support\_case\]. This configuration includes the following related fields:

-   Account
-   Contact
-   Product
-   Install Base
-   Assigned to

Users can create special handling notes by navigating to **Special Handling Notes** &gt; **Special Handling Notes** and selecting **New**. For more information, see the following topics:

-   Special handling notes
-   Configure special handling notes
-   Create a special handling note

## Service definitions

The Technology Product Support Case application includes the following service definitions. These definitions belong to the Technology Support category and are associated with the Create a Technology Product Case catalog item.

-   Question
-   Service Request
-   Something is Broken
-   Performance Issue

For more information, see Service definitions and Service definition categories.

## Email notifications and email templates

Email notifications are sent to the contact and, in some cases, to users on the case watch list for the following actions. The system uses email templates to create these notifications.

<table id="table_qsj_n1k_y1c"><thead><tr><th>

Notification

</th><th>

Action

</th><th>

Email template

</th></tr></thead><tbody><tr><td>

Tech Case opened for customer

</td><td>

An agent opens a case for a contact.The notification is sent to the contact and to users in the watch list.

</td><td>

case.opened.for.customer

</td></tr><tr><td>

Tech Case commented for customer

</td><td>

An agent adds a customer-visible comment to a case.The notification is sent to the contact and to users in the watch list.

</td><td>

case.commented.for.customer

</td></tr><tr><td>

Tech Case awaiting info for Customer

</td><td>

An agent requests more information for a case from the contact.The notification is sent to the contact and to users in the watch list.

</td><td>

tech.case.awaiting.info

</td></tr><tr><td>

Tech Case closed for customer

</td><td>

An agent closes a case.The notification is sent to the contact and to users in the watch list.

</td><td>

case.closed.for.customer

</td></tr><tr><td>

Tech Case cancelled for customer

</td><td>

An agent cancels a case.The notification is sent to the contact and to users in the watch list.

</td><td>

tech.case.cancelled

</td></tr><tr><td>

Tech Case solution accepted for customer

</td><td>

An agent accepts a solution on behalf of the customer.The notification is sent to the contact.

</td><td>

tech.case.solution.accepted.for.customer

</td></tr><tr><td>

Tech Case solution rejected for customer

</td><td>

An agent rejects a solution on behalf of the customer.The notification is sent to the contact.

</td><td>

tech.case.solution.rejected.for.customer

</td></tr><tr><td>

Tech Case resolved for customer

</td><td>

An agent resolves a case for a customer.The notification is sent to the contact.

</td><td>

case.resolved.for.customer

</td></tr><tr><td>

Tech Case resolved - customer\_watchlist

</td><td>

An agent resolves a case for a customer.The notification is sent to the users in the watch list.

</td><td>

case.resolved.for.customer.watchlist

</td></tr></tbody>
</table>To access a list of email notifications, navigate to **System Notification** &gt; **Email** &gt; **Notifications**.

To access a list of email templates, navigate to **System Notification** &gt; **Email** &gt; **Templates**.

## Provider notifications

Provider notifications for agents are sent on the following updates to technology product support cases. Notifications appear in the bell icon in the CSM Configurable Workspace header. To access a list of provider notifications, navigate to **System Notification** &gt; **Provider** &gt; **Notifications**.

|Case update|Notification|
|-----------|------------|
|A case is assigned to an agent|Tech Case assigned to notification|
|Case comments or work notes are updated|Tech Case comments/notes added|
|The proposed solution is accepted or rejected|Tech Case solution accepted/rejected|
|The case is cancelled|Tech Case cancelled notification|

## SLA definitions

The Technology Product Support Case application includes the following SLA definitions.

<table id="table_xsy_fcl_y1c"><thead><tr><th>

SLA type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

First Response Time - P2 \(8 Hours\)First Response Time - P3-P4 \(2 Days\)

</td><td>

The first response time is the time between the customer submitting a case and receiving a response.The first response time is defined by case priority.

-   P2 cases: response time is 8 business hours.
-   P3 and P4 cases: response time is 2 business days.

This SLA is fulfilled when the customer receives a response in one of the following ways:

-   The agent updates the **First response** field.
-   The agent posts a comment in the activity stream.
-   The agent uses the **Compose Email** action to send an email.

For the playbook experience, this SLA is fulfilled when the initial response is posted in the activity stream.

</td></tr><tr><td>

Ongoing Response Time - P2 \(8 Hours\)Ongoing Response Time - P3-P4 \(2 Days\)

</td><td>

The ongoing response time begins after the first response time SLA is fulfilled and continues until the agent sends the next update to the customer.The ongoing response time SLA is defined by case priority:

-   P2: response time is 8 business hours.
-   P3 and P4: response time is 2 business days.

ThIs SLA is fulfilled when the agent updates the additional comments in the activity stream. Once completed, the ongoing response SLA is reset and the default ongoing response is applied again.

This SLA is paused when the case is in the Awaiting Info state and is restarted when the customer responds to the request for information.

This SLA is stopped when the agent proposes a solution for a case. If the customer rejects the solution and the case moves back to work in progress, a new ORT SLA instance is started.

</td></tr><tr><td>

Case Resolution - P2 \(14 days\)Case Resolution - P3-P4 \(28 days\)

</td><td>

The resolution time is the maximum amount of time in which a customer can expect a solution to be provided. This is the time between the customer submitting a case and accepting a solution \(or a case being automatically closed\).The case resolution SLA is defined by case priority:

-   P2: resolution time 14 days.
-   P3 and P4: resolution time is 28 days.

This SLA is paused when the case is in the Awaiting Info state and is restarted when the customer responds to the request for information.

This SLA is stopped when the agent proposes a solution for a case. If the customer rejects the solution and the case moves back to work in progress, this SLA resumes.

</td></tr></tbody>
</table>## Record producer

The Technology Product Support Case application includes a record producer that customers can use to create cases from the Customer Service Portal. The **Create a Technology Product Case** record producer is available for users with the following roles:

-   sn\_tech\_support.customer
-   sn\_tech\_support.customer\_admin

To create a case from the Customer Service Portal using this record producer:

1.  Select **Requests** &gt; **Request Something**.
2.  Select the **Support** category.
3.  Select the **Create a Technology Product Case** catalog item.
4.  Fill in the fields on the record producer. For field definitions, see the [Create a Technology Product Case record producer fields table](tech-product-support-case-type.md#table_egg_1ky_1bc) below.
5.  Select **Submit**.

The **Create a Technology Product Case** record producer includes the following fields.

<table id="table_egg_1ky_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issue Type

</td><td>

Select the type of issue for the case:-   Something is broken
-   Performance issue
-   Service request
-   Question

</td></tr><tr><td>

Account

</td><td>

Auto filled with the account of the logged-in user.

</td></tr><tr><td>

Contact

</td><td>

Auto filled with the name of the logged-in user.

</td></tr><tr><td>

Affected Instances

</td><td>

Add the affected instances to this list.

</td></tr><tr><td>

Sold Product

</td><td>

Select a product from the list of available products. This list includes the sold products for the logged-in user.

</td></tr><tr><td>

Product Component

</td><td>

Select a product component from the list of available product components.

</td></tr><tr><td>

Short Description

</td><td>

Provide a brief description of the issue.

</td></tr><tr><td>

Description of the issue

</td><td>

Provide a more detailed description of the issue.

</td></tr><tr><td>

Describe the Business Impact

</td><td>

Describe the impact that this issue is having on your business.

</td></tr><tr><td>

Steps to reproduce

</td><td>

Add the steps to reproduce the issue.

</td></tr><tr><td>

Contact Timezone

</td><td>

Displays the timezone of the user in the **Contact** field.

</td></tr><tr><td>

Add attachments

</td><td>

Add any attachments to the case.

</td></tr></tbody>
</table>## Case action status

The case action status feature enables agents to easily identify cases that need attention. Visual indicators in the **Action status** column on case lists highlight case status.

-   A blue indicator highlights cases that need attention, such as cases that have been updated by customers or internal users and are waiting for input or review.
-   A red indicator highlights cases that are blocked, such as cases that have open related task records or are waiting for customer feedback.

In addition to the colored indicators, the **Action status** column also displays a brief status message, such as Needs Attention.

When a case is in the Awaiting Info state and the customer, or a customer contact who has access to the case, responds to the request for information:

-   The **Action status** field is updated to Customer Responded.
-   The **Needs attention** field is enabled.

For more information, see the following topics:

-   Administering case action status
-   Case action status \(CSM Configurable Workspace\)

## Field indicators and highlights

The Technology Product Support case type uses field indicators and field highlights to indicate information about cases. These indicators and highlights appear on columns that are displayed in the list view.

<table id="table_pcn_pzd_y1c"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Priority

</td><td>

The **Priority** field uses the following colors to highlight the case priority:

-   Red: 1 - Critical
-   Orange: 2 - High
-   Purple: 3 - Moderate
-   Green: 4 - Low

</td></tr><tr><td>

Action status

</td><td>

The **Action status** field uses the following colors to highlight the following actions:

-   Red: Blocked internally:
-   Blue: Needs attention

</td></tr><tr><td>

State

</td><td>

The **State** field uses the following colors to highlight the case state:

-   Draft: Yellow
-   New: Green
-   Work in progress: Purple
-   Closed: Light green
-   Solution proposed: Gray

</td></tr><tr><td>

Escalated cases and accounts

</td><td>

Field indicators and field highlights appear on the **Short description** field for escalated cases and on the **Name** field for escalated accounts.

-   Red: High severity
-   Orange: Medium severity

 For more information, see Administering case and account escalation.

</td></tr></tbody>
</table>## Automatically close technology product support cases

The Auto Close Resolved Cases feature is available with the technology product support case type. Cases in the Resolved state can be closed automatically if customers do not take any action.

**Note:** This feature is active by default.

A case can remain in the Resolved state for 10 days before it is automatically closed. System administrators can change this default value in the **Auto Close Resolved Cases** Flow Designer flow.

Customers receive the following notifications before a case is automatically closed:

-   First notification: sent after 3 days
-   Second notification: sent after 5 days
-   Third notification: sent after 8 days

For more information, see Automatically close customer service cases.

**Parent Topic:**[Exploring Technology Product Support Case](tech-product-support-case-app.md)

