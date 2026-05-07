---
title: Create an incident in Service Operations Workspace
description: Track the investigation, possible solutions, and resolution of a problem for a customer.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Incident Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Create an incident in Service Operations Workspace

Track the investigation, possible solutions, and resolution of a problem for a customer.

## Before you begin

Role required: itil or admin

## Procedure

1.  Perform one of the following actions to start creating an incident.

<table id="choicetable_vrd_rrt_tsb"><thead><tr><th align="left" id="d234135e52">

Option

</th><th align="left" id="d234135e55">

Description

</th></tr></thead><tbody><tr><td id="d234135e61">

**From the List menu**

</td><td>

1.  From the primary navigation, click the list icon \(![List icon](../../itsm-manager-workspace/image/lists_icon.png)\).
2.  Click the add icon \(![add icon](../image/add-icon.png)\) next to the **List** tab.
3.  Click **New Incident**.


</td></tr><tr><td id="d234135e100">

**From an incident list**

</td><td>

1.  Navigate to a list of incidents.

**Note:** Following lists are available for incidents:

    -   Assigned to me
    -   Unassigned
    -   Open
    -   Resolved
    -   All
2.  Click **New**.


</td></tr><tr><td id="d234135e140">

**From an interaction**

</td><td>

1.  Open an interaction.
2.  From the record page, select **Create incident**.


</td></tr></tbody>
</table>2.  On the form, fill the fields in the **Details** tab.

<table id="table_un2_dyl_n3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Incident

</td></tr><tr><td>

Short description

</td><td>

Brief description of the incident.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation of the incident.

</td></tr><tr><td>

Number

</td><td>

Auto-generated unique number to identify the incident record.

</td></tr><tr><td>

Caller

</td><td>

User who contacted you with an issue. Begin typing the first name of the caller to select from a list of matching names, or look up and select the user.

</td></tr><tr><td>

Location

</td><td>

Location of the caller.

</td></tr><tr><td>

Channel

</td><td>

Mode of communication taken by the user to create the incident.

</td></tr><tr><td>

State

</td><td>

Different states through which the incident proceeds during its life cycle.

</td></tr><tr><td>

Impact

</td><td>

The effect of an incident, problem, or change on the business processes.

</td></tr><tr><td>

Urgency

</td><td>

How long the resolution can be delayed until an incident, problem, or change has a significant business impact.

</td></tr><tr><td>

Priority

</td><td>

How quickly the service desk should address the task. Priority is based on impact and urgency.

</td></tr><tr><td class="sub-head" colspan="2">

Impact

</td></tr><tr><td>

Service

</td><td>

Business service that is affected.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item that is affected.

</td></tr><tr><td>

Service Offering

</td><td>

Consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. Service offering enables you to receive different features and their levels of performance for a given service.

</td></tr><tr><td>

Business impact

</td><td>

Impact of the incident.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group to work on this incident. If you do not provide a value, the incident is automatically assigned based on assignment rules.

</td></tr><tr><td>

Assigned to

</td><td>

The user to work on this incident. **Note:** If the **Assignment group** changes, the **Assigned to** field is cleared.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

More information about the issue as needed. All users who can view incidents can also see additional comments.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the incident or steps taken to resolve it, if applicable.

</td></tr><tr><td class="sub-head" colspan="2">

Related Records

</td></tr><tr><td>

Parent Incident

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
</table>3.  Click **Save**.


**Parent Topic:**[Incident Management in Service Operations Workspace](../concept/incident-sow.md)

**Related topics**  


[View and update incident information on the Overview tab in SOW](view-update-inc-overview-tab.md)

[Viewing incident record information using the Contextual side panel](../concept/view-inc-record-info-contextual-sidepanel.md)

[Work on an incident list page in Service Operations Workspace](work-incident-list-page-sow.md)

[Work on an incident record in Service Operations Workspace](work-on-incident-sow.md)

[Remedial actions using Playbook](../concept/remedial-actions-playbook.md)

[Close resolved incident](close-resolved-incident-sow.md)

[Reopen an incident in Service Operations Workspace](reopen-incident-sow.md)

[Incident Management in Service Operations Workspace reference](../concept/sow-im-reference.md)

