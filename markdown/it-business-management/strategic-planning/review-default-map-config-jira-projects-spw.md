---
title: Review default mapping configuration for Jira projects in SPW
description: Verify that the default mapping configuration between work items in Strategic Planning Workspace \(SPW\) and Jira aligns with your team's processes.
locale: en-US
release: yokohama
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Configure Jira project settings, Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Review default mapping configuration for Jira projects in SPW

Verify that the default mapping configuration between work items in Strategic Planning Workspace \(SPW\) and Jira aligns with your team's processes.

## Before you begin

[Import Jira projects to SPW](imports-jira-projects-to-spw.md)

Role required: sn\_jira\_int.user

## About this task

Review the predefined table, field, and choice mapping configuration for a Jira Project. For more information on the default configuration for Epics, Stories, and Sprints, see [Default mapping configuration for SPW Jira Integrations](../reference/default-mapping-configuration-spw-jira.md).

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Jira Integration** &gt; **Jira Projects**.

2.  Open your Jira project record.

3.  From the Table Maps related list, review the list of mappings available between tables of Jira and SPW for this project.

4.  Review the field mapping for each table map.

    1.  Select a table mapping record to open it.

    2.  From the Field Maps related list, review the mapping configuration of the fields between the tables.

5.  Review the choice mapping for a field such as the State field.

    1.  Select a field mapping record to open it.

    2.  From the Choice Maps related list, review the mapping configuration of choices of the fields.

6.  Repeat steps 3, 4, and 5 for all table maps of the Project.


## What to do next

If the available mapping configuration doesn't fit your team's requirements or processes, you can create custom mappings between entities of Jira and SPW. For more information, see [Custom mapping configuration for SPW Jira Integrations](../concept/custom-mapping-configuration-spw-jira.md#).

