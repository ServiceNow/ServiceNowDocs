---
title: Components installed with Goal Framework and Goal Framework for SPM
description: Several types of components are installed with the installation of the Goal Framework and Goal Framework for Strategic Portfolio Management \(SPM\) applications, including user roles, scheduled jobs, tables, and scripts.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Components installed with Goal Framework and Goal Framework for SPM

Several types of components are installed with the installation of the Goal Framework and Goal Framework for Strategic Portfolio Management \(SPM\) applications, including user roles, scheduled jobs, tables, and scripts.

## Roles installed

<table id="table_sb2_g2y_gpb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_gf.goal\_user\_read

</td><td>

Can view the goals. This role can be given to users such as the project user and demand user.

</td><td>

None

</td></tr><tr><td>

sn\_gf.goal\_user

</td><td>

-   Can create, view, edit, and delete goals, sub-goals, and associated targets.

**Note:**

    -   A goal or sub-goal can be deleted only by the owner and contributors of the goal or its immediate parent goal when the **sn\_gf.allow\_goal\_deletion** system property is set to **Yes**.
    -   An associated target can be deleted only by the owner and contributors of the target or its goal when the **sn\_gf.allow\_goal\_deletion** system property is set to **Yes**.
    -   A goal can be edited only by the owner and contributors of the goal or its immediate parent goal.
    -   A target can be edited only by the owner and contributors of the target or its goal.
-   Can remove the existing goal relationships between work item and goal, from the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table.

</td><td>

sn\_gf.goal\_user\_read

</td></tr><tr><td>

sn\_gf.goal\_admin

</td><td>

-   Can update the goal preferences.
-   Can create target sources and context variables as part of enabling the target automation feature.

**Note:** Creating target sources and context variables is available when Goal Framework for SPM is installed.


</td><td>

-   sn\_gf.goal\_user\_read
-   sn\_gf.goal\_user

</td></tr><tr><td>

sn\_gf.strategy\_planner\_read

</td><td>

Can view all strategic plans and strategic values.

</td><td>

None

</td></tr><tr><td>

sn\_gf.strategy\_planner

</td><td>

Can create, view, edit, and delete strategic plans and strategic values.**Note:**

-   A strategic plan can be edited only by the owner and sponsor of the strategic plan.
-   A strategic value can be edited only by the sponsor of the strategic plan.

</td><td>

sn\_gf.strategy\_planner\_read

</td></tr><tr><td>

sn\_gf.epmo\_strategy\_planner

</td><td>

Can create, view, edit, and delete any goal.

</td><td>

-   sn\_gf.goal\_user\_read
-   sn\_gf.goal\_user
-   sn\_gf.goal\_admin
-   sn\_gf.strategy\_planner

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables|Migrates the existing goals data to the Goal Framework tables. For information on what data is migrated and how the data can be migrated, see [goal data migration.](../task/migrate-existing-goals-data.md)|
|Migrate goal relationships for assigned entities|\(For Strategic Planning users\) Populates the fields, **Assigned entity type** and **Assigned entity** on the [Goal form](../../spw-goals/reference/goal-form-egm.md) based on the data in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table if you have created m2m relationship with lens entities other than **Company**, **Business Unit**, **Department**, and **Portfolio**.|

|Scheduled job|Description|
|-------------|-----------|
|Update Actual value of the targets using Goal Framework for SPM|Updates the actual value of the targets by collecting the data from the respective target sources, so that the progress of the targets is updated and then the targets' progress is rolled up to the goals.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Display name \[Table name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Goal\[sn\_gf\_goal\]

</td><td>

Stores the goal details.

</td></tr><tr><td>

Goal Core\[sn\_gf\_core\_goal\]

</td><td>

Stores the core \(basic\) details for the goal. The Goal \[sn\_gf\_goal\] table extends the Goal Core \[sn\_gf\_core\_goal\] table.

</td></tr><tr><td>

Target\[sn\_gf\_goal\_target\]

</td><td>

Stores the target details for the goal.

</td></tr><tr><td>

Units\[sn\_gf\_units\]

</td><td>

Stores the available units for measuring the progress of targets.

</td></tr><tr><td>

Target Progress\[sn\_gf\_goal\_target\_progress\]

</td><td>

Stores the target progress details for the goal.

</td></tr><tr><td>

Goal Relationship\[sn\_gf\_goal\_m2m\_relationship\]

</td><td>

Defines the relationship between a goal and items \(Project, Demand, Program, Scrum Epic, Scrum Feature, and Planning item\).

</td></tr><tr><td>

Strategic Plan\[sn\_gf\_strategic\_plan\]

</td><td>

Stores the strategic plans defined for each planning organization hierarchy.**Note:** This table is visible only when Alignment Planner Workspace \(APW\) is installed.

</td></tr><tr><td>

Strategic Priority\[sn\_gf\_strategy\]

</td><td>

Stores the strategic priorities defined for the organization.

</td></tr><tr><td>

Strategy Value\[sn\_gf\_strategy\_value\]

</td><td>

Stores the strategic values for strategic plans.**Note:** This table is visible only when APW is installed.

</td></tr></tbody>
</table><table id="table_yvt_cmb_fdc"><thead><tr><th>

Display name \[Table name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Context Variable\[sn\_gfa\_context\_variable\]

</td><td>

Stores the context variable details for the target source.

</td></tr><tr><td>

Target Breakdown\[sn\_gfa\_target\_breakdown\]

</td><td>

Stores the target breakdown details for the target that were created based on the breakdown intervals specified for the target.

</td></tr><tr><td>

Target Source\[sn\_gfa\_target\_source\]

</td><td>

Stores the target source configuration details for automating the actual value of the targets.

</td></tr></tbody>
</table>## Custom scripts installed

<table id="table_hlp_flh_dvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Benefit PlansA target source with predefined script.

</td><td>

Predefined script that updates the **Actual value** field on the target form by fetching the required value from the **Actual benefit** field or **Non-monetary actual benefit** field from the monetary or non-monetary benefit plan records. For the script template, see [Target automation script for benefit plans](target-automation-script-benefit-plans.md).**Note:** You can use the Benefit Plans custom script only when PPM Standard \(Project Portfolio Management\) is installed.

</td></tr></tbody>
</table>## System properties installed

|Name|Description|
|----|-----------|
|sn\_gf.allow\_goal\_deletion|Option to enable deletion of goals. The default value is true.|
|sn\_gf.allow\_target\_deletion|Option to enable deletion of targets. The default value is true.|
|sn\_gf.goal\_calendar\_type|Option to set calender type for setting goals. The available calendar types are Gregorian Calendar and Fiscal Period. The default value is Gregorian Calendar.|
|sn\_gf.weighted\_average\_enabled|Option to enable the weighted average logic to calculate the progress of goals from their subgoals and targets.|

|Name|Description|
|----|-----------|
|sn\_gfa\_disable\_target\_breakdown|Option to enable the target breakdowns feature at the instance level. The default value is false.|
|sn\_gfa.target\_breakdown\_decimals|Option to define the number of decimals to show for target values while generating the target breakdowns. The default value is 2.|
|sn\_gfa.weeklyCheckInDayToMapMonth|Option to define end day of the week for weekly target breakdowns mapping to month. The default value is Friday.|

**Parent Topic:**[Goal Framework and Goal Framework for SPM reference](goal-framework-reference.md)

