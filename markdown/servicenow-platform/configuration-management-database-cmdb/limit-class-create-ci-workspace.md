---
title: Limit the class list for new CIs created in a workspace
description: Limit the selection of classes for a new CI being manually created in your workspace, to only those classes that are relevant to that workspace. When then creating a new CI in the respective workspace, users can only select a class that is authorized as an option.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Limit the class list for new CIs created in a workspace

Limit the selection of classes for a new CI being manually created in your workspace, to only those classes that are relevant to that workspace. When then creating a new CI in the respective workspace, users can only select a class that is authorized as an option.

## About this task

Creating a new CI is an experience in CMDB Workspace which you might be integrating into another workspace. Within CMDB Workspace, there are default settings for some of the behaviors of the create CI experience. However, you can use configuration identifiers to customize some of those default settings for CMDB Workspace or other workspaces. For example, you can customize the list of classes to choose from, for the new CI.

By default, when creating a new CI in CMDB Workspace, the list of classes to choose from for the new CI, contains almost all classes in the CMDB hierarchy. For your workspace, it might be important to reduce that list to specific classes or hierarchy branches.

Settings for specific classes available for new CIs are stored in the CI class config \[sn\_cmdb\_ws\_ci\_class\_config\] table which is part of the configuration identifiers framework. Therefore, to manage the list of classes for new CIs in your workspace, you must use config identifiers. To manage that list, you must create a config identifier for each class or hierarchy branch that you want to include or exclude in the class drop-down list. By default, the CI class config table contains a single entry for the Configuration Item \[cmdb\_ci\] class, which is derived by the entire CMDB hierarchy. Any class or workspace without direct config identifiers for inclusion or exclusion, uses the default entry.

For more information:

-   About configuration identifiers, see [Configuration identifiers framework](../concept/configuration-identifiers-framework.md).
-   About the experience of manually creating a new CI in CMDB Workspace, see [Create a CI manually in CMDB Workspace](create-ci-manual-cmdb-workspace.md).

## Before you begin

Role required: sn\_cmdb\_ws.config\_editor

## Procedure

1.  Navigate to **All** and in the navigation filter, enter `sn_cmdb_ws_ci_class_config.list` to access the CI class config table.

2.  On the table list view page, select **New** and fill out the form.

<table id="table_vzb_p4f_pdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Config identifier

</td><td>

Name of a configuration identifier from the Config identifier \[sn\_cmdb\_ws\_config\_identifier\] table.

 The default value of 'Default' is used as a fallback for any workspace without its own config identifiers.

</td></tr><tr><td>

CI class

</td><td>

Class to be included or excluded from the list of classes available for a new CI.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the setting in the experience of creating a new CI.

</td></tr><tr><td>

Feature

</td><td>

Pre-set to 'Create CI'.

</td></tr><tr><td>

Apply to hierarchy

</td><td>

Apply the class setting to all classes descending from the specified **CI class**.

</td></tr><tr><td>

Operation

</td><td>

Include or exclude the **CI class** in the list of classes for a new CI.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Result

When manually creating a new CI in the respective workspace, the specified **CI class** is included in the **Class** drop-down list on the Select class page only if it is set to be available.

**Parent Topic:**[Configuring CMDB Workspace](../concept/configuring-cmdb-workspace.md)

