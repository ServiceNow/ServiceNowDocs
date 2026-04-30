---
title: Facilities visualization workbench configuration
description: Space administrators configure properties on the workbench. In the application navigator, Facilities Workbench Configuration contains the configuration settings divided into sections.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Activate Facilities Visualization Workbench, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Facilities visualization workbench configuration

Space administrators configure properties on the workbench. In the application navigator, **Facilities** &gt; **Workbench Configuration** contains the configuration settings divided into sections.

## Map properties

Map properties allow some customization on the floor plan. For a full description of each property, see [Space Management properties](../../facilities-service-management/reference/SpaceMgmntProperties.md).

## Parsing configuration

Map features \[fm\_facility\_feature\] define how to handle features during processing map set files and running transforms. A basic set of Map Features are pre-loaded for your use under **Space Management** &gt; **Map Configuration** &gt; **Feature Definitions**.

To create spaces for a feature type during parsing:

-   Set **Create spaces** to true.
-   Set the default space type to specify the class of space that is created.

## Icon definition

A set of Map Icons \[fm\_icon\] is pre-loaded for your use.

-   These icon definitions affect both parsing and runtime configuration.
-   If the geoJSON property of type "point" type is found during parsing and its name matches the **Parsing name** field, then an icon is added to the map.
-   Set **Active** to true to show the icons on the map.
-   Set **Show by default** to true so the icons appear on the initial map load.

## Map colors

A set of Feature Colors \[fm\_map\_color\] is preloaded for your use.

-   The **Color** and **Outline** color fields support hex values, RGB values, and HTML colors.
-   The **Opacity** field supports decimal values from 0 to 1 to set the opacity of the feature on the map.
-   The **Outline thickness** field supports whole numbers to set the outline thickness of a feature on the map.

## Map labels

Specify which space types have labels shown by default on the interactive map. The settings section of the map lets you change the currently selected values.

-   For each facilities space type, set **show label** to true for its label to be visible on the map by default.

## Map tasks

Specify which **Tasks** to show and search on the workbench.

-   For each facilities map task, set **show task** to true for its pin to be visible on the map by default.
-   Showing tasks can be limited to specified roles \(not specifying a role shows tasks to all who can see them based on security settings\).

## Map filters

Specify filters to apply to the map, coloring spaces based on conditions specified.

-   Limit showing map filters to **Roles** or specific users with the **Owner**, **Public**, and **Roles** fields.
-   Example filters are provided as a default.

## Map menu items

Specify which catalog items are displayed in the pop-up menu on the workbench.

<table id="table_mq1_f45_pcb"><thead><tr><th>

 

</th></tr></thead><tbody><tr><td>

-   To view catalog items from **Workbench**, right-click on a space and the catalog items appear. Or, click a space and the catalog items appear under **Related Links**.

</td></tr><tr><td>

-   For each facility map menu item, select the **Roles** for which this catalog item is visible. No defined roles means that the catalog item is available to all users.

</td></tr><tr><td>

-   For each facility map menu item, select the **Order** in which this entry appears.

</td></tr><tr><td>

-   For each facility map menu item, select the **Campuses** for which this catalog item is visible. No defined campuses means that the catalog item is available on all campuses.

</td></tr></tbody>
</table>**Note:** You can show catalog items from any catalog \(Facilities, IT, HR, and others\).

## URL parameters

Workbench supports URL parameters. URL parameters provide configuration information for a form or list.

**Note:** The URL parameters are listed in order of dependency. For example, syspar\_drawingId requires sysparm\_campusSysId in the URL parameter.

The URL parameters supported are:

|URL parameters|Description|
|--------------|-----------|
|sysparm\_campusSysId|Loads the map to a Campus \[fm\_campus\] identified by its sys\_id.|
|sysparm\_drawingId|Loads the map to a Building \[alm\_building\] identified by its external\_building\_id \(requires sysparm\_campusSysId\).|
|sysparm\_levelId|Loads the map to a Level \[fm\_level\] identified by its external\_level\_id \(requires sysparm\_drawingId\).|
|sysparm\_spaceid|Loads the map to a space \[fm\_space\] identified by its external\_space\_id \(requires sysparm\_levelId\).|
|sysparm\_scenarioSysId|Loads the map to a Scenario \[enterprise\_move\_scenario\] identified by its sys\_id \(requires Facilities Move Management plugin\).|
|sysparm\_zoneSysId|Loads the map to a zone \[fm\_zone\] identified by its sys\_id. Multiple spaces make up a zone.|
|sysparm\_filterSysId|Applies a filter \[fm\_map\_filter\] for a loaded map. Filters highlight spaces based on conditions.|
|sysparm\_refreshInterval|Enter a whole number value to specify a rate in minutes to automatically refresh applied filters.|
|sysparm\_labelDisplay|Specify the label to appear for a map \(can be changed under settings on the map\).|
|sysparm\_move|Loads a move query for a map.|
|sysparm\_tab|Specify the number of the tab to default to on the map.|
|sysparm\_fromWidget|Triggers event "space.clicked" on a space click, which returns \{'sys\_id': SPACESYSID, 'displayName': SPACEDISPLAYNAME\}, or hiding space which returns \{'sys\_id':", 'displayName':"\};|

**Parent Topic:**[Activate Facilities Visualization Workbench](../task/t_ActivateFacVisWorkbench.md)

