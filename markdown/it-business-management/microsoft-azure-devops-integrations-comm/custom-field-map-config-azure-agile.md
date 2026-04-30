---
title: Customize your field map configuration
description: Create a custom field map configuration to map a field in an Agile Development 2.0 table for Azure DevOps projects of a process type.Understand how to configure a reference field while creating a new field map configuration.
locale: en-US
release: xanadu
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Customize your field map configuration

Create a custom field map configuration to map a field in an Agile Development 2.0 table for Azure DevOps projects of a process type.

## Before you begin

-   [Discover and import Azure DevOps projects](discover-import-azure-projects.md).
-   Role required: sn\_ado\_int.user

## About this task

The following field types are supported for custom field map configuration:

-   Number
-   Select
-   Text
-   Date
-   Identity
-   Date time
-   Reference
-   List

## Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  From the Process Mapping related list, open a process map for which you want to customize the map configuration.

4.  From the Table maps related list, open a record to create a field map configuration for that table map.

5.  From the Field Maps relates list, click **New**.

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

Lookup Column Name

</td><td>

This field is required when you select a reference field as the internal field.

 For more information, see [Configuring a reference field in Azure DevOps](custom-field-map-config-azure-agile.md#).

</td></tr><tr><td>

Table Map

</td><td>

Table map in Agile Development 2.0, in which this field is created. This field is auto-populated based on the table map record you select.

</td></tr><tr><td>

External Field

</td><td>

Field ID in Azure DevOps.

</td></tr><tr><td>

External Field Name

</td><td>

Display name of the field in Azure DevOps.

</td></tr></tbody>
</table>7.  Click **Submit**.


## What to do next

1.  Validate your new table map configuration by clicking **Validate and fix mapping** from your process map form.
2.  From the Table maps related list, navigate to your new field map configuration. If the Valid column of your configuration shows:
    -   true, validation of your map configuration is successful.
    -   false, validation of your map configuration failed. Ensure that you enter the correct values for all fields and validate again.

**Important:** If your custom map configuration is invalid or if the required fields are not mapped for that work item, the export and import action does not work.

**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

## Configuring a reference field in Azure DevOps

Understand how to configure a reference field while creating a new field map configuration.

When you select a reference field for the **Internal Field** field, you must select a value for the **Lookup Column Name** field. The value from the **Lookup Column Name** field is used during the import and export of work items between Azure DevOps and Agile Development 2.0.

During import, the integration application searches for the record in the reference table using the **Lookup Column Name** field. If the record is not found, the value in the work item will be empty in Agile Development 2.0.

![Lookup column name field.](../image/lookup-column-name.png)

