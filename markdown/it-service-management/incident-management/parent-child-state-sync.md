---
title: Synchronization between a parent and a child incident
description: The parent and the child incidents are synchronized such that the state of a child incident changes depending on the state of the parent incident.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Synchronization between a parent and a child incident

The parent and the child incidents are synchronized such that the state of a child incident changes depending on the state of the parent incident.

<table id="table_iqz_kmm_qbb"><thead><tr><th>

Parent State

</th><th>

On Hold Reason \(Parent\)

</th><th>

Child State

</th><th>

On Hold Reason \(Child\)

</th></tr></thead><tbody><tr><td>

In Progress

</td><td>

NA

</td><td>

In Progress

</td><td>

NA

</td></tr><tr><td>

On Hold

</td><td>

Awaiting Change/Awaiting Problem/Awaiting Vendor

</td><td>

Same as parent

</td><td>

Same as parent

</td></tr><tr><td>

On Hold

</td><td>

Awaiting caller

</td><td>

Not updated

</td><td>

Not updated

</td></tr><tr><td>

Resolved

</td><td>

NA

</td><td>

Resolved.The Activity log in the child incident form is updated with the resolution notes copied from the parent Incident.

</td><td>

NA

</td></tr><tr><td>

Closed

</td><td>

NA

</td><td>

Not closed.Child incidents must always be closed by the caller or by the system based on the auto-closure property.

</td><td>

NA

</td></tr><tr><td>

Canceled

</td><td>

NA

</td><td>

NA

</td><td>

NA

</td></tr></tbody>
</table>**Note:**

When an incident has a child incident, the following actions take place:

-   If an ITIL user reopens the parent incident, then the parent incident as well as the child incident reopens. Both the parent and the child incident state is set to **In Progress**.
-   If an ESS user reopens the parent incident, the parent incident state is set to **In Progress** but the child incident is not reopened.

