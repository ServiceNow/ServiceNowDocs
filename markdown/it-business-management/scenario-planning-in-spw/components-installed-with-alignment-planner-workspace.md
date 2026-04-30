---
title: Components installed with Strategic Planning Workspace
description: Several types of components are installed with installation of the Strategic Planning application, such as user roles, tables, scheduled jobs, system properties, and custom scripts.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Components installed with Strategic Planning Workspace

Several types of components are installed with installation of the Strategic Planning application, such as user roles, tables, scheduled jobs, system properties, and custom scripts.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Roles installed with Strategic Planning Workspace

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Strategic Planning Workspace admin\[sn\_align\_core.apw\_admin\]

</td><td>

Can access all the features in the Strategic Planning application.**Note:** Goals and Capacity Planning can be accessed only with the sn\_apw\_advanced.spw\_goal\_user\_read and sn\_align\_ws.spw\_capacity\_read roles respectively.

</td><td>

-   it\_portfolio\_manager
-   sn\_align\_core.apw\_user
-   sn\_gf.goal\_admin
-   view\_changer

</td></tr><tr><td>

Strategic Planning Workspace user\[sn\_align\_core.apw\_user\]

</td><td>

Can create, update, and delete portfolio plans, free-form roadmaps, and planning items.

 This role can be given to users such as portfolio or product managers, business unit leads, and other planning personas.

</td><td>

-   sn\_align\_cmn\_int.user
-   sn\_milestones.milestone\_editor
-   sn\_gf.strategy\_planner
-   sn\_gf.goal\_user
-   sn\_align\_core.ap\_read\_only
-   model\_manager

</td></tr><tr><td>

sn\_align\_core.ap\_read\_only

</td><td>

-   Can view portfolio plans \(Planning and Scoring pages\) and free-form roadmaps that are shared with them.
-   Can add notes, comments, or attachments to portfolio plans and roadmaps that are shared with them.
-   Can create, edit, and delete portfolio plan views and free-form roadmap views.

**Note:** Only the owner can edit or delete a portfolio plan view or a free-form roadmap view.


</td><td>

-   sn\_milestones.milestone\_viewer
-   sn\_dpr\_model.product\_enhancement\_read
-   sn\_dpr\_model.product\_feature\_read

</td></tr><tr><td>

Milestones editor\[sn\_milestones.milestone\_editor\]

</td><td>

Can create, update, and delete milestones on the roadmap.

</td><td>

sn\_milestones.milestone\_viewer

</td></tr><tr><td>

Milestones viewer\[sn\_milestones.milestone\_viewer\]

</td><td>

Can view milestones on the roadmap.

</td><td>

None

</td></tr><tr><td>

Business stakeholder\[business\_stakeholder\]

</td><td>

-   Can create and update portfolio plans and free-form roadmaps.
-   Can add notes, comments, or attachments to portfolio plans and roadmaps that are shared with them.
-   Can personalize the roadmaps.
-   Can view generated resource capacity for planning items in the Capacity Planning screen.
-   Can view goals defined for the portfolio plan.

 **Note:** Users with this role do not have access to create or edit any roadmap items.

</td><td>

-   sn\_align\_core.ap\_read\_only
-   sn\_align\_ws.spw\_capacity\_read
-   sn\_apw\_advanced.spw\_goal\_user\_read

</td></tr></tbody>
</table>|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_align\_ws.scenario\_approver|Can approve the scenarios for the portfolio.|sn\_align\_core.apw\_user|

<table id="table_lx2_q51_fdc"><thead><tr><th>

Role title \[name\]

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

-   Can create, view, edit, and delete goals, subgoals, and associated targets.

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

-   Create goals and targets.
-   Edit goals and targets created by other users.
-   Edit target breakdowns.

**Note:** The user must also be assigned the sn\_apw\_advanced.spw\_goal\_user role to edit target breakdowns.

-   Can update the goal preferences.
-   Can create target sources and context variables as part of enabling the target automation feature.

**Note:** The sn\_gf.goal\_admin role is installed as part of Goal Framework installation but this privilege is added to the role when Goal Framework for SPM is installed.


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

</td></tr><tr><td>

sn\_apw\_advanced.spw\_goal\_user

</td><td>

Can view the Goals page in the Strategic Planning Workspace and edit goals and targets.

</td><td>

-   sn\_apw\_advanced.spw\_goal\_user\_read
-   sn\_gf.goal\_user

</td></tr><tr><td>

sn\_apw\_advanced.spw\_goal\_user\_read

</td><td>

Can view the Goals page in the Strategic Planning Workspace.

</td><td>

sn\_gf.goal\_user\_read

</td></tr></tbody>
</table><table id="table_nnx_q51_fdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Strategic Planning integrations user

 \[sn\_align\_cmn\_int.user\]

</td><td>

Imports, exports, and manages planning items between Strategic Planning and Agile, SAFe, and PPM.

</td><td>

connection\_admin

</td></tr></tbody>
</table>|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_align\_ws.spw\_capacity\_user|Can generate resource capacity details.|sn\_align\_ws.spw\_capacity\_read|
|sn\_align\_ws.spw\_capacity\_read|Can view resource capacity details.|None|

<table id="table_n5v_r51_fdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_align\_ws.spw\_financial\_user

</td><td>

-   Can view financials, create cost plans and expense lines, create and compare financial baselines for planning items.
-   Can create, edit, and view financial values in scenario planning.

</td><td>

None

</td></tr><tr><td>

sn\_align\_ws.spw\_funding\_user

</td><td>

Can view the financial widgets while comparing scenarios and approve a scenario with financial changes.

</td><td>

sn\_align\_ws.spw\_financial\_user

</td></tr></tbody>
</table>## Tables installed with Strategic Planning Workspace

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom planning item 1\[sn\_align\_core\_custom\_planning\_item\_1\]

</td><td>

Stores information for a additional planning item type.

</td></tr><tr><td>

Custom planning item 2\[sn\_align\_core\_custom\_planning\_item\_2\]

</td><td>

Stores information for a additional planning item type.

</td></tr><tr><td>

Custom planning item 3\[sn\_align\_core\_custom\_planning\_item\_3\]

</td><td>

Stores information for a additional planning item type.

</td></tr><tr><td>

Custom planning item 3\[sn\_align\_core\_custom\_planning\_item\_3\]

</td><td>

Stores information for a additional planning item type.

</td></tr><tr><td>

Custom planning item 4\[sn\_align\_core\_custom\_planning\_item\_4\]

</td><td>

Stores information for a additional planning item type.

</td></tr><tr><td>

Custom planning item 5\[sn\_align\_core\_custom\_planning\_item\_5\]

</td><td>

Stores information for a additional planning item type.

</td></tr><tr><td>

Demand\[sn\_align\_core\_demand\]

</td><td>

Stores records created with Demand planning item type.

</td></tr><tr><td>

Epic\[sn\_align\_core\_scrum\_epic\]

</td><td>

Stores records created with Epic planning item type. These records could be Scrum or SAFe epics.

</td></tr><tr><td>

Initiative\[sn\_align\_core\_initiative\]

</td><td>

Stores records created with Initiative item.

</td></tr><tr><td>

Lens\[sn\_align\_core\_lens\]

</td><td>

Stores data of the lens configuration.

</td></tr><tr><td>

Lens structure\[sn\_align\_core\_lens\_structure\]

</td><td>

Stores data of lens entities and the relationship between them for different lenses.

</td></tr><tr><td>

Milestone\[sn\_milestones\_milestone\]

</td><td>

Stores data of milestones.

</td></tr><tr><td>

Planning Item\[sn\_align\_core\_planning\_item\]

</td><td>

Stores the data of all planning item types.

</td></tr><tr><td>

Portfolio plan\[sn\_align\_ws\_portfolio\_plan\]

</td><td>

Stores data of portfolio plans.

</td></tr><tr><td>

Project\[sn\_align\_core\_project\]

</td><td>

Stores records created with Project planning item type.

</td></tr><tr><td>

Roadmap configuration\[sn\_align\_ws\_roadmap\_configuration\]

</td><td>

Stores the configuration data for tables that are used to create portfolio roadmaps and free-form roadmaps.

</td></tr><tr><td>

Strategic Program\[sn\_align\_core\_program\]

</td><td>

Stores records created with Strategic Program item.

</td></tr></tbody>
</table><table id="table_zqc_tw1_fdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Context Variable\[sn\_gfa\_context\_variable\]

</td><td>

Stores the context variable details for the target source.

</td></tr><tr><td>

Goal\[sn\_gf\_goal\]

</td><td>

Stores the goal details.

</td></tr><tr><td>

Goal Assigned Entity Configuration\[sn\_gf\_assigned\_entity\_config\]

</td><td>

Store the assigned entity configuration for a table for an assigned entity type, so that the goal user can associate the goal with the required assigned entity.

</td></tr><tr><td>

Goal Core\[sn\_gf\_core\_goal\]

</td><td>

Stores the core \(basic\) details for the goal. The Goal \[sn\_gf\_goal\] table extends the Goal Core \[sn\_gf\_core\_goal\] table.

</td></tr><tr><td>

Goal Relationship\[sn\_gf\_goal\_m2m\_relationship\]

</td><td>

Defines the relationship between a goal and items \(Project, Demand, Program, Scrum Epic, Scrum Feature, SAFe Epic, SAFe Feature, and Planning item\).

</td></tr><tr><td>

Strategic Plan\[sn\_gf\_strategic\_plan\]

</td><td>

Stores the strategic plans defined for each planning organization hierarchy.

</td></tr><tr><td>

Strategic Priority\[sn\_gf\_strategy\]

</td><td>

Stores the strategic priorities defined for the organization.

</td></tr><tr><td>

Strategy Value\[sn\_gf\_strategy\_value\]

</td><td>

Stores the strategic values for strategic plans.

</td></tr><tr><td>

Target\[sn\_gf\_goal\_target\]

</td><td>

Stores the target details for the goal.

</td></tr><tr><td>

Target Breakdown\[sn\_gfa\_target\_breakdown\]

</td><td>

Stores the target breakdown details for the target that were created based on the breakdown intervals specified for the target.

</td></tr><tr><td>

Target Progress\[sn\_gf\_goal\_target\_progress\]

</td><td>

Stores the target progress details for the goal.

</td></tr><tr><td>

Target Source\[sn\_gfa\_target\_source\]

</td><td>

Stores the target source configuration details for automating the actual value of the targets.

</td></tr><tr><td>

Units\[sn\_gf\_units\]

</td><td>

Stores the available units for measuring the progress of targets.

</td></tr></tbody>
</table><table id="table_fkl_tw1_fdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Map

 \[sn\_align\_cmn\_int\_field\_map\]

</td><td>

Field mappings for work items between Strategic Planning and the execution applications.

</td></tr><tr><td>

Alignment Integration

 \[sn\_align\_cmn\_int\_integrations\_setup\]

</td><td>

Integration setup information for your instance.

</td></tr><tr><td>

Table Map

 \[sn\_align\_cmn\_int\_table\_map\]

</td><td>

Table maps for work items between Strategic Planning and the execution applications.

</td></tr><tr><td>

Integration Mapping

 \[sn\_align\_cmn\_int\_integration\_mapping\]

</td><td>

Integration mappings for work items between Strategic Planning and the execution applications.

</td></tr><tr><td>

Import Request

 \[sn\_align\_cmn\_int\_import\_request\]

</td><td>

Stores the information for import requests created to import records from PPM, Agile Development 2.0, or SAFe to Strategic Planning.

</td></tr><tr><td>

Instance Mapping

 \[sn\_align\_cmn\_int\_instance\_mapping\]

</td><td>

Stores instance mapping information between Strategic Planning and the execution applications.

</td></tr><tr><td>

Integration Error

 \[sn\_align\_cmn\_int\_integration\_error\]

</td><td>

List of the integration errors.

</td></tr><tr><td>

Choice Map

 \[sn\_align\_cmn\_int\_choice\_map\]

</td><td>

Workflow choice mappings for work items between Strategic Planning and the execution applications.

</td></tr></tbody>
</table><table id="table_erv_tw1_fdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Investment Baselines

 \[sn\_invst\_pln\_invst\_investment\_baseline\]

</td><td>

Stores the information about the financial baselines.

</td></tr><tr><td>

Investment Baseline Headers

 \[sn\_invst\_pln\_invst\_investment\_baseline\_header\]

</td><td>

Stores all the information about financial baselines and the investment tables.

</td></tr><tr><td>

Investment Budget

\[sn\_invst\_pln\_invst\_budget\]

</td><td>

Stores the migrated budget information to work on lean budgeting at required time scope.

</td></tr></tbody>
</table><table id="table_tlf_5w1_fdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scoring Framework\[sn\_apw\_advanced\_scoring\_framework\]

</td><td>

Stores the records of scoring frameworks such as RICE, WSJF, Value vs Effort, or any new custom framework.

</td></tr><tr><td>

Scoring Framework Attribute\[sn\_apw\_advanced\_scoring\_attributes\]

</td><td>

Stores the attributes of each of the scoring frameworks such as Reach, Impact, Confidence, Effort, Value, Job Size, Time Criticality, and so on. These attributes are of Glide var type fields.

</td></tr></tbody>
</table><table id="table_dxv_hmj_b2c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product Enhancement\[sn\_dpr\_model\_product\_enhancement\]

</td><td>

Stores the information about the product enhancement of a product feature.

</td></tr><tr><td>

Product Feature\[sn\_dpr\_model\_product\_feature\]

</td><td>

Stores the information about the function or capability that adds value to a product for the customer.

</td></tr></tbody>
</table>## Scheduled jobs installed with Strategic Planning Workspace

|Scheduled job|Description|
|-------------|-----------|
|Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables|Migrates the existing goals data to the Goal Framework tables. For information on what data is migrated and how the data can be migrated, see [goal data migration](../../spw-goals/task/migrate-existing-goals-data-apw.md).|
|Migrate goal relationships for assigned entities|Populates the fields, **Assigned entity type** and **Assigned entity** on the [Goal form](../../spw-goals/reference/goal-form-egm.md) based on the data in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table if you have created m2m relationship with lens entities other than **Company**, **Business Unit**, **Department**, and **Portfolio**.|
|Clear the Planning item value in the Goal Relationship for strategic items|Clears the planning item value in the existing Goal Relationship records for strategic items - Program and Initiative.|
|Update Actual value of the targets using Goal Framework for SPM|Updates the actual value of the targets by collecting the data from the respective target sources, so that the progress of the targets is updated and then the targets' progress is rolled up to the goals.|
|Create Goals Demo Data with Target Breakdowns|Creates a target breakdowns demo data for the targets.|

|Scheduled job|Description|
|-------------|-----------|
|Create Financial Baseline For Planning Items|Automatically create financial baselines for your planning items at a defined cadence.|
|Migrate budget for active demands and projects|Migrate the budget of your planning items as a bulk action.|
|Generate Labor Costs|Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments for Projects and Demands.|
|Generate Labor Costs For Epic|Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments for Epics.|

## Custom scripts installed with Strategic Planning Workspace

<table id="table_hlp_flh_dvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Benefit PlansA target source with predefined script.

</td><td>

Predefined script that updates the **Actual value** field on the target form by fetching the required value from the **Actual benefit** field or **Non-monetary actual benefit** field from the monetary or non-monetary benefit plan records. For script template, see [Predefined target automation script for benefit plans](../../spw-goals/reference/target-automation-script-benefit-plans-apw.md).**Note:** You can use the Benefit Plans custom script only when PPM Standard \(Project Portfolio Management\) is installed.

</td></tr></tbody>
</table>## System properties installed with Strategic Planning Workspace

<table id="table_jmj_kvt_c2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_align\_ws.portfolio\_plan\_items\_limit

</td><td>

Option to define the number of planning items to be loaded on the planning page.**Note:** If the value in the system property is more than 250, the performance of the UI may degrade. The default value is 250.

</td></tr><tr><td>

sn\_align\_ws.item\_milestone\_limit

</td><td>

Option to define the number of milestone items to be loaded in the Roadmap tab. The default value is 50.

</td></tr><tr><td>

sn\_align\_ws.is\_scenario\_planning\_disabled

</td><td>

Option to enable the scenario\_planning feature.

</td></tr><tr><td>

sn\_align\_core.planning\_item\_types\_allow\_list

</td><td>

Option to define the planning item types to be allowed for configured for a portfolio plan.

</td></tr></tbody>
</table><table id="table_zqj_zbx_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.sn\_gf\_goal\_target\_activity.fields

</td><td>

Option to enable activity stream for fields of the targets.

</td></tr><tr><td>

glide.ui.sn\_gf\_goal\_activity.fields

</td><td>

Option to enable activity stream for fields of the goals.

</td></tr><tr><td>

sn\_align\_ws.goal\_hierarchy.max\_records

</td><td>

Specifies the number of goals to be loaded on the Hierarchy tab on the Goals view.**Note:** If the value in the system property is more than 500, the performance of the Goals UI may degrade. The default value is 500.

</td></tr><tr><td>

sn\_gf.allow\_goal\_deletion

</td><td>

Option to enable deletion of goals. The default value is true.

</td></tr><tr><td>

sn\_gf.allow\_target\_deletion

</td><td>

Option to enable deletion of targets. The default value is true.

</td></tr><tr><td>

sn\_gf.goal\_calendar\_type

</td><td>

Option to set calender type for setting goals. The available calendar types are Gregorian Calendar and Fiscal Period. The default value is Gregorian Calendar.

</td></tr><tr><td>

sn\_gf.weighted\_average\_enabled

</td><td>

Option to enable the weighted average logic to calculate the progress of goals from their subgoals and targets.

</td></tr><tr><td>

sn\_gfa\_disable\_target\_breakdown

</td><td>

Option to enable the target breakdowns feature at the instance level. The default value is false.

</td></tr><tr><td>

sn\_gfa.target\_breakdown\_decimals

</td><td>

Option to define the number of decimals to show for target values while generating the target breakdowns. The default value is 2.

</td></tr><tr><td>

sn\_gfa.weeklyCheckInDayToMapMonth

</td><td>

Option to define end day of the week for weekly target breakdowns mapping to month. The default value is Friday.

</td></tr></tbody>
</table><table id="table_kk1_wy1_fdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.sn\_align\_cmn\_int.bulk\_import

</td><td>

-   Type: Choice list
-   Default value: INSERT
-   Other possible values:
    -   INSERT
    -   &lt;Value 2 name&gt;:
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure bulk import](../../apw-internal-integrations/reference/configure-bulk-import.md)

</td></tr></tbody>
</table>**Parent Topic:**[Strategic Planning Workspace reference](alignment-planner-workspace-reference.md)

