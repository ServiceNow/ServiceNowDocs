---
title: Customize your state map configuration
description: Create a custom state map for a field of an Agile Development 2.0 table to map the workflow states of your preference for Azure DevOps projects of a process type.
locale: en-US
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Customize your state map configuration

Create a custom state map for a field of an Agile Development 2.0 table to map the workflow states of your preference for Azure DevOps projects of a process type.

## Before you begin

-   [Discover and import Azure DevOps projects](discover-import-azure-projects.md).
-   Role required: sn\_ado\_int.user

## About this task

You can map a state in Azure DevOps to multiple states in Agile Development 2.0. In such cases, the state in Agile Development 2.0 for an issue type depends on the choice order value that you provide for this state configuration.

For example, when an work item from Azure DevOps that is in the **Active** state imported, the **State** field in Agile Development 2.0 is set to **Work in progress** as it has the lowest choice order value.

You can also map multiple states in Azure DevOps to a single state in Agile Development 2.0.

## Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  From the Process Mapping related list, open a process map for which you want to customize the choice map configuration.

4.  Open the workflow state map for this process type.

    1.  From the Table Maps related list, click **User Story**.

    2.  From the Field Maps related list, click **state**.

5.  From the Choice maps related list, click **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Internal Choice|Value of the state in Agile Development 2.0. This value is an integer.|
    |External Choice|Name of the state in Azure DevOps.|
    |External Choice Name|Display name of the state in Azure DevOps.|

7.  Click **Submit**.


## What to do next

1.  Validate your new table map configuration by clicking **Validate and fix mapping** from your process map form.
2.  Navigate to your new choice map configuration. If the Valid column of your configuration shows:
    -   true, validation of your map configuration is successful.
    -   false, validation of your map configuration failed. Ensure that you enter the correct values for all fields and validate again.

**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

