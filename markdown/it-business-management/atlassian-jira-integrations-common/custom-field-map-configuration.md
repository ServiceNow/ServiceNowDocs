---
title: Customize your field map configuration
description: Map a field of your preference for a Jira project.Understand how to configure a reference field while creating a new field map configuration.
locale: en-US
release: yokohama
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Customize your field map configuration

Map a field of your preference for a Jira project.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md).
-   Role required: sn\_jira\_int.user

## About this task

If you have a custom field for a Jira project that you want to map with a field in Agile Development 2.0, you can create custom field map configuration that would apply only to this Jira project.

If you have a custom field that is applicable to all Jira projects of a specific project type, see [Apply custom map configuration to multiple Jira projects](apply-custom-field-map-to-all-jira-projects.md).The following field types are supported for custom field map configuration:

-   Number
-   Select
-   Text
-   Date
-   Identity
-   Date time
-   Reference
-   List

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  From the Jira Projects related list, open a Jira project for which you want to customize the map configuration.

4.  From the Table Maps related list, open the Sprint, Epic, or Story record to add a new field map configuration for that record.

5.  From the Field Maps related list, click **New**.

6.  On the form, fill in the fields.

<table id="table_s3l_xlt_bkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal Field

</td><td>

Field name in Agile Development 2.0.

</td></tr><tr><td>

Table Map

</td><td>

Table map in Agile Development 2.0, in which this field is created. This field is auto-populated based on the table map record you select.

</td></tr><tr><td>

Internal Table

</td><td>

Table in Agile Development 2.0. This field is auto-populated based on the table map record you select.

</td></tr><tr><td>

External Field

</td><td>

Field ID in Jira.

</td></tr><tr><td>

External Field Name

</td><td>

Display name of the field in Jira. Ensure that this field is added to the Jira project screen.

</td></tr></tbody>
</table>7.  Click **Update**.


## What to do next

1.  Validate your field map configuration by clicking **Validate and fix mapping** from your project form.
2.  From the Table maps related list of your project, navigate to your new field map configuration. If the Valid column of your configuration shows:
    -   true, validation of your map configuration is successful.
    -   false, validation of your map configuration failed. Ensure that you enter the correct values for all fields and validate again.

        **Important:** If your custom map configuration is invalid or if the custom field configured is not added to the default screen scheme of the issue, the export action does not work.


**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

## Configuring a reference field in Jira

Understand how to configure a reference field while creating a new field map configuration.

When you select a reference field for the **Internal Field** field, you must select a value for the **Lookup Column Name** field. The value from the **Lookup Column Name** field is used during the import and export of work items between Jira DevOps and Agile Development 2.0.

During import, the integration application searches for the record in the reference table using the **Lookup Column Name** field. If the record is not found, the value in the work item will be empty in Agile Development 2.0.

