---
title: Contractor Management components
description: The plugin and roles for the Contractor Management application.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Contractor Management components

The plugin and roles for the Contractor Management application.

Contractor Management adds the Outsourced Field Service menu to the application navigator and the following modules:

-   **My Outsourced Service providers**: Use this module to view the list of onboarded contractor companies and its external workforce managed by the logged-in user.
-   **Outsourced Service Providers**: Use this module to view the list of all the contractor companies, onboard contractor companies and their external workforce, and create groups.
-   **Field Service**: Use this module to view a list of activities associated with Field Service Management and managed by an internal contractor manager. This list includes the work order tasks assigned to external agents, personal stockrooms of external agents and managers, stockrooms based on the associated external groups, and groups created for contractor companies.

## Roles

Contractor Management adds the following roles:

<table id="table_gzx_lz1_zlb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Service Contractor Management Internal Manager\[wm\_contractor\_manager\_int\]

</td><td>

Manager of the organization that outsources its work order tasks to the contractor companies.

</td></tr><tr><td>

Field Service Contractor Management External Agent\[wm\_ext\_agent\]

</td><td>

Employee of the contractor company who works on the assigned tasks.

</td></tr><tr><td>

Field Service Contractor Management External Manager\[wm\_ext\_manager\]

</td><td>

Manager of the contractor company to whom tasks are outsourced and who is responsible for reviewing and reassigning tasks to agents.

</td></tr></tbody>
</table>## Task Filters

Contractor Management adds the following task filters:

<table id="table_fll_gv4_zbc"><thead><tr><th>

Task Filter

</th><th>

Conditions

</th><th>

Criterion

</th><th>

Function

</th></tr></thead><tbody><tr><td>

Contractor tasksEnsure that the Field Service Contractor Management plugin is active. For more information, see [Activate Field Service Contractor Management](../task/activate-contractor-management-plugin.md).

Demo data is provided with this plugin.

</td><td>

-   State is pending dispatch
-   Location is populated

</td><td>

Distance between task and contractorsMatching skills of contractors

</td><td>

Only eligible for external contractor assignment.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](../reference/components-inst-additional-plugin.md)

