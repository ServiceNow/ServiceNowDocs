---
title: Create or modify map indicators
description: Dependency Views maps and application service maps, use icons to display additional information for a CI by displaying its related records such as alerts, outages, incidents and problems. These icons are called map indicator.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or modify map indicators

Dependency Views maps and application service maps, use icons to display additional information for a CI by displaying its related records such as alerts, outages, incidents and problems. These icons are called map indicator.

## Before you begin

Role required: admin

## About this task

The default configuration includes map indicators for the following record types:

-   Open incident.
-   Open alert.
-   Unplanned current outage.
-   Planned current outage, or an open problem.
-   Current, planned, or recent change request.

You can filter out the display of affected CIs, alerts, current change requests, incidents and problems from the map settings menu.

The Affected CI’s map indicator appears for CIs in two related but not identical situations. It appears for CIs for which tasks such as change request, incident, or problem were directly created for, and for any CIs that were added in those tasks \(parent tasks\) as Affected CIs \(The CI for which a task is directly created for, is automatically added as an affected CI in that task\). The state of affected CI’s depends on the status of the respective parent task. For as long as the parent task is active, the associated affected CIs continue to be impacted by the task issue. In a map, the Affected CI’s indicator displays for all affected CIs for as long as the parent task is active. On a map, the Affected CI tooltip displays the details of the task records in which the CI was added as an affected CI. However, the **Details** pane does not contain an Affected CI’s tab, and no further details about affected CIs, or the associated tasks are displayed. After the parent task is closed, the Affected CI’s indicator no longer displays for any of the tasks’ affected CIs. For information about affected CIs in Change Management, see [Associate CIs to a change request](https://www.servicenow.com/docs/access?context=c_AffectedCIsAndImpactedServices&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

**Note:** Details about affected CIs are derived from the **task** and the **cmdb\_ci** tables and their extensions. Therefore, if you use custom tables to store CIs for incidents, problems and changes, it affects the details that are displayed for affected CIs.

For more information on how map indicators are used to show tasks and outages in clusters and collapsed nodes, see [Cluster nodes in a Dependency Views map](../concept/c_CollapsedNodesInNGBSM.md).

## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **Map Indicators**.

2.  Click **New** to create a new map indicator, or click the name of an indicator from the **Table** column to modify an existing map indicator.

3.  Fill in the fields on the form, as appropriate.

<table id="table_rvd_wct_dr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table represented by this map indicator. **Note:** The list shows only tables and database views that are in the same scope as the map indicator. Views are not supported, although included in the list.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Order

</td><td>

Priority order of the task. The highest priority task is the indicator with the lowest order number.

</td></tr><tr><td>

Icon

</td><td>

File name and path of the icon image file, which can be a system image.-   To create a new icon, see [Create or modify map icons](t_CreateModifyNGBSMMapIcons.md)
-   To create or use a system image see [Storing images in the database](https://www.servicenow.com/docs/access?context=c_StoringImagesInTheDatabase&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


</td></tr><tr><td>

CMDB CI field

</td><td>

Name of the field on the selected table that contains the configuration item.

</td></tr><tr><td>

Start field

</td><td>

Record property that determines the time-point on the metric chart timeline for placing records in the Insights Explorer.Possible values depend on the selected **Table**. For example, the incident indicator has values such as **Actual end**, **Actual Start**, and **Approval Set**.

</td></tr><tr><td>

Description field

</td><td>

Name of the field on the selected table that contains the description of the configuration item.

</td></tr><tr><td>

Description

</td><td>

Text to display when hovering over the indicator. Alphanumeric characters and spaces are valid for this field.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder that specifies for which CIs to apply this indicator. For example, a CI that has a current past outage is highlighted for 5 days. You can configure a condition to designate a different timeframe for what is considered to be current.

</td></tr><tr><td>

Active in Service Map

</td><td>

Toggle that you can enable to make the specified table available in the Settings dialog box for application service maps. You can then toggle between displaying or not displaying the respective records on the map.

</td></tr><tr><td>

Active Dependencies

</td><td>

Toggle that you can enable to make the specified table available in the Settings dialog box for Dependency Views maps. You can then toggle between displaying or not displaying the respective records on the map.

</td></tr><tr><td>

Active in Metrics

</td><td>

Enable to make the toggle for the specified table available in the Settings dialog box for the Insights Explorer. You can then toggle between displaying or not displaying the respective records on the Insights Explorer.

</td></tr><tr><td>

Label

</td><td>

Text to display for the indicator on the map.

</td></tr><tr><td>

Tooltip Label

</td><td>

Prefix portion of the tooltip \(Tooltip Label : Tooltip info\).

</td></tr><tr><td>

Tooltip Info

</td><td>

Suffix portion of the tooltip \(Tooltip Label : Tooltip info\).

</td></tr></tbody>
</table>4.  Click **Submit** to enter a new map indicator or click **Update** to modify an existing map indicator.


## Result

For an indicator to appear in a Dependency Views map, a CI must meet all filter conditions, and **Active Dependencies** must be selected.

**Parent Topic:**[Administer Dependency Views](../topic/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map icons](t_CreateModifyNGBSMMapIcons.md)

[Create a predefined filter](create-predefined-filter.md)

[Set a predefined filter as default](set-predefined-filter-default.md)

[Create or modify Map Related Items](t_CreateModifyNGBSMMapRelatedItems.md)

[Create or modify Dependency Views menu actions](t_CreateModifyNGBSMMenuActions.md)

[Condition and script parameters for menu actions](../reference/condition-script-parameters.md)

[Create or edit a dependency type](t_CreateMapScript.md)

