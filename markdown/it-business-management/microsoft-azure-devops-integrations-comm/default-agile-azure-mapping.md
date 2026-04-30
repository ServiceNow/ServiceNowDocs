---
title: Default map configuration for Azure DevOps integration with Agile Development 2.0
description: Understand the default field map configuration, of different process types, between Azure DevOps and Agile Development 2.0.
locale: en-US
release: yokohama
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discover and import Azure DevOps projects, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Default map configuration for Azure DevOps integration with Agile Development 2.0

Understand the default field map configuration, of different process types, between Azure DevOps and Agile Development 2.0.

By looking at the default map configuration for different process types, you can see how work item types in Azure DevOps are mapped in Agile Development. You can also see how fields are mapped between the two applications.

When you import available epics, stories, and issues from Azure DevOps, this data is stored in tables as defined in the process map configuration.

**Note:**

When you upgrade to version 1.3 of the application, map configuration is generated at the process level per process type and not at the instance level. You must update any custom maps that you previously configured to ensure that the import and export of work items is not impacted.

Here's how you can view the default map configuration for different process types.

1.  Navigate to **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.
2.  Open your Azure DevOps instance record.
3.  From the Process Mappings related list, open the record for a process map.

You can add or update the configuration for field, table, and choice maps between Azure DevOps and Agile Development 2.0. For details, see [Customizing your map configuration for Azure DevOps integration](customizing-map-config-agile-azure.md).

The following are the details of the default map configuration for various process types in Azure DevOps.

## Default mapping for Agile process

|Table in Azure DevOps|Table in Agile Development 2.0|
|---------------------|------------------------------|
|User Story|Story \[rm\_story\]|
|Epic|Epic \[rm\_epic\]|
|Feature|Feature \[ sn\_safe\_feature\]|

## Default mapping for Basic process

|Table in Azure DevOps|Table in Agile Development 2.0|
|---------------------|------------------------------|
|Issue|Story \[rm\_story\]|
|Epic|Epic \[rm\_epic\]|

## Default mapping for CMMI process

|Table in Azure DevOps|Table in Agile Development 2.0|
|---------------------|------------------------------|
|Epic|Epic \[rm\_epic\]|
|Requirement|Story \[rm\_story\]|

## Default mapping for Scrum process

|Table in Azure DevOps|Table in Agile Development 2.0|
|---------------------|------------------------------|
|Product Backlog Item|Story \[rm\_story\]|
|Epic|Epic \[rm\_epic\]|

**Parent Topic:**[Discover and import Azure DevOps projects](../task/discover-import-azure-projects.md)

