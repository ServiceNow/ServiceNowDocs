---
title: Platform Analytics tables
description: The following tables relate to Platform Analytics data visualizations and dashboards and can be accessed through scripts.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics tables

The following tables relate to Platform Analytics data visualizations and dashboards and can be accessed through scripts.

## Data visualization tables

|Table|Description|
|-----|-----------|
|analytics\_visualization|Parent table for all sys\_report\* and par\_visualization\* tables. This table holds all fields common to both Platform Analytics data visualizations and Core UI reports.|
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
|report\_stats|Contains usage information for migrated reports and data visualizations including run times, most recent view time, and the number of recent executions.|

## Dashboard tables

|Table|Description|
|-----|-----------|
|analytics\_dashboard|Parent table for all par\_dashboard\* and pa\_dashboard\* tables. This table holds all fields common to both Platform Analytics and Core UI dashboards.|
|par\_automated\_kpi\_promin\_project|Stores references to Process Mining maps that are on Platform Analytics dashboards.|
|par\_computed\_insight|Contains all standard proactive analytics insights|
|par\_custom\_insight\_content|Contains all custom-built proactive analytics insights|
|par\_dashboard|Contains all dashboards in the dashboard library. Technical dashboards can be identified by belonging to the Advanced Dashboards experience. Extends sys\_metadata.|
|par\_dashboard\_cache|Stores all changes to Platform Analytics dashboard layouts.|
|par\_dashboard\_canvas|Stores the names, descriptions, and layouts of Platform Analytics dashboards and dashboard tabs. Extends sys\_metadata.|
|par\_dashboard\_config|Contains the macroponent definitions for each type of data visualization that you can create inside a dashboard. Extends sys\_metadata.|
|par\_dashboard\_filter|Lists all filters on Platform Analytics dashboards and the name of the dashboard.|
|par\_dashboard\_permission|Contains the role, group, and user permissions for all dashboards in the dashboard library. Extends sys\_metadata.|
|par\_dashboard\_tab|Contains the name, domain, application scope, and parent dashboard of all Platform Analytics dashboard tabs. Extends sys\_metadata.|
|par\_dashboard\_user\_metadata|Contains all options set by a dashboard viewer that persist between that viewer's user sessions. Extends sys\_metadata.|
|par\_dashboard\_visibility|Cross-references all dashboards in the library by which experiences and workspaces contain them. Extends sys\_metadata.|
|par\_dashboard\_widget|Cross-references all components that appear on dashboards by the dashboard canvas and the library component, if any. Extends sys\_metadata.|
|par\_dashboard\_widget\_group|Contains the configuration for a set of grouped widgets including name, coordinates, and color properties for border and background.|
|par\_dashboard\_widget\_group\_mapping|Contains a mapping of elements in a widget group to those elements. Group this table by Elements Group to see the widgets in each group clearly.|
|par\_export|Lists all scheduled dashboard and data visualization exports.|
|par\_export\_dashboard|Stores the export details of all scheduled dashboard exports. Extends par\_export.|
|par\_export\_job|Stores details of every attempt to export a dashboard or data visualization.|
|par\_indicator\_model|Contains recommendations related to Performance Analytics analytics in proactive analytics insights.|
|par\_insight\_user\_actions|Stores actions that viewers took on proactive analytics insights.|
|par\_notification|Lists email notification definitions of scheduled dashboard and data visualization exports.|
|par\_notification\_email|Stores subject line and message body of scheduled dashboard and data visualization export emails. Extends par\_notification.|
|par\_notification\_email\_recipients|Stores groups and users who receive a notification email with a scheduled dashboard and data visualization export.|
|par\_recommendation|Stores recommendations of Process Mining projects to create. These recommendations are given through Process Mining insights.|
|par\_recommendation\_user\_action|Stores whether users accepted or dismissed a Process Mining insight recommendation.|

## Library recommendation tables

<table id="table_fwc_dcc_h3c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analytics Library Scan Items

 \[analytics\_library\_scan\_item\]

</td><td>

Stores the results of the scheduled library management jobs

</td></tr><tr><td>

Analytics Library Scan Executions

 \[analytics\_library\_scan\_execution\]

</td><td>

Stores the logs of the scheduled library management jobs

</td></tr></tbody>
</table>**Parent Topic:**[Platform Analytics experience reference](../concept/platform-analytics-exp-reference.md)

