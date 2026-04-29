---
title: Roles installed with Field Service Management
description: Roles are added with Field Service Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Components installed, Reference, Field Service Management]
---

# Roles installed with Field Service Management

Roles are added with Field Service Management.

<table id="table_roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Field Service Management Administrator\[wm\_admin\]

</td><td>

Manages data related to field service management. Field service management administrators also can:-   Control and override all information in the Field Service Management application.
-   Delete work orders and tasks.
-   Create tasks using the Clone Task feature.
-   Create, edit, and delete work order models and work task models.
-   Create, edit, and delete incidentals.
-   View expense lines.
-   View certain fields in non-subscription-based contracts.
-   Create questionnaires.
-   Book an appointment.
-   Create, read, upload, and delete ACLs for Custom Map Screen and Custom Map Provider.
-   Review quality management configuration, auto close configuration, and monitor the quality dashboard.
-   Manage the Acceptance due date, and work management order fields.
-   Migrate UI actions to questionnaires.

</td><td>

-   wm\_approver\_user
-   fsm\_skill\_admin
-   dynamic\_scheduling\_admin
-   wm\_agent
-   skill\_model\_admin
-   skill\_admin
-   territory\_admin
-   sn\_apptmnt\_booking.appointment\_booking\_admin
-   plan\_maint\_admin
-   wm\_dispatcher
-   questionnaire\_admin
-   catalog\_admin
-   wm\_qualifier
-   knowledge\_manager
-   template\_admin

</td></tr><tr><td>

Field Service Management Agent\[wm\_agent\]

</td><td>

Manages actual task time and performs work on site. Agents also can:-   Accept or reject tasks assigned to them.
-   Add parts requirements.
-   Source parts.
-   Create tasks using the Clone Task feature.
-   Add work notes to work orders and work order tasks.
-   Submit questionnaires.
-   Create, edit, and delete incidentals.
-   View expense lines.
-   View certain fields in non-subscription-based contracts.
-   Book an appointment.

 Agents can’t update schedule or task window times or toggle the window control.

</td><td>

-   wm\_basic
-   skill\_user
-   inventory\_user
-   territory\_user
-   document\_management\_user
-   agent\_schedule\_user
-   questionnaire\_user
-   sn\_apptmnt\_booking.appointment\_booking\_manager
-   timecard\_user
-   fsm\_skill\_user

</td></tr><tr><td>

Field Service Management location agent\[wm\_location\_agent\]

</td><td>

-   Accept or reject tasks assigned to them.
-   Create tasks using the clone task feature.
-   Add work notes to work orders and work order tasks.

 **Note:** Work Management and Service Organization plugins are to be installed.

</td><td>

wm\_location\_security

</td></tr><tr><td>

Field Service Management location manager\[wm\_location\_assignment\_manager\]

</td><td>

-   Create, read, and write work orders.
-   Create, read, and write work order tasks.
-   Assign work order tasks to fulfillers within their own service organizations.

 **Note:** Work Management and Service Organization plugins are to be installed.

</td><td>

-   wm\_location\_security
-   fsm\_skill\_user

</td></tr><tr><td>

Field Service Management Approver User\[wm\_approver\_user\]

</td><td>

Responsible for approving work orders before they’re qualified or assigned.

</td><td>

-   approver\_user
-   cmdb\_read

</td></tr><tr><td>

Field Service Management Basic\[wm\_basic\]

</td><td>

Create work orders and follow up on work orders they had created. Common data access shared by all field service roles.

</td><td>

-   task\_activity\_writer
-   skill\_user
-   inventory\_user
-   territory\_user
-   wm\_read
-   service\_fullfiller
-   document\_management\_user
-   fsm\_skill\_user

</td></tr><tr><td>

Field Service Management Dispatcher\[wm\_dispatcher\]

</td><td>

Schedules tasks, adds parts, and assigns tasks to work agents. Dispatchers also can:-   Create tasks.
-   Add part requirements.
-   Source parts.
-   Edit all work order task fields and manage tasks from **Draft** to **Assigned** status.
-   Edit the **Assigned to** field until work starts.
-   Create tasks using the Clone Task feature.
-   Set actual travel time and work start and end times if needed.
-   Add work notes to any field service record.
-   Create, edit, and delete incidentals.
-   View expense lines.
-   View certain fields in non-subscription-based contracts.

</td><td>

-   wm\_basic
-   inventory\_user
-   territory\_user
-   dynamic\_scheduling\_user
-   document\_management\_user
-   sn\_customerservice.customer\_data\_viewer
-   skill\_model\_user
-   sn\_apptmnt\_booking.appointment\_booking\_manager
-   timecard\_user

</td></tr><tr><td>

Field Service Management Initiator\[wm\_initiator\]

</td><td>

Creates work orders and assigns qualification group. Initiators also can:-   Edit work orders that they create that are in the **Draft** state.
-   Add work notes to any field service record.
-   View work order tasks and part requirements.

</td><td>

wm\_basic

</td></tr><tr><td>

Field Service Management Initiator Qualifier\[wm\_initiator\_qualifier\]

</td><td>

Initiator-qualifiers can:-   Create work orders.
-   Create tasks.
-   Add part requirements.
-   Source parts.
-   Assign skills to agents.
-   View incidentals.

</td><td>

-   wm\_initiator
-   wm\_qualifier

</td></tr><tr><td>

Field Service Management Initiator Qualifier Dispatcher\[wm\_initiator\_qualifier\_dispatcher\]

</td><td>

Initiator-qualifier-dispatchers can:-   Create work orders.
-   Create tasks.
-   Add parts requirements.
-   Source parts.
-   Assign skills to agents.
-   Assign work to agents.
-   Manage agent tasks.
-   View incidentals.

</td><td>

-   wm\_initiator
-   wm\_dispatcher
-   wm\_qualifier

</td></tr><tr><td>

Field Service Management Manager\[wm\_manager\]

</td><td>

Field Service Managers can:-   Manage agent skills
-   Manage time cards
-   View and maintain work schedules
-   View and maintain personal events

</td><td>

-   fsm\_skill\_admin
-   wm\_agent
-   timecard\_manager
-   agent\_schedule\_manager

</td></tr><tr><td>

Field Service Management Qualifier\[wm\_qualifier\]

</td><td>

Qualifies work orders and creates work order tasks. Qualifiers also can:-   Edit work orders in the **Qualified** state.
-   Edit work orders in the **Awaiting Qualification** state.
-   Edit tasks that are in the **Draft** state to provide technical details, such as information about CIs involved or parts needed.
-   Create tasks using the Clone Task feature.
-   Change the qualification group.
-   Set the dispatch group.
-   Add part requirements.
-   Source parts
-   Add work notes to any field service record.
-   View incidentals.

</td><td>

-   wm\_basic
-   inventory\_user
-   territory\_user
-   document\_management\_user
-   skill\_model\_user

</td></tr><tr><td>

Field Service Management Read\[wm\_read\]

</td><td>

Capable of reading work orders and work order tasks.

</td><td>

-   sn\_apptmnt\_booking.appointment\_booking\_user
-   cmdb\_read

</td></tr><tr><td>

Field Service Desk Agent \[sn\_fsm\_servicedesk\_agent\]

</td><td>

Allows a user to create a work order, apply a template, and progress the work order.

</td><td>

-   wm\_read
-   sn\_apptmnt\_booking.appointment\_booking\_user

</td></tr><tr><td>

Field Service Management Task Initiator\[wm\_task\_initiator\]

</td><td>

Create, delete, and modify work order tasks and part requirements when both the work order and work order task are in the draft state.

</td><td>

wm\_initiator

</td></tr></tbody>
</table>## Role integration with Customer Service Management

When you enable the Customer Service Management plugin \(com.sn\_customerservice\) along with the Field Service Management plugin \(com.snc.work\_management\) and add specific Customer Service roles to Field Service agents, they can view or create a case and also view additional customer service data. For more information on customer service agent roles, see [Roles installed with Customer Service Management](https://www.servicenow.com/docs/access?context=r_RolesInstalledWithCustomerService&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

<table id="table_abt_gsr_4jb"><thead><tr><th>

Adding this role

</th><th>

Allows agents

</th></tr></thead><tbody><tr><td>

sn\_customerservice.case\_viewer

</td><td>

-   To have read access to cases.
-   To view all fields in a case that a customer service agent \[sn\_customerservice\_agent\] can access.

</td></tr><tr><td>

sn\_customerservice.customer\_data\_viewer

</td><td>

To have read-only access to customer data entities such as:-   Install base items
-   Contracts
-   Entitlements
-   Accounts, contacts, and account team members
-   Assets
-   Consumers
-   Sold product

</td></tr><tr><td>

sn\_customerservice.proxy\_contact

</td><td>

To create a case using a record producer.

</td></tr><tr><td>

wm\_location\_security

</td><td>

View data based on the provider service organization.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Field Service Management](r_InstalledWithFSM.md)

