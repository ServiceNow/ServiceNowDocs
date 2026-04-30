---
title: Projects landing page
description: From the projects landing page for Process Mining, you can access generated projects, business process insights, and the Analyst Workbench.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Process Mining workspace, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Projects landing page

From the projects landing page for Process Mining, you can access generated projects, business process insights, and the Analyst Workbench.

The projects landing page shows project cards for projects that have been created by or shared with you for viewing. A project that has been created but not yet generated shows a warning icon ![warning icon](../image/warning-icon.png) next to its grayed out title. The warning indicates that the project isn’t available to view.

![Projects landing page](../image/landing-page2.png "Projects landing page")

Project cards show overview details of mined projects. You can filter them by table, created by, project, activity definition, name, or short description.

|Field|Description|
|-----|-----------|
|Project name|The name of the project. You can select a project name to open the Analyst Workbench and access business findings.|
|Status|Designation of usage status of the project.|
|Short description of the project.|Brief description provided about the project.|
|Created by|The user who created the project.|
|Tables|The selected table the project reports on.|
|Last mined|When the project's data was last mined, in days.|
|\# of records|The number of records that apply to the selected data table and filter configurations for the project.|
|Process Variation|The percentage profile of uncertainty in process steps. Example: Users taking multiple routes versus the ideal path to a goal. The percentage is calculated by the number of variants divided by the number of records.|
|Average Duration|The average time across all closed filtered records from the time of their being opened to being closed.|

From a project card, relevant user roles can perform the following tasks by selecting a card's menu.

![Project card menu](../image/project-card.png)

|Menu item|Description|
|---------|-----------|
|Open|Select to open a project.|
|Edit|Select to edit a project.|
|Copy|Select to copy the configuration and create a project definition.|
|Mine Project \(Sample\)|Mines a sample project using limited data instead of performing a full data extraction.|
|Mine Project \(Full\)|Mines a full data extraction for a project.|
|Delete|Deletes a project.|

**Parent Topic:**[Process Mining workspace](analyst-workbench-overview.md)

