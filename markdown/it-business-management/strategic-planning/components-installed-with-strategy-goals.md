---
title: Components installed with Strategy and Goals
description: Several types of components are installed with installation of the Strategic Planning application, such as user roles, tables, scheduled jobs, system properties, and custom scripts.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Reference, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Components installed with Strategy and Goals

Several types of components are installed with installation of the Strategic Planning application, such as user roles, tables, scheduled jobs, system properties, and custom scripts.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

**Note:** This topic covers reference information specific to Strategy and Goals, including user roles, tables, and system properties. For common reference information about tables, roles, and system properties installed with Strategic Planning, see [Strategic Planning Workspace reference](../../alignment-planner-workspace/reference/alignment-planner-workspace-reference.md).

## Tables installed with Strategic Planning Workspace

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Strategic Plan\[sn\_gf\_strategic\_plan\]

</td><td>

Stores the strategic plans defined for each planning organization hierarchy.

</td></tr><tr><td>

Strategic Priority\[sn\_gf\_strategy\]

</td><td>

Stores the strategic priorities defined for the organization.

</td></tr></tbody>
</table>## System properties installed with Strategic Planning Workspace

<table id="table_jmj_kvt_c2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

target\_checkin\_due\_date\_reminder\_feature\_toggle

</td><td>

Option to enable the reminder notifications feature for target actuals check-in.

</td></tr><tr><td>

target\_checkin\_due\_date\_reminder\_config

</td><td>

Option to define the number of days before the due date to send the reminder for target actuals check-in.The default values depend on the check-in frequency set for the target:

-   For the **None** check-in frequency, the default is 7 days.
-   For **Weekly** it's 2 days.
-   For **Monthly**, it's 5 days.
-   For **Quarterly**, it's 7 days.
-   For **Yearly**, it's 10 days.

</td></tr></tbody>
</table>## Scheduled jobs installed with Strategic Planning Workspace

|Scheduled job|Description|
|-------------|-----------|
|Goal insights generation job|Generates goal insights automatically for the set of goals that match the defined goal filter criteria.|

**Parent Topic:**[Strategy and Goals reference](strategy-goals-reference.md)

