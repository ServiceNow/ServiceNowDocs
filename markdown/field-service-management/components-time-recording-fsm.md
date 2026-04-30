---
title: Time Recording for Field Service components
description: The plugin and roles for the Time Recording for Field Service.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Time Recording for Field Service components

The plugin and roles for the Time Recording for Field Service.

## Time Recording Plugins

Activation of the Time Recording for Field Service \(com.snc.wm\_time\_recording\) plugin activates these related plugins when they aren’t already active.

<table id="table_i5n_bbv_frb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time Card Management\[com.snc.time\_card\]

</td><td>

Enables time card users such as task assignees to report and track their time for the assigned tasks.

</td></tr><tr><td>

Cost Management\[com.snc.cost\_management\]

</td><td>

Enables tracking configuration item costs. The costs can be allocated to business units and used in reports.

</td></tr></tbody>
</table>## Time Recording Roles

Time Recording for Field Service adds the following roles:

<table id="table_h1b_t4z_mbb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time card usertimecard\_user

</td><td>

Create time worked records, time cards, and time sheets. Users with the wm\_agent role inherit the timecard\_user role.**Note:** This role restricts access to the time sheets, time cards, and time worked records created by the agent.

</td></tr><tr><td>

Time card admintimecard\_admin

</td><td>

View, approve, and reject time cards and time sheets. Users with the wm\_manager role inherit the timecard\_admin role.**Note:** This role restricts access to the time sheets, time cards, and time worked records created by the agents in the groups assigned to the manager.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

