---
title: Filter the view of a Dependency Views map
description: Filter a Dependency Views map to display specific types or categories of configuration items.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Filter the view of a Dependency Views map

Filter a Dependency Views map to display specific types or categories of configuration items.

## Before you begin

Role required: sn\_cmdb\_admin or admin

## About this task

Use the filter panel to control which elements of the map are displayed and to save versions of a filter for later use.

## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **View Map**.

2.  Click the Map settings icon ![Map Settings.](../image/dv-map-settings.png) to open map settings.

<table id="table_irc_3sy_dr"><thead><tr><th>

Filter panel strips and options

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Save Custom Settings**

</td><td>

Configure desired custom settings, then enter a name and click **Save**.Custom settings can be loaded by using the **Load Saved Custom Settings** option.

 Navigate to **Dependency Views** &gt; **Saved Settings** &gt; **** to display all saved custom settings.

</td></tr><tr><td>

**Load Custom Settings**

</td><td>

Apply previously saved custom settings to the current map.

</td></tr><tr><td>

**Predefined Filters**

</td><td>

Apply [previously defined filters](create-predefined-filter.md) consisting of configuration type, CI type, and relationship filters. You can [Set a predefined filter as default](set-predefined-filter-default.md).This filter is applied first, before any other filters \(such as **Filter CIs by Depth**\) are applied.

</td></tr><tr><td>

**Dependency Type**

</td><td>

Apply a filter that runs in real time and generates a custom view of a service map for a specific CI.

</td></tr><tr><td>

**Max Levels**

</td><td>

Designate how many levels from the root CI display on the map.

</td></tr><tr><td>

**Filter CIs by Depth**

</td><td>

Designate which levels of CI display on the map.

</td></tr><tr><td>

**Filter CIs by CI Type**

</td><td>

Designate what CI types display in the map.

</td></tr><tr><td>

**Filter CIs By CI Location**

</td><td>

Designate what CI locations display in the map.

</td></tr><tr><td>

**Filter CIs By CI Manufacturer**

</td><td>

Designate what CI manufacturers display in the map.

</td></tr><tr><td>

**Filter CIs By Audit Failure**

</td><td>

Hides CIs that failed the CMDB health staleness test. This option is available only if there are any such CIs.

</td></tr><tr><td>

**Filter Relationship Types**

</td><td>

Designate what relationship types display in the map.

</td></tr><tr><td>

**Map Indicators**

</td><td>

Designate what types of tasks display and get counted in the map.

</td></tr><tr><td>

**Remove Filtered Items**

</td><td>

**Off:** Gray out filtered items on the map. **On:** Do not display filtered items on the map.

</td></tr><tr><td>

**Run Layout Automatically**

</td><td>

**On:** The configured layout to the map is reapplied whenever the filter is changed. **Off:** The map layout remains static when the filter is changed.

</td></tr><tr><td>

**Fit to Screen Automatically**

</td><td>

**On:** The map magnification will increase or decrease automatically to display all CIs on the map. **Off:** The map magnification remains unchanged when the map is reloaded.

</td></tr></tbody>
</table>3.  Click a filter strip to expand or collapse it, and to set filter items.


**Parent Topic:**[Use Dependency Views](../topic/p_UseNGBSM.md)

**Related topics**  


[View a Dependency Views map](t_AccessNGBSM.md)

[Save or load a Dependency Views map](t_SaveLoadMapView.md)

[Delete a saved Dependency Views map view](t_DeleteSavedMapView.md)

[Change the layout of Dependency Views map](t_ChangeLayoutNGBSMMap.md)

[Perform actions on nodes in a Dependency Views map](t_PerformActionsOnNGBSMMap.md)

[Export a Dependency Views map](t_ExportAnNGBSMMap.md)

[View collapsed nodes in a Dependency Views map](t_ViewCollapsedNodesInNGBSM.md)

