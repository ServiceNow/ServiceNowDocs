---
title: Generate a default map configuration between Azure DevOps and Agile Development 2.0
description: Generate a default mapping for an Azure DevOps process type if you want to reset the existing map configuration.
locale: en-US
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Generate a default map configuration between Azure DevOps and Agile Development 2.0

Generate a default mapping for an Azure DevOps process type if you want to reset the existing map configuration.

## Before you begin

-   [Discover and import Azure DevOps projects](discover-import-azure-projects.md).
-   Role required: sn\_ado\_int.user

## About this task

You can restore the default map configuration of an Azure DevOps process type by deleting the existing table maps and then creating mappings for this process type.

When you import available work items such as epics and stories from Azure DevOps, this data is stored in tables as defined in the map configuration of the project's process type.

If the table map does not exist for a work item in your Azure DevOps process, this work item cannot be imported and exported between Azure DevOps and Agile Development 2.0.

## Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  From the Process Mapping related list, open a process map for which you want to generate the default map configuration.

4.  Click **Create Mappings**.

    **Note:** If a table maps already exist for this process, the **Create Mappings** button is not displayed.

    A request of the type Create Mappings is created and is visible in the Azure DevOps Import Requests related list of your Azure DevOps instance.


## Result

Once the state of the Create mappings request changes to **Completed**, you can see that the **Mapping Config** field of this Azure DevOps process is populated. Also, you can see the default map configuration in the Table Maps related list of this process.

**Parent Topic:**[Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0](../concept/setting-up-agile-azure-integration.md)

**Related topics**  


[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

