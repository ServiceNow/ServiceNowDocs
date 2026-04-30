---
title: Customize your table map configuration
description: Configure table maps between tasks, iterations, and work areas of Azure DevOps and tables in Agile Development 2.0 and configure its fields for Azure DevOps projects of a process type.
locale: en-US
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Customize your table map configuration

Configure table maps between tasks, iterations, and work areas of Azure DevOps and tables in Agile Development 2.0 and configure its fields for Azure DevOps projects of a process type.

## Before you begin

-   [Discover and import Azure DevOps projects](discover-import-azure-projects.md).
-   Role required: sn\_ado\_int.user

## Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  From the Process Mapping related list, open a process map for which you want to customize the map configuration.

4.  From the Table maps related list, click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Internal Table|Name of the table in Agile Development 2.0.|
    |External Table|Table ID in Azure DevOps.|
    |External Table Name|Display name of the table in Azure DevOps.|

6.  Save the table configuration.

7.  From the Field Maps related list of your table map record, create new field maps to map the following fields.

    |Field in Azure DevOps|Field in Agile Development|
    |---------------------|--------------------------|
    |Title of the work item|Short description|

    For information on how to configure field mapping for a table, see [Customize your field map configuration](custom-field-map-config-azure-agile.md#). You can also create other field maps for your new table configuration.


## What to do next

1.  Validate your new table map configuration by clicking **Validate and fix mapping** from your process map form.
2.  In the Table maps related list, if the Valid column of your configuration shows:
    -   true, validation of your map configuration is successful.
    -   false, validation of your map configuration failed. Ensure that you enter correct values for all fields and validate again.
3.  Create a business rule to support export of this new table map configuration to Azure DevOps. For more information, see [Create a business rule to apply a custom table map configuration](create-business-rule-to-apply-custom-table-map.md).

**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

