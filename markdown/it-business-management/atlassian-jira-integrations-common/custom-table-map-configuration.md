---
title: Customize your table map configuration
description: Map a Agile Development 2.0 table of your preference for a Jira project.
locale: en-US
release: xanadu
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Customize your table map configuration

Map a Agile Development 2.0 table of your preference for a Jira project.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md).
-   Role required: sn\_jira\_int.user

## About this task

Create a custom table map of your preference for your Jira project and configure its fields.

If you have a custom table that is applicable to all Jira projects of a specific project type, see [Apply custom map configuration to multiple Jira projects](apply-custom-field-map-to-all-jira-projects.md).

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  From the Jira Projects related list, open a Jira project for which you want to customize the map configuration.

4.  From the Table maps related list of the Jira project, click **New**.

5.  On the form, fill in the fields.

<table id="table_s3l_xlt_bkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal Table

</td><td>

Table name in Agile Development 2.0.

</td></tr><tr><td>

Map configuration

</td><td>

Map configuration for this project.This field is auto-populated based on the project.

</td></tr><tr><td>

External Table

</td><td>

Table ID in Jira.

</td></tr><tr><td>

External Table Name

</td><td>

Display name of the table in Jira.

</td></tr></tbody>
</table>6.  Save the table configuration.

7.  From the Field Maps related list of your table map record, create new field maps for the following fields:

    |Field in Jira|Field in Agile Development 2.0|
    |-------------|------------------------------|
    |Summary of the issue|Short description|
    |Description of the issue|Description|

    For information on how to configure field mapping for a table, see [Customize your field map configuration](custom-field-map-configuration.md#). You can also create other field maps for your new table configuration.


## What to do next

1.  Validate your new table map configuration by clicking **Validate and fix mapping** from your project form.
2.  In the Table maps related list of your project, if the Valid column of your configuration shows:
    -   true, validation of your map configuration is successful.
    -   false, validation of your map configuration failed. Ensure that you enter correct values for all the fields and validate again.
3.  Create a business rule to support export of this new table map configuration to Jira. See [Create a business rule to apply a custom Agile Development 2.0 table map configuration](jira-create-business-rule-to-apply-custom-table-map.md).
4.  If you want to support import and export of attachments for this new table map, see [Allow import and export of attachments on a custom Agile Development 2.0 table](jira-allow-import-and-export-of-attachments-on-custom-table-maps.md).
5.  If you want to enable display of fields that reference Jira identifiers in your custom table map, see [Populate Jira project identifier reference fields for Agile Development 2.0 custom table](jira-populate-external-identifier-reference-fields-on-a-custom-table.md).

**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

