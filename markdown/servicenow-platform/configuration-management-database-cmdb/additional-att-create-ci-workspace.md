---
title: Request additional attributes for new CIs
description: Integrate a request for specific CI attributes when manually creating a new CI in your workspace. Then, when creating a new CI in the respective workspace, users can enter values for the requested attributes, as appropriate for the new CI.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Request additional attributes for new CIs

Integrate a request for specific CI attributes when manually creating a new CI in your workspace. Then, when creating a new CI in the respective workspace, users can enter values for the requested attributes, as appropriate for the new CI.

## About this task

Creating a new CI is an experience in CMDB Workspace which you might be integrating into another workspace. Within CMDB Workspace, there are default settings for some of the behaviors of the create CI experience. However, you can use configuration identifiers to customize some of those default settings for CMDB Workspace or other workspaces. For example, you can customize the list of attributes that is requested for the new CI.

Requests for additional attributes for new CIs are stored in the CI additional attributes config \[sn\_cmdb\_ws\_ci\_additional\_attributes\] table which is part of the configuration identifiers framework. Therefore, to manage requests for additional attributes in your workspace, you must use config identifiers. By default, the CI additional attributes config table contains a single entry for CMDB Workspace, that applies to the entire CMDB hierarchy. Any workspace or class without a direct config identifier for additional attributes, uses the default entry.

For more information:

-   About configuration identifiers, see [Configuration identifiers framework](../concept/configuration-identifiers-framework.md).
-   About the experience of manually creating a new CI in CMDB Workspace, see [Create a CI manually in CMDB Workspace](create-ci-manual-cmdb-workspace.md).

## Before you begin

Role required: sn\_cmdb\_ws.config\_editor

## Procedure

1.  Navigate to **All** and in the navigation filter, enter `sn_cmdb_ws_ci_additional_attributes.list` to access the CI additional attributes config table.

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

Class for which the specified additional attributes will be requested when creating a new CI.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the request for the additional attributes when creating a new CI.

</td></tr><tr><td>

Additional attributes

</td><td>

List of class attributes that will be requested when creating a new CI of the **CI class**.

</td></tr><tr><td>

Apply to hierarchy

</td><td>

Apply the request for additional attributes to all classes descending from the specified **CI class**.

</td></tr><tr><td>

Feature

</td><td>

Pre-set to 'Create CI'.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Result

When manually creating a new CI for the specified **CI class** in the respective workspace, users are requested to enter values for the specified **Additional attributes** on the Additional attributes page.

**Parent Topic:**[Configuring CMDB Workspace](../concept/configuring-cmdb-workspace.md)

