---
title: Lists
description: Learn about how Workspace lists function with Configurable Workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Lists

Learn about how Workspace lists function with Configurable Workspace.

The list view displays filtered lists of records, such as All tasks, Open tasks, and My tasks. By setting up list categories and filtered lists, you help your agents quickly find the records they need to work on. Configure your Workspace lists setups in Configurable Workspace.

## List Menu Configuration

The Menu Configuration is a container that houses the default configurations of the list menu which consists of categories and filters.

|Legacy table name|UIB table name|
|-----------------|--------------|
|No corresponding table|sys\_ux\_list\_menu\_config|

The List Menu setup is added by default to Configurable Workspace. Associate your list and list categories with this configuration.

## List categories

List categories enable you to group records so that agents can find the records they need to work on.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_list\_category|sys\_ux\_list\_category|

List category data lives in a new UIB table. For more information about setting up list categories, see List categories.

## Filtered lists

Filtered lists enable you to group records that help agents do their work more efficiently.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_list|sys\_ux\_list|

List filter data lives in a new UIB table. For more information about setting up list filters, see List filters.

**Note:** Roles and groups are defined in the UIB table and are not applicable.

## Role and Access

Roles and access enable you to define the audience of each of the lists defined in the list filters.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_list|sys\_ux\_applicability\_m2m\_list|

To migrate roles and access, select a filtered list and choose the audience.

