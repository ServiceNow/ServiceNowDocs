---
title: Installed with Change Management - Change Schedule
description: Several types of components are installed with the Change Management - Change Schedule.Plugins are added with activation of Change Management - Change Schedule.Roles are added with activation of Change Management - Change Schedule.Tables are added with activation of Change Management - Change Schedule.Properties are added with activation of Change Management - Change Schedule.Business rules are added with activation of Change Management - Change Schedule.UI policies are added with activation of Change Management - Change Schedule.Script includes are added with activation of Change Management - Change Schedule.UI scripts are added with activation of Change Management - Change Schedule.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Activate Change Management - Change Schedule, Change Management plugins, Configure, Change Management, IT Service Management]
---

# Installed with Change Management - Change Schedule

Several types of components are installed with the Change Management - Change Schedule.

**Parent Topic:**[Activate Change Management - Change Schedule](../task/activate-changemgmt-changeschedule.md)

## Plugins installed with Change Management - Change Schedule

Plugins are added with activation of Change Management - Change Schedule.

|Plugin|ID|Description|
|------|---|-----------|
|Change Management - Change Schedule|com.snc.change\_management.soc|This plugin is the core Change Schedules plugin which includes the supporting Change Schedules table structure, landing page, and Change Schedules user interface.|
|Change Management - Change Schedule foundation|com.snc.change\_management.soc.foundation|This plugin contains six change schedules to help users. Enabling this plugin automatically enables Change Management – Change Schedules Version 1.0.0.|

## Roles installed with Change Management - Change Schedule

Roles are added with activation of Change Management - Change Schedule.

|Role title \[name\]|Description|
|-------------------|-----------|
|\[sn\_chg\_soc.change\_soc\_admin\]|This role has full administrative rights to Change Schedule pages.|

## Tables installed with Change Management - Change Schedule

Tables are added with activation of Change Management - Change Schedule.

Change Management - Change Schedule adds the following tables.

<table id="table_id2_fgd_3db"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Style Rule\[chg\_soc\_style\_rule\]

</td><td>

Define a default style rule that is applied to all Change Schedule definitions for each Change record displayed on the page

</td></tr><tr><td>

Style Rule\[chg\_soc\_definition\_style\_rule\]

</td><td>

Define a style rule for each Change record displayed on the Change Schedule page

</td></tr><tr><td>

Style Rule\[chg\_soc\_def\_child\_style\_rule\]

</td><td>

Define a style rule for each related record displayed on the Change Schedule page

</td></tr><tr><td>

Change Schedule Definition\[chg\_soc\_definition\]

</td><td>

Define a Change Schedule page

</td></tr><tr><td>

Change Schedule Definition Core \[chg\_soc\_definition\_child\]

</td><td>

Define related records for each Change record that is presented on the Change Schedule page

</td></tr></tbody>
</table>## Properties installed with Change Management - Change Schedule

Properties are added with activation of Change Management - Change Schedule.

Change schedules are loaded on the timeline page on the client side in batches of 20. You can load a maximum of 1000 records. These numbers can be modified using the following properties from the System Properties \[sys\_properties\] table. To open the System Property table, enter `sys_properties.list` in the navigation filter.

<table id="table_gmc_1gd_3db"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

sn\_chg\_soc.change\_soc\_initial\_limit

</td><td>

Define the number of change\_request records to display on load of the Change Schedule.-   **Type**: Integer
-   **Default value**: 40
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_chg\_soc.change\_soc\_scroll\_load\_limit

</td><td>

Define the number of change\_request records to display as the Change Schedule is scrolled.-   **Type**: Integer
-   **Default value**: 20
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_chg\_soc.change\_soc\_total\_limit

</td><td>

Define the total number of change\_request records that can be displayed on a Change Schedule.-   **Type**: Integer
-   **Default value**: 1000
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_chg\_soc.landing\_page.pinned\_notification

</td><td>

Show a message when pin or unpin a change schedule. -   **Type**: String
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_chg\_soc.schedule\_window\_days

</td><td>

Define the number of days to be factored before and after the respective start/end of a change\_request record when displaying blackout and maintenance window spans on the Change Schedule page.-   **Type**: Integer
-   **Default value**: 30
-   **Location**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Business rules installed with Change Management - Change Schedule

Business rules are added with activation of Change Management - Change Schedule.

<table id="table_u2s_mzv_mdb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create default style rule

</td><td>

Related Definition\[chg\_soc\_definition\_child\]

</td><td>

Defines a standard style rule with a high order for the related records.

</td></tr><tr><td>

Different start and end fields

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

Ensures that the start and end fields are different by aborting an insert or save when this is the case.

</td></tr><tr><td>

Flush share lists when ShareWith is none

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

Empties shared with lists when share with none is set.

</td></tr><tr><td>

Flush shareWith to match empty lists

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

Ensures shared with is updated to reflect the selected share options such as groups, roles, users.

</td></tr><tr><td>

Update style field

</td><td>

Style Rule Core\[chg\_soc\_style\_rule\_core\]

</td><td>

Updates the stylesheet defined in the style field when one of the conditions is met: -   Label color changes
-   Label weight changes
-   Event color changes

Providing Advanced is not true.

</td></tr></tbody>
</table>## UI policies installed with Change Management - Change Schedule

UI policies are added with activation of Change Management - Change Schedule.

<table id="table_ghl_vf4_mdb"><thead><tr><th>

UI Policy

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show maintenance color

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

Only show the maintenance color field if Show maintenance has been enabled.

</td></tr><tr><td>

Switch between Basic and Advanced

</td><td>

Style Rule Core \[chg\_soc\_style\_rule\_core\]

</td><td>

Only show label and event options if the style rule advanced option is false. When advanced is specified only the style field is presented.

</td></tr><tr><td>

Hide share users, groups and roles if share with everyone

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

If sharing with everyone then the other share options are hidden.

</td></tr><tr><td>

Show blackout color

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

Only show the Blackout color field if Show blackout has been enabled.

</td></tr><tr><td>

Hide table name

</td><td>

Style Rule Core\[chg\_soc\_style\_rule\_core\]

</td><td>

Condition builder requires a table field to be present on the form, but it is not necessary to present this so it is hidden.

</td></tr><tr><td>

Hide table name

</td><td>

Change Schedule Definition \[chg\_soc\_definition\]

</td><td>

Condition builder requires a table field to be present on the form, but it is not necessary to present this so it is hidden.

</td></tr></tbody>
</table>## Script includes installed with Change Management - Change Schedule

Script includes are added with activation of Change Management - Change Schedule.

|Script include|Description|
|--------------|-----------|
|SoC|Base class that provides utilities and constants for Change Schedules|
|SoCChangeRequest|Extends SoCChangeRequestSNC and can be used to overwrite functionality defined therein|
|SoCChangeRequestSNC|Provides utilities for the change\_request table|
|SoCDefinition|Extends SoCDefinitionSNC and can be used to overwrite functionality defined therein|
|SoCDefinitionSNC|Provides utilities for the chg\_soc\_definition table|
|SoCDefinitionChild|Extends SoCDefinitionChildSNC and can be used to overwrite functionality defined therein|
|SoCDefinitionChildSNC|Provides utilities for the chg\_soc\_child\_def table|
|SoCDefinitionChildStyleRule|Extends SoCDefinitionChildStyleRuleSNC and can be used to overwrite functionality defined therein|
|SoCDefinitionChildStyleRuleSNC|Provides utilities for the chg\_soc\_def\_child\_style\_rule table|
|SoCDefinitionStyleRule|Extends SoCDefinitionStyleRuleSNC and can be used to overwrite functionality defined therein|
|SoCDefinitionStyleRuleSNC|Provides utilities for the chg\_soc\_definition\_style\_rule table|
|SoCLandingModelBuilder|Extends SoCLandingModelBuilderSNC and can be used to overwrite functionality defined therein|
|SoCLandingModelBuilderSNC|Builds the change schedule definition model used by the Change Schedule landing page|
|SoCModelBuilder|Extends SoCModelBuilderSNC and can be used to overwrite functionality defined therein|
|SoCModelBuilderSNC|Builds the change schedule model used by the change schedule page|
|SoCRefFieldsList|Field choice list processor. Return the fields on the current table which reference the parent table|
|SoCRefTablesList|Field Choice List Processor. Return the tables referencing the provided table name.|
|SoCStyleRule|Extends SoCStyleRuleSNC and can be used to overwrite functionality defined therein|
|SoCStyleRuleSNC|Provides utilities for style rules|

## UI scripts installed with Change Management - Change Schedule

UI scripts are added with activation of Change Management - Change Schedule.

|UI Scripts|Description|
|----------|-----------|
|sn\_chg\_soc.change\_soc|Angular module for the change schedule, which includes all of the angular applications dependencies|
|sn\_chg\_soc.change\_soc\_filter|Angular module for text filtering on the change schedule page|
|sn\_chg\_soc.config|Angular module for the configuration panel on the change schedule page|
|sn\_chg\_soc.context\_menu|Angular module for the context menu on the change schedule page|
|sn\_chg\_soc.data|Angular module for the data model on the change schedule page|
|sn\_chg\_soc.duration|Angular module for a duration calculation utility|
|sn\_chg\_soc.filter\_control|Angular module implementation of the filter widget|
|sn\_chg\_soc.filter\_widget|Angular module that provides a filter control similar to a condition builder|
|sn\_chg\_soc.gantt|Angular module that maintains instances of gantt objects and handles the definition of the gantt scale|
|sn\_chg\_soc.keyboard|Angular module for the keyboard panel on the change schedule page|
|sn\_chg\_soc.landing.app|Angular module for the change schedule landing page, which includes all of the angular applications dependencies|
|sn\_chg\_soc.landing\_accessibility|Angular module for acceissbility support on the change schedule landing page|
|sn\_chg\_soc.landing\_card|Angular module defines a directive for a change schedule definition card|
|sn\_chg\_soc.landing\_decoration|Angular module defines a directive that provides styling|
|sn\_chg\_soc.landing\_notifications|Angular module for displaying notifications|
|sn\_chg\_soc.landing\_page\_header|Angular module provides header for change schedule landing page|
|sn\_chg\_soc.landing\_sort|Angular module provides utility for sorting cards on the change schedule landing page|
|sn\_chg\_soc.landing\_splash\_screens|Angular module provides splash screen when no change schedule definitions are present in a tab on the change schedule landing page|
|sn\_chg\_soc.landing\_tabs|Angular module provides tabs for the change schedule landing page|
|sn\_chg\_soc.landing\_wizard|Angular module defines the creation of a new change schedule definition from the landing page|
|sn\_chg\_soc.loading|Angular module defines when the change schedule page is loading by listening to requests|
|sn\_chg\_soc.mousedown|Angular module that makes a button execute multiple times when holding mouse down|
|sn\_chg\_soc.notification|Angular module used to display messages on the change schedule page|
|sn\_chg\_soc.popover|Angular module used for accessibility support for the popover that is displayed on the change schedule page|
|sn\_chg\_soc.share|Angular module for the share panel on the change schedule page|
|sn\_chg\_soc.sn.app\_itsm.now.iscroll|Angular module that supports scrolling to load more content on the change schedule landing page|
|sn\_chg\_soc.snCreateNewInvite|Angular module for the share panel component that adds elements to the shared with field for the change schedule|
|sn\_chg\_soc.sn\_soc\_now.scheduleService|Angular module for the change schedule landing page that is used to retrieve change schedule definitions from the server|
|sn\_chg\_soc.style|Angular module for the style panel on the change schedule page|

