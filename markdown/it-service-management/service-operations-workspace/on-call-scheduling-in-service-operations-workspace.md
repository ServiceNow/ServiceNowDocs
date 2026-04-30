---
title: On-call Scheduling in Service Operations Workspace
description: On-Call Scheduling ensures that dedicated support team members are always available to resolve issues as they arise. You can set up on-call schedules, roster rotations, and escalation policies, escalate notifications for a group, and determine the current contact for an escalation.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# On-call Scheduling in Service Operations Workspace

On-Call Scheduling ensures that dedicated support team members are always available to resolve issues as they arise. You can set up on-call schedules, roster rotations, and escalation policies, escalate notifications for a group, and determine the current contact for an escalation.

You can access your shifts and schedules within Service Operations Workspace using **Schedules** options.

Managers can also use the **Teams** menu to perform all the administrative tasks.

See [On-Call Scheduling in Service Operations Workspace](../concept/on-call-scheduling-in-sow.md) for more details.

## On-Call Scheduling in Service Operations Workspace workflow

The various members of an organisation use On-Call Scheduling to work together. See a sample end-to-end workflow:![On-call scheduling workflow](../../../administer/on-call-scheduling/image/Oncall_workflow.png)

1.  Shift admin creates shift and group templates.
2.  Shift admin assigns role and configures escalation trigger rules. See [Roles in Service Operations Workspace for ITSM](../reference/roles-in-sow.md) and [Assigning On-Call Scheduling roles](../../../administer/on-call-scheduling/concept/roles-assigning-oncall.md)
3.  The shift manager creates a shift and add or delete members to the shift.
4.  Shift manager designs the entire escalation process for the new shift.
5.  Roster member views their on-call schedules and find out who the other members on their shift are.
6.  Roster member can specify their availability and preferred contact methods from the methods set up by Shift admin.
7.  Roster members can submit a time-off request and refer another member of the group to cover the shift.
8.  Roster members views the roster and escalation details for a shift.
9.  Roster members view on-call reports and receive reminders.
10. The shift manager approves or rejects the time-off requests.
11. Shift manager reviews the on-call schedules for their groups for any gaps and time-off requests.
12. Shift manager provides, replace, or delete coverage and time-off requests.
13. Roster members receive on-call escalation notifications to acknowledge tasks or conference requests.
14. Shift manager views escalation, group, and performance reports of their on-call teams.

**Note:** To view version compatibility matrix, view the latest release notes.

## On-Call Scheduling benefits

<table id="table_zxt_h3r_fyb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Create a new shift, assign members to the shift, set the shift preferences like rotations and responder levels.

</td><td>

[Create and edit shift in Service Operations Workspace](../concept/create-a-schedule-in-sow.md)

</td><td>

itil, rota\_manager \(Shift Manager\)

</td></tr><tr><td>

Manage your shift by accepting or rejecting time-off requests. Resolve gaps and conflicts by providing coverage. Assign extra-time to the members to the shift.

</td><td>

[Manage shifts in service operation workspace](../concept/manage-shifts-in-service-operation-workspace.md)

</td><td>

itil, rota\_manager \(Shift Manager\), rota\_admin

</td></tr><tr><td>

Create your own escalation policies and path. On-Call Scheduling allows you to create an escalation trigger rule using the templates available, based on your requirement.

</td><td>

[Escalation triggers and policies](../concept/work-on-escalation-trigger-rules-and-policies-in-sow.md)

</td><td>

itil, rota\_manager \(Shift Manager\), rota\_admin, admin

</td></tr><tr><td>

Create and edit Notification preferences for an entire team.

</td><td>

[Edit On-call team preference using Teams menu](../concept/oncall-team-preference-tab-in-teams.md)

</td><td>

itil, rota\_manager \(Shift Manager\), rota\_admin

</td></tr><tr><td>

Use any one of the multiple channels such as Slack, Microsoft Teams, mobile push messages, SMS, and voice messages to set as the preferred contact method for receiving notifications.

</td><td>

[Edit delivery channel](../concept/work-on-a-notification-preference-rule-in-sow.md)To configure delivery channels, see:

-   For Slack: [Setting up Slack as a contact method](../../../administer/on-call-scheduling/reference/slack-setup-oncall.md)
-   For SMS and voice message: [Setting up SMS and voice messaging as contact methods](../../../administer/user-administration/concept/c_UseNotifyWithOnCallScheduling.md)
-   For teams: Microsoft Teams
-   For mobile push notifications: [Set up mobile push as a contact method for an on-call escalation](../../../administer/on-call-scheduling/task/set-up-mobile-push-oncall.md)

</td><td>

rota\_admin, admin

</td></tr></tbody>
</table>**Note:** For more details on user roles, see [Assigning On-Call Scheduling roles](../../../administer/on-call-scheduling/concept/roles-assigning-oncall.md).

**Parent Topic:**[Configuring Service Operations Workspace for ITSM](../concept/configure-sow.md)

**Related topics**  


[Admin Center in Service Operations Workspace for ITSM](../concept/admin-center-sow.md)

[Customize the Service Operations Workspace for ITSM landing page](../concept/customize-sow-landing-page.md)

[Assign the service desk agent role to the user in Service Operations Workspace](assign-service-desk-agent-role-sow.md)

[Reorder the navigation pane modules in Service Operations Workspace for ITSM](reorder-left-navigation-pane-modules.md)

[Configure a record page tab in Service Operations Workspace](configure-record-page-tab.md)

[Configure a task record form in Service Operations Workspace](configure-form-layout-task.md)

[Configure the inbox in Service Operations Workspace](configure-inbox-in-sow.md)

[AI Search in Service Operations Workspace for ITSM](../concept/ai-search-sow.md)

[Configure Standard Record Page in Service Operations Workspace](../concept/srp-service-operations-workspace.md)

[Configure the SOW list page](incident-list-page.md)

[Define and customize activity stream tags](define-customize-activity-stream-tags.md)

[Configure the Assign or Resolve dialog box for an incident or change request in Service Operations Workspace](configure-assign-resolve-modals-incident.md)

[Customize the incident record page](../concept/customize-the-incident-record-page.md#)

[Setting up Investigation Framework in Service Operations Workspace](../concept/set-up-investigate.md)

[Create a task type for problem or change in Service Operations Workspace](create-task-type-sow.md)

[Configuring Recommendation Framework in Service Operations Workspace](../concept/set-up-recommendation-framework-sow.md)

[Configure the display of requester related records in an interaction](configure-order-related-records-interaction.md)

[Configure the experts On-call panel](customize-experts-on-call-tab.md)

[Setting up Service Desk assisted Password Reset in Service Operations Workspace](../concept/setup-password-reset-sow.md)

[Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](integrate-cti-sow.md)

[Configure the task record information in the MS Teams Import tab](configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](../concept/configure-interaction-management-sow.md)

