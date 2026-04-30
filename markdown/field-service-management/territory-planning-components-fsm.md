---
title: Field Service Territory Planning components
description: Several types of components are installed with the Field Service Territory Planning feature, including tables, role, script includes, and business rules.Territory Planning console uses the following properties.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Field Service Territory Planning components

Several types of components are installed with the Field Service Territory Planning feature, including tables, role, script includes, and business rules.

## Tables

Field Service Territory Planning adds the following tables.

<table id="table_w5n_3bj_stb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territorysn\_tp\_territory

</td><td>

Stores information about territories, such as the name of a territory.

</td></tr><tr><td>

Territory Conditionsn\_tp\_territory\_condition

</td><td>

Stores conditions added to a territory to filter the best matched territory for a work order or work order task.

</td></tr><tr><td>

Territory Geographysn\_tp\_territory\_geography

</td><td>

Stores the geoJSON script information that is auto-generated when drawing a geography for the territories.

</td></tr><tr><td>

Territory Groupsn\_tp\_territory\_group

</td><td>

Stores information about the qualification, dispatch, and assignment groups assigned to a territory.

</td></tr><tr><td>

Territory Membership Overridesn\_tp\_territory\_membership\_override

</td><td>

Store information whether the agent or crew is primary or secondary member of the territory.

</td></tr><tr><td>

Territory Modelsn\_tp\_territory\_model

</td><td>

Store information about the default territory model and its mapped territories and resources.

</td></tr><tr><td>

Territory Model Sourcesn\_tp\_territory\_model\_source

</td><td>

Store information about the source tables mapped to the territory model, such as wm\_task and wm\_order.

</td></tr><tr><td>

Territory Managersn\_tp\_territory\_manager

</td><td>

Stores information regarding the managers of the territory.

</td></tr></tbody>
</table>## Roles

Field Service Territory Planning adds the following roles.

<table id="table_rsw_l3l_stb"><thead><tr><th>

Roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Service Territory Edit Resource Allocation\[sn\_fsm\_tp.fsm\_territory\_edit\_resource\_allocation\]

</td><td>

Edit allocation of resources who are associated with the selected Field Service territory.

</td></tr><tr><td>

FSM Territory Planner\[sn\_fsm\_tp.fsm\_territory\_planner\]

</td><td>

Create Field Service territories along with the ability to view the existing Field Service territories, manage resource allocation in territories, and others.

</td></tr><tr><td>

FSM Territory Read\[sn\_fsm\_tp.fsm\_territory\_read\]

</td><td>

View Field Service territory data.

</td></tr><tr><td>

Territory Admin\[sn\_tp.territory\_admin\]

</td><td>

Create territory models, sources, and matching rules.

</td></tr><tr><td>

Territory Edit Resource Allocation\[sn\_tp.territory\_edit\_resource\_allocation\]

</td><td>

Edit allocation of resources who are associated with the selected territory.

</td></tr><tr><td>

Territory Geography Write\[sn\_tp.territory\_geography\_write\]

</td><td>

Create, update, or delete the territory geography.

</td></tr><tr><td>

Territory Planner\[sn\_tp.territory\_planner\]

</td><td>

View territories, resource allocations, and others along with the ability to create territories.

</td></tr><tr><td>

Territory Read\[sn\_tp.territory\_read\]

</td><td>

Viewing territory data.

</td></tr><tr><td>

Territory Resource Manager\[sn\_tp.territory\_resource\_manager\]

</td><td>

Manage resources of territory where the logged-in user has been assigned as resource manager

</td></tr><tr><td>

Territory Manager\[sn\_tp.territory\_manager\]

 \[sn\_tp.territory\_resource\_manager\]

</td><td>

Manage territories and their related information. Additionally, inherit the role of territory resource manager.

</td></tr><tr><td>

FSM Territory Manager\[sn\_fsm\_tp.fsm\_territory\_manager\]

 \[sn\_tp.territory\_manager\]

 \[sn\_tp.territory\_resource\_manager\]

</td><td>

Manage Field Service territories and their related information. Additionally, inherit the role of territory resource manager.

</td></tr><tr><td>

FSM Territory Resource Manager\[sn\_fsm\_tp.fsm\_resource\_manager\]

 \[sn\_tp.territory\_manager\]

 \[sn\_tp.territory\_resource\_manager\]

</td><td>

Manage Field Service resources of territory where the logged-in user has been assigned as resource manager

</td></tr></tbody>
</table>## Script Includes

Field Service Territory Planning adds the following script includes.

|Script include|Description|
|--------------|-----------|
|FieldServiceTerritoryPlanning|Contains the utility functions to provide data, such as territory details, assignment groups, or others to data brokers.|
|MatchTerritoryCondition|Contains the utility functions Filter territories for work order task based on the filtering conditions used by the territory planning matching rules​.|
|TerritoryFilters|Contains methods for all reference qualifiers to filter territory based on the corresponding groups, agents, crews, and parent territory.|
|TerritoryMatchingDimensionLocation|Contains the utility functions to filter territories based on the task location to be used by the Matching Rule​.|
|TerritoryPlanningHelpers|Contains helper methods for overall territory planning implementation.|
|TerritoryPlanningAJAX|Ajax class that provides helper functions to verify if the territory planning plugin is active, get default model, populate territory in the work order task form, and validates the assignment group selected for a work order task.|

## Business Rules

Field Service Territory Planning adds the following business rules.

<table id="table_amv_vjl_stb"><thead><tr><th>

Business Rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delete Agent Override

</td><td>

Territory Group\[sn\_tp\_territory\_group\]

</td><td>

Deletes the modified membership record of an agent when the corresponding group is deleted​ from the territory.

</td></tr><tr><td>

Delete Crew Member Override

</td><td>

Territory Group\[sn\_tp\_territory\_group\]

</td><td>

Deletes the modified membership record of a crew when the corresponding group is deleted​ from the territory.

</td></tr><tr><td>

Populate assignment groups

</td><td>

Territory Group\[sn\_tp\_territory\_group\]

</td><td>

Auto-populates the corresponding assignment groups when adding a dispatch group to the territory.

</td></tr><tr><td>

Update Territory if not matched

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Validates and assigns the best territory for the selected assignment group​ when allow\_assignment\_override is selected.

</td></tr><tr><td>

Validate Qualification Group

</td><td>

Work Order\[wm\_order\]

</td><td>

Checks if work order has a valid qualification group​.

</td></tr><tr><td>

Allow only unique group-territory

</td><td>

Territory Group\[sn\_tp\_territory\_group\]

</td><td>

Prevents adding a combination of duplicate groups that includes qualification, dispatcher, and assignment to a territory.

</td></tr><tr><td>

Allow only unique users

</td><td>

Territory Membership Override\[sn\_tp\_territory\_membership\_override\]

</td><td>

Prevents the selection of duplicate user for a territory in the territory membership override table​.

</td></tr><tr><td>

Calculate geography bounding box

</td><td>

Territory Geography\[sn\_tp\_territory\_geography\]

</td><td>

Calculates the maximum or minimum latitude and longitude value from defined territory geography GeoJSON​.

</td></tr><tr><td>

Check and create crew membership

</td><td>

Work order task\[wm\_task\]

</td><td>

Creates a territory membership record for the dynamically assigned crew when saving the work order task, setting the 'From' and 'To' dates to match the 'Effective start' and 'Effective end' dates of the crew.

</td></tr><tr><td>

Membership date validations

</td><td>

Territory Membership Override\[sn\_tp\_territory\_membership\_override\]

</td><td>

Validates the dates entered in the **From** and **To** fields in the territory membership override table for a territory member.

</td></tr><tr><td>

Validate Color Field

</td><td>

Territory\[sn\_tp\_territory\]

</td><td>

Validates the hexadecimal code for the color of a territory.

</td></tr><tr><td>

Validate Parent

</td><td>

Territory\[sn\_tp\_territory\]

</td><td>

Validates the hierarchy of a parent territory.

</td></tr><tr><td>

Validate Source Table For Model

</td><td>

Territory Model Source\[sn\_tp\_territory\_model\_source\]

</td><td>

Prevents duplicate entries for a model and source table on the territory model source.

</td></tr><tr><td>

Validate Territory Condition

</td><td>

Territory Condition\[sn\_tp\_territory\_condition\]

</td><td>

Prevents the creation of duplicate entries for territory conditions for a specific territory.

</td></tr><tr><td>

Validate territory geography name

</td><td>

Territory Geography\[sn\_tp\_territory\_geography\]

</td><td>

Prevents the creation of duplicate entries for a new territory geography.

</td></tr><tr><td>

Validate Territory Model Name

</td><td>

Territory Model\[sn\_tp\_territory\_model\]

</td><td>

Prevents the creation of duplicate entries for a new territory model.

</td></tr><tr><td>

Validate Territory Name

</td><td>

Territory\[sn\_tp\_territory\]

</td><td>

Prevents the creation of duplicate entries for a new territory.

</td></tr><tr><td>

Validate User and Territory

</td><td>

Territory Membership Override\[sn\_tp\_territory\_membership\_override\]

</td><td>

Ensures that the user added to the territory membership override table is associated with the territory

</td></tr></tbody>
</table>## Properties

Field Service Territory Planning adds the following system properties.

<table id="table_s2q_vfq_5zb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm.use\_query\_rules

</td><td>

When the setting is "true", the rules from the "sn\_query\_rule" table control what Field Service Management-related data a user can read. This includes work orders \(WO\) and work order tasks \(WOT\). If set to "false", these records aren't filtered based on rules, and users can access them without rule-based restrictions.-   **Type**: Boolean
-   **Default value**: False
-   Location: **All** &gt; **sys\_properties\_list.do**

</td></tr><tr><td>

sn\_tp.max\_coordinates\_allowed

</td><td>

Maximum number of coordinates allowed in GeoJSON Geography. This property is read only and is non-editable. -   **Type**: Integer
-   **Default value**: 3250
-   Location: **All** &gt; **Territory Planning** &gt; **Properties**

</td></tr><tr><td>

sn\_tp.percentage\_overlap

</td><td>

Percentage value \(ranging from 0 to 100\) indicating the threshold for geographical overlap between territories. The default is set to 5%.-   **Type**: Integer
-   **Default value**: 5
-   Location: **All** &gt; **Territory Planning** &gt; **Properties**

</td></tr></tbody>
</table>## Query Rules

Field Service Territory Planning adds the following query rule. You can find the following query rule by clicking **All** &gt; **sn\_query\_rule\_list.do**

|Query rule|Description|
|----------|-----------|
|wm task - My assigned territory|Allows admins to enable data security for agents, dispatchers, and qualifiers for work orders and work order tasks. This helps them to see the work orders and work order tasks created in their territories. Mark the **WO - My territory** and **WOT - MY Territory** tables as active.|

## Scheduled Jobs

Field Service Territory Planning adds the following Schedule Optimization adds the following scheduled jobs. You can find the following scheduled jobs by clicking **All** &gt; **sn\_schedulejobs.do**

|Scheduled job|Description|
|-------------|-----------|
|Territory Planning- Calculate Overlapping Territories|Calculates the overlaps for both agents and geographies.|
|Territory Planning- Calculate Overlapping Territories - Agent|Calculates the overlaps for agents. When executed, the scheduled job triggers events to calculate the overlap between two agents.|
|Territory Planning- Calculate Overlapping Territories - Geography|Calculates the overlaps for geographies. When executed, the scheduled job triggers events to calculate the overlap between two geographies.|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

## Field Service Territory Planning console properties

Territory Planning console uses the following properties.

You can find these properties by clicking **Field Service** &gt; **Territory Planning** &gt; **Properties**.

<table id="table_kkv_np2_stb"><thead><tr><th>

Properties

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

sn\_fsm\_tp.territory\_membership\_override\_to\_date

</td><td>

Determines agent's default till date field when added to territory using the **Suggested agents** tab. Agents are available in the territory till the specified date.

</td></tr><tr><td>

sn\_fsm\_tp.territory\_max\_zoom\_level

</td><td>

Sets the maximum auto-zoom level for the map. The valid values are between 1–20.-   **Type**: Integer
-   **Default value**: 12

</td></tr><tr><td>

sn\_fsm\_tp.overlay\_markers\_type

</td><td>

Determines to display the data such as agents and crews based on the view port or territory. -   **Type**: Choice list
-   **Default value**: Viewport

</td></tr><tr><td>

sn\_fsm\_tp.territory\_initial\_zoom

</td><td>

Sets the initial zoom level for the map.-   **Type**: Integer
-   **Default value**: 3

</td></tr><tr><td>

sn\_fsm\_tp.territory\_transparency\_level

</td><td>

Determines how opaque a newly created geographic area looks on the map. -   **Type**: Integer
-   **Default value**: 1

</td></tr><tr><td>

sn\_fsm\_tp.territory\_map\_type

</td><td>

Uses different types of map views to visualize territories, such as roadmap, satellite, hybrid, and terrain.-   **Type**: choice list
-   **Default value**: roadmap

</td></tr><tr><td>

sn\_fsm\_tp.max\_territories\_for\_scheduling

</td><td>

Determines the maximum number of territories that are ready for scheduling work order tasks.-   **Type**: Integer
-   **Default value**: 100

</td></tr><tr><td>

Opacity level for heatmap on the map

</td><td>

Determines the opactiy of the heatmap. Valid values are between 0.0 and 1.0.-   **Type**: Integer
-   **Default value**: 0.6

</td></tr><tr><td>

Radius of influence of data points in heatmap

</td><td>

Determines the radius that influence the data point in the heatmap. -   **Type**: Integer
-   **Default value**: 20 \(pixels\)

</td></tr></tbody>
</table>