---
title: Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0
description: Understand the setup process of Microsoft Azure DevOps Integration for Agile Development 2.0.
locale: en-US
release: xanadu
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0

Understand the setup process of Microsoft Azure DevOps Integration for Agile Development 2.0.

After you have the application installed in your ServiceNow instance, you can proceed to set up the integration, using the sn\_ado\_int.user role.

The setup process for the integration includes the following tasks:

1.  Connect Agile Development 2.0 with Azure DevOps.
2.  Discover and import available projects from Azure DevOps.
3.  Import area, teams, and iterations into Agile Development 2.0 from Azure DevOps.
4.  Set up the import and export between Agile Development 2.0 and Azure DevOps.
    1.  Register webhooks for an Azure DevOps project.
    2.  Associate Azure DevOps projects with assignment groups in Agile Development 2.0.
5.  Bulk import work items and iterations into Agile Development 2.0. Enable a scheduled job to auto-import issues from Azure DevOps.
6.  Create custom map configurations for tables, fields, and workflow states between Azure DevOps and Agile Development 2.0.

-   **[Connecting Agile Development 2.0 and Azure DevOps](../reference/connect-sn-agile-with-azure.md#)**  
Establish a connection between Agile Development 2.0 and Azure DevOps using a connection alias and an Azure DevOps instance.
-   **[Discover and import Azure DevOps projects](../task/discover-import-azure-projects.md)**  
Discover and import all available Azure DevOps projects into Agile Development 2.0 to start using the integration between the two applications.
-   **[Import areas, teams, and iterations from Azure DevOps](../task/import-areas-teams-azure-agile.md)**  
Import areas, teams, and iterations of your Azure DevOps projects. These details are used to import sprint data and associate your Azure DevOps projects with assignment groups in Agile Development 2.0.
-   **[Setting up import and export between Azure DevOps and Agile Development 2.0](../task/set-up-import-export-azure-agile.md#)**  
Configure the settings for the import and export actions of work items between Agile Development 2.0 and Azure DevOps.
-   **[Import work items from Azure DevOps to Agile Development 2.0](../task/bulk-import-agile-azure.md)**  
Import work items and iterations of an Azure DevOps project into Agile Development to track and update the status of your work.
-   **[Schedule jobs to import projects, teams, areas, and work items from Azure DevOps](../task/schedule-jobs-import-projects-azure.md)**  
Schedule jobs to automatically import new projects, teams, areas, work items, and sprints periodically from Azure DevOps into Agile Development 2.0.
-   **[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)**  
Customize the table, field, or state map configuration between Azure DevOps and Agile Development 2.0 according to your organizational preferences.
-   **[Generate a default map configuration between Azure DevOps and Agile Development 2.0](../task/generate-default-map-config-agile-azure.md)**  
Generate a default mapping for an Azure DevOps process type if you want to reset the existing map configuration.

**Parent Topic:**[Microsoft Azure DevOps Integration for Agile Development](agile-azure-integration-overview.md)

