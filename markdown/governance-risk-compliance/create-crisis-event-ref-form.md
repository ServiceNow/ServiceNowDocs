---
title: Create Crisis Event form
description: Use the Create Crisis Event form in BCM UIB Workspace to add details about a crisis event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-crisis-event-ref-form.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Start a crisis event, Structured workflows for Crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create Crisis Event form

Use the Create Crisis Event form in BCM UIB Workspace to add details about a crisis event.

## Create Crisis Event form

For description of the field values, see the table.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Details tab

</td></tr><tr><td>

Short description

</td><td>

Brief description about the crisis event.

</td></tr><tr><td>

State

</td><td>

State of the event. Defaults to the **Pending** state.

</td></tr><tr><td>

Event type

</td><td>

Type of the event. For a crisis event, the event type is **Actual**.

</td></tr><tr><td>

Description

</td><td>

Description of the crisis event.

</td></tr><tr><td>

Impact

</td><td>

Measure of the business criticality of the affected service. Available options are:-   **1 - High**
-   **2 - Medium**
-   **3 - Low**

</td></tr><tr><td>

Priority

</td><td>

Sequence in which an Incident or Problem needs to be resolved, based on impact and urgency. Available options are:-   **1 - Critical**
-   **2 - High**
-   **3 - Moderate**
-   **4 - Low**
-   **5 - Planning**
-   **None**

</td></tr><tr><td>

Level

</td><td>

Escalation level of the crisis event: **1-Site**, **2-Regional**, **3-Corporate**, or **4-Global**. Defaults to **-- None --** until selected manually. Read-only for the BCM viewer role.

</td></tr><tr><td>

Assigned to

</td><td>

User or users from the Assignment group. If the **Assignment group** field is empty, then select any user.

</td></tr><tr><td>

Description

</td><td>

Description of the event.

</td></tr><tr><td class="sub-head" colspan="2">

Plans

</td></tr><tr><td>

Plans associated with the event

</td><td>

Details of the plans such as Number, Short description, State, Actual time taken, Total effort, Type, and Parent.

</td></tr><tr><td class="sub-head" colspan="2">

Action items

</td></tr><tr><td>

Action items associated with the event

</td><td>

Ad-hoc action items of task and assessment type, associated with the event and their details such as Number, Short description, State, Assigned to, and Due date.

</td></tr><tr><td class="sub-head" colspan="2">

Issues

</td></tr><tr><td>

Issues

</td><td>

GRC issues that can be created or added from an event.

</td></tr><tr><td class="sub-head" colspan="2">

Similar tasks groups

</td></tr><tr><td>

Group of similar tasks associated with the event

</td><td>

Group of similar tasks, their names, and original tasks associated with the event.

</td></tr><tr><td class="sub-head" colspan="2">

Collaborations

</td></tr><tr><td>

Collaborations

</td><td>

Collaboration threads related to an event. Includes action items, email notifications and email attachments. For more information, see[Creating collaborations in exercises and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/creating-collaboration-threads-in-crisis.md).

</td></tr><tr><td class="sub-head" colspan="2">

Event tasks

</td></tr><tr><td>

Event tasks associated with the event

</td><td>

Information on the event tasks such as Number, Short description, State, Impacted assets, Assigned to, Dependencies, Actual start, Actual end, Related activated plan, Similar tasks group, Phase.

</td></tr></tbody>
</table>**Parent Topic:**[Start a crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/start-crisis-event-in-uib-ws.md)

