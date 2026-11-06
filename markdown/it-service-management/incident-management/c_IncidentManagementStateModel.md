---
title: Incident life cycle
description: Incident Management manages incidents through a defined set of states, from creation to closure, so you can track where each incident is in its life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/c\_IncidentManagementStateModel.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Incident Management, IT Service Management]
---

# Incident life cycle

Incident Management manages incidents through a defined set of states, from creation to closure, so you can track where each incident is in its life cycle.

Each incident moves through a set of states in the Incident Management process, as shown in the following diagram:

\[Omitted image "IM\_StateModel.png"\] Alt text: Incident state flow diagram

**Note:**

The state names in the diagram correspond to the states described in the following table.

<table id="table_t51_21c_b5"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Incident is logged but not yet investigated.

</td></tr><tr><td>

In Progress

</td><td>

Incident is assigned and is being investigated.

</td></tr><tr><td>

On Hold

</td><td>

The responsibility for the incident shifts temporarily to another entity to provide further information, evidence, or a resolution. When you select the **On Hold** option, the following **On hold reason** list appears. -   Awaiting Caller
-   Awaiting Change
-   Awaiting Problem
-   Awaiting Vendor

If the **On hold reason** is **Awaiting Caller**, the **Additional comments** field becomes required.

**Note:** If the caller updates the incident, the **On hold reason** field is cleared and the state of the incident is changed to **In Progress**. An email notification is sent to the user whose name is mentioned in the **Assigned to** field and to the users in the **Watch list**. An incident can be placed in the **On Hold** state one or more times before being closed.

</td></tr><tr><td>

Resolved

</td><td>

A satisfactory fix is provided for the incident to help keep it from recurring.

</td></tr><tr><td>

Closed

</td><td>

Incident is marked **Closed** after it is in the **Resolved** state for a specific duration and it is confirmed that the incident is satisfactorily resolved.

</td></tr><tr><td>

Canceled

</td><td>

Incident is triaged but found to be a duplicate incident, an unnecessary incident, or not an incident at all.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-management-process.md)

