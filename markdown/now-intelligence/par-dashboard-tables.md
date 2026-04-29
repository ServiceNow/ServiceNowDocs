---
title: Platform Analytics dashboard tables
description: The following tables relate to Platform Analytics dashboards and can be accessed through scripts.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics dashboard tables

The following tables relate to Platform Analytics dashboards and can be accessed through scripts.

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

**Parent Topic:**[Dashboard reference](../concept/dashboard-reference-page.md)

