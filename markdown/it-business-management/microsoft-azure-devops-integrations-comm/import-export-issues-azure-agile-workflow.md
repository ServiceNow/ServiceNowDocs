---
title: Importing and exporting work items between Agile Development and Azure DevOps
description: Understand the workflow for the import and export of work items between Agile Development and Azure DevOps.Sync sprint details from Agile Development 2.0 to Azure Devops. Any change in the sprint details in Agile Development 2.0 is exported to Iteration paths in Azure DevOps, when the Sync sprint field is checked.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Importing and exporting work items between Agile Development and Azure DevOps

Understand the workflow for the import and export of work items between Agile Development and Azure DevOps.

To enable import and export of work items between Agile Development 2.0 and Azure DevOps, you must [configure the settings](../task/set-up-import-export-azure-agile.md#).

## Importing to Agile Development 2.0 from Azure DevOps

-   When you create a work item of type epic in Azure DevOps, an epic is created for the assignment group according to the team integration settings that you configured.
-   When you create a work item of type story in Azure DevOps, a story is created for the assignment group according to the team integration settings that you configured.

    The relationship between the story and its epic is retained as it is in Azure DevOps.

-   Only the fields that are defined in the field map configuration are retained in the story or epic. For the details of the default map configuration, see [Default map configuration for Azure DevOps integration with Agile Development 2.0](default-agile-azure-mapping.md).
-   When you add an attachment to a work item in Azure DevOps, the same attachment is added to the corresponding story or epic in Agile Development 2.0.
-   Any new iterations created in Azure DevOps do not create a corresponding sprint record in Agile Development 2.0 immediately.

    When a work item is added for the first time to the new iteration in Azure DevOps, only then a corresponding sprint record is created in Agile Development 2.0. To ensure consistent data across the two applications at all times, create sprints in Agile Development 2.0.

-   Only leaf level iterations are retained as sprints in Agile Development 2.0.
-   When you add comments for an issue in Azure DevOps, they are updated in the **Work notes** field of the story or epic in Agile Development, based on the map configuration.

    **Note:** The images added in the comments are not supported.

-   When you delete a work item in Azure DevOps, the corresponding record is deleted in Agile Development 2.0.
-   When you delete an iteration in Azure DevOps, the corresponding sprint is deleted in the Agile Development 2.0.

    **Note:** To delete records in the Agile Development 2.0, set the **Can Delete** field to **true** in the Application access of the respective tables. For details, see Table design and runtime settings.

-   When you restore a work item from recycle bin in Azure DevOps, a corresponding record is created in Agile Development 2.0 according to its team integration settings.

![Import of work item from Azure DevOps to Agile Development](../image/Import-workflow-for-work-item-created.png "Import workflow for work items created in Azure DevOps")

![Import of area update in Azure DevOps](../image/Import-workflow-for-area-update.png "Import workflow for areas updated in Azure DevOps")

## Exporting from Agile Development to Azure DevOps

-   When you create an epic for an assignment group, it is exported as a work item to the area in Azure DevOps according to the team integration settings that you configured.
-   When you create a story for an assignment group, it is exported as a work item to the area in Azure DevOps according to the team integration settings that you configured.

    The relationship between the story and its epic is retained in Azure DevOps.

-   When you add an attachment to a story or an epic, the same attachment is added to the corresponding work item in Azure DevOps.
-   When you update the assignment group of an existing story in the Agile Development 2.0, the work item is recreated for the Azure DevOps area that is associated with the updated assignment group.
-   When you create a sprint for an assignment group in Agile Development 2.0, it is exported to Azure DevOps under its backlog iteration as per the team integration settings.
-   When you delete a sprint for an assignment group in Agile Development 2.0, it unlinks the sprint selection from the team's iteration in Azure DevOps.
-   When you update a work item in Agile Development 2.0, only the fields that are updated are sent to Azure DevOps as a part of the payload

![Export workflow for assignment group update in Agile Development 2.0](../image/Export-workflow-for-assignment-group-update.png "Export workflow for assignment groups updated in Agile Development 2.0")

**Parent Topic:**[Microsoft Azure DevOps Integration for Agile Development](../concept/agile-azure-integration-overview.md)

## Sync sprint details between Agile Development 2.0 and Azure DevOps

Sync sprint details from Agile Development 2.0 to Azure Devops. Any change in the sprint details in Agile Development 2.0 is exported to Iteration paths in Azure DevOps, when the Sync sprint field is checked.

|Sync Sprint|Export|Import|
|-----------|------|------|
|Disabled \(Iteration path available in Azure Devops\)|Sends the default iteration path for the project to Azure DevOps.|Sprint value does not change in Agile Development 2.0.|
|Disabled \(Iteration path is not available in Azure Devops\)|Sends the default iteration path for the project to Azure DevOps.|Sprint value does not change in Agile Development 2.0.|
|Enabled \(Iteration path is available in Azure Devops\)|Sends the appropriate iteration path for the project to Azure DevOps.|Sprint value does not change in Agile Development 2.0.|
|Enabled \(Iteration path is not available in Azure Devops\)|Sends the default iteration path for the project to Azure DevOps.|Sprint value clears in Agile Development 2.0.|

|Sync sprint|Export|Import|
|-----------|------|------|
|Disabled|Sends the previous iteration path to Azure. Iteration path will be same in Azure DevOps.|Sprint value in Agile Development 2.0 is selected.|
|Enabled|Sends the new iteration path based on the selection. Iteration will be changed based on selection.|Sprint value in Agile Development 2.0 is selected.|

