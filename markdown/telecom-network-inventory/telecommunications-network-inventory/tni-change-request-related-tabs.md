---
title: Change request related tabs
description: The related tabs in the Change Request form display related records that dynamically change based on the context of the change request.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Change request related tabs

The related tabs in the Change Request form display related records that dynamically change based on the context of the change request.

<table id="table_tni_change_request_field"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Affected CIs

</td><td>

List of configuration items \(CI\). These items \(from the CMDB\) are affected by the change request. You can associate multiple, affected CIs with a change.

 **Note:**

-   The **Affected CIs** tab of the Change Request form lists all CIs that are created through the change tasks of that change request. This tab also lists all the affected CIs of the change tasks.
-   If a CI in the affected CIs list of a change task is manually \(or through an API\) changed to another CI, the changes are also updated in the affected CI list of the corresponding change request.
-   If a CI in the affected CI list of a change task is manually \(or through an API\) deleted, the same CI is deleted in the affected CI list of the corresponding change request.

</td></tr><tr><td>

Impacted Services/CIs

</td><td>

List of CIs, such as business services or from other CI classes. These items are impacted by the affected CIs in the change request. You can associate multiple, impacted CIs with a change.

</td></tr><tr><td>

Approvers

</td><td>

List of approvers. These items are automatically generated from the workflow. You can also view the group of approvers who are assigned to the task.

</td></tr><tr><td>

Change Tasks

</td><td>

List of change tasks. These items are created from a workflow. The default workflow generates tasks in the Implementation state. You can also create a new change task. The **Planned start date** and **Planned end date** in the task must fall within the planned start and end dates that are specified in the change request.

</td></tr><tr><td>



</td><td>



</td></tr><tr><td>

Problems

</td><td>

List of problem statements. If the change was generated from a problem, this list is generated automatically.

</td></tr><tr><td>

Incidents Fixed By Change

</td><td>

Incidents that require a resolution for the change.

</td></tr><tr><td>

Incidents Caused By Change

</td><td>

List of incidents caused by the implementation of the change.

</td></tr><tr><td>

Task SLAs

</td><td>

List of Task SLA records for the SLAs that are attached to the particular change tasks.

</td></tr><tr><td>

Outages

</td><td>

List of CI unavailability or outages. If there is an actual down time for any of the CI items, the outage information is listed.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md)

