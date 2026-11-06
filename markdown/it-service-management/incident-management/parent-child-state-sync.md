---
title: Synchronizing parent and child incidents
description: The state of a child incident follows the state of its parent incident for most incident states, which keeps related incidents aligned without manual updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/parent-child-state-sync.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Synchronizing parent and child incidents

The state of a child incident follows the state of its parent incident for most incident states, which keeps related incidents aligned without manual updates.

<table id="table_iqz_kmm_qbb"><thead><tr><th>

Parent state

</th><th>

On hold reason \(parent\)

</th><th>

Child state

</th><th>

On hold reason \(child\)

</th></tr></thead><tbody><tr><td>

In Progress

</td><td>

N/A

</td><td>

In Progress

</td><td>

N/A

</td></tr><tr><td>

On Hold

</td><td>

Awaiting Change, Awaiting Problem, or Awaiting Vendor

</td><td>

Same as parent

</td><td>

Same as parent

</td></tr><tr><td>

On Hold

</td><td>

Awaiting Caller

</td><td>

Not updated

</td><td>

Not updated

</td></tr><tr><td>

Resolved

</td><td>

N/A

</td><td>

Resolved.The Activity log in the child incident form is updated with the resolution notes copied from the parent incident.

</td><td>

N/A

</td></tr><tr><td>

Closed

</td><td>

N/A

</td><td>

Not closed.Child incidents must be closed by the caller or by the system based on the auto-closure property.

</td><td>

N/A

</td></tr><tr><td>

Canceled

</td><td>

N/A

</td><td>

N/A

</td><td>

N/A

</td></tr></tbody>
</table>**Note:**

This table applies only to standard incident life cycle states. When a parent incident is proposed or accepted as a major incident, the states of any associated child incidents do not change automatically. For more information, see [Managing major incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-management.md).

When an incident has a child incident, the following actions take place:

-   If an ITIL user reopens the parent incident, both the parent and child incidents reopen. Both the parent and the child incident state is set to **In Progress**.
-   If an employee self-service \(ESS\) user reopens the parent incident, the parent incident state is set to **In Progress** but the child incident is not reopened.

