---
title: Platform Analytics tables
description: The following tables relate to Platform Analytics data visualizations and dashboards and can be accessed through scripts.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-16"
reading_time_minutes: 2
breadcrumb: [Reference, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics tables

The following tables relate to Platform Analytics data visualizations and dashboards and can be accessed through scripts.

## Data visualization tables

|Table|Description|
|-----|-----------|
|par\_component|Contains all data visualizations in the visualization library and all filters in the filter library. Extends sys\_metadata.|
|par\_component\_permission|Contains the role, group, and user permissions for all data visualizations and filters in their respective libraries.|
|par\_export|Lists all scheduled dashboard and data visualization exports. Extends sys\_metadata.|
|par\_export\_job|Stores details of every attempt to export a dashboard or data visualization.|
|par\_export\_visualization|Stores the export details of all scheduled data visualization exports. Extends par\_export.|
|par\_metadata|Stores the metadata for each data visualization type.|
|par\_notification|Lists email notification definitions of scheduled dashboard and data visualization exports. Extends sys\_metadata.|
|par\_notification\_email|Stores metadata of scheduled dashboard and data visualization export emails, including subject and message. Extends par\_notification.|
|par\_notification\_email\_recipients|Stores groups and users who receive a notification email with a scheduled dashboard and data visualization export. Contains the non-metadata information for the emails.|
|par\_visualization|Contains all data visualizations in the visualization library. Extends par\_component.|
|par\_visualization\_permission|Contains the role, group, and user permissions for all data visualizations in the visualization library. Extends par\_component\_permission.|

## Dashboard tables

<table id="id_wtk_hqk_rfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

par\_automated\_kpi\_promin\_project

</td><td>

Stores references to Process Mining maps that are on Platform Analytics dashboards.

</td></tr><tr><td>

par\_computed\_insight

</td><td>

Contains all standard proactive analytics insights

</td></tr><tr><td>

par\_custom\_insight\_content

</td><td>

Contains all custom-built proactive analytics insights

</td></tr><tr><td>

par\_dashboard

</td><td>

Contains all dashboards in the dashboard library. Technical dashboards can be identified by belonging to the Advanced Dashboards experience. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_cache

</td><td>

Stores all changes to Platform Analytics dashboard layouts.

</td></tr><tr><td>

par\_dashboard\_canvas

</td><td>

Stores the names, descriptions, and layouts of Platform Analytics dashboards and dashboard tabs. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_config

</td><td>

Contains the macroponent definitions for each type of data visualization that you can create inside a dashboard. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_configuration

</td><td>

Contains the macroponent definitions for each type of data visualization that you can create inside a dashboard. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_filter

</td><td>

Lists all filters on Platform Analytics dashboards and the name of the dashboard.

</td></tr><tr><td>

par\_dashboard\_permission

</td><td>

Contains the role, group, and user permissions for all dashboards in the dashboard library. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_tab

</td><td>

Contains the name, domain, application scope, and parent dashboard of all Platform Analytics dashboard tabs. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_user\_metadata

</td><td>

Contains all options set by a dashboard viewer that persist between that viewer's user sessions. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_visibility

</td><td>

Cross-references all dashboards in the library by which experiences and workspaces contain them. Extends sys\_metadata.

</td></tr><tr><td>

par\_dashboard\_widget

</td><td>

Cross-references all components that appear on dashboards by the dashboard canvas and the library component, if any. Extends sys\_metadata.

</td></tr><tr><td>

par\_export

</td><td>

Lists all scheduled dashboard and data visualization exports.

</td></tr><tr><td>

par\_export\_dashboard

</td><td>

Stores the export details of all scheduled dashboard exports. Extends par\_export.

</td></tr><tr><td>

par\_export\_job

</td><td>

Stores details of every attempt to export a dashboard or data visualization.

</td></tr><tr><td>

par\_indicator\_model

</td><td>

Contains recommendations related to Performance Analytics analytics in proactive analytics insights.

</td></tr><tr><td>

par\_insight\_user\_actions

</td><td>

Stores actions that viewers took on proactive analytics insights.

</td></tr><tr><td>

par\_notification

</td><td>

Lists email notification definitions of scheduled dashboard and data visualization exports.

</td></tr><tr><td>

par\_notification\_email

</td><td>

Stores subject line and message body of scheduled dashboard and data visualization export emails. Extends par\_notification.

</td></tr><tr><td>

par\_notification\_email\_recipients

</td><td>

Stores groups and users who receive a notification email with a scheduled dashboard and data visualization export.

</td></tr><tr><td>

par\_recommendation

</td><td>

Stores recommendations of Process Mining projects to create. These recommendations are given through Process Mining insights.

</td></tr><tr><td>

par\_recommendation\_user\_action

</td><td>

Stores whether users accepted or dismissed a Process Mining insight recommendation.

</td></tr></tbody>
</table>**Parent Topic:**[Platform Analytics experience reference](../concept/platform-analytics-exp-reference.md)

