---
title: Create a custom list in the Lists view in Service Graph Workspace
description: Create your own lists of classes that you can then navigate in the Lists view in Service Graph Workspace to explore data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a custom list in the Lists view in Service Graph Workspace

Create your own lists of classes that you can then navigate in the Lists view in Service Graph Workspace to explore data.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Graph Workspace** and then in the navigation panel, select the Lists icon.

2.  In Lists view, select the My lists tab and then select **Create new list**.

3.  Fill out the fields in the New List dialog box.

    Select either of the following tabs and then fill out the fields that appear. Drop-down selections are limited to what you have access to:

    -   Start from existing: Create another version of an existing list.
    -   Create your own: Create a new list that is based on an existing table.
    |Field|Description|
    |-----|-----------|
    |Name the new list|Display name for the new list.|
    |Select a list|Select an existing list, that the new list will be based on.|
    |Select a source|System table that you want to use for your custom list.The system only displays tables that your role has access to. After you select a list, additional fields are displayed on the pop-up.|
    |Select columns|Columns that are picked from the selected system table to be included in the new custom list. Select an empty space in the field to open the list of values that you can choose from. Options are based on the table in **Select a source** and some columns might be preselected based on the selected list.|
    |Add Filters|Condition builder to create filters for the data included and how data should be sorted.|

4.  Select **Create**.


