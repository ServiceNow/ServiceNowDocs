---
title: Setting up import and export between Azure DevOps and Agile Development 2.0
description: Configure the settings for the import and export actions of work items between Agile Development 2.0 and Azure DevOps.Register webhooks to subscribe to the events from your Azure DevOps projects to Agile Development 2.0.Associate your Azure DevOps projects and teams with assignment groups in Agile Development 2.0 to enable import and export of issues between the two applications.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Setting up import and export between Azure DevOps and Agile Development 2.0

Configure the settings for the import and export actions of work items between Agile Development 2.0 and Azure DevOps.

To enable synchronization of work items, register webhooks for your Azure DevOps projects and associate your Azure DevOps projects and teams with assignment groups in Agile Development 2.0.

**Parent Topic:**[Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0](../concept/setting-up-agile-azure-integration.md)

## Register webhooks for an Azure DevOps project

Register webhooks to subscribe to the events from your Azure DevOps projects to Agile Development 2.0.

### Before you begin

-   [Discover and import Azure DevOps projects](discover-import-azure-projects.md).
-   Role required: sn\_ado\_int.user

### Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  From Azure DevOps Projects related list, open your project record.

4.  Click **Register Webhooks**.

    If the webhook registration is successful, the **State** field in the project form changes from **Not Registered** to **Registered**.


### Result

When you register webhooks in Azure DevOps,it receives the following event updates between Azure DevOps and Agile Development 2.0.

-   Create a work item
-   Update a work item
-   Delete a work item
-   Restore a work item
-   Comment on a work item

For more information on synchronization of work items according to these webhook events, see [Importing and exporting work items between Agile Development and Azure DevOps](../reference/import-export-issues-azure-agile-workflow.md#).

### What to do next

[Associate Azure DevOps projects with assignment groups in Agile Development 2.0](set-up-import-export-azure-agile.md#)

.

## Associate Azure DevOps projects with assignment groups in Agile Development 2.0

Associate your Azure DevOps projects and teams with assignment groups in Agile Development 2.0 to enable import and export of issues between the two applications.

### Before you begin

-   [Import areas, teams, and iterations from Azure DevOps](import-areas-teams-azure-agile.md).
-   Create assignment groups in Agile Development. See [Create an assignment group in Agile Development 2.0](../../agile-development/task/create-an-agile-group.md#).
-   Role required: sn\_ado\_int.user

### About this task

After you associate an Azure DevOps team with an assignment group, you can:

-   Import all available stories and epics of this team into the associated group.
-   View any new stories and epics or updates made to the existing stories and epics in both Agile Development 2.0 and Azure DevOps.
-   Import iterations as sprints in Agile Development 2.0.

### Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Team Integration Settings**.

2.  Click **New**.

3.  In the Team Integration Settings form, select:

    -   An Azure DevOps project.
    -   A team of your Azure DevOps project.
    -   An assignment group in Agile Development 2.0 with which you want to associate the selected Azure DevOps team.
    The value of the **Default Area** field is filled automatically depending on the selected team.

    **Note:** If a **Default Area** value is already used for a Team Integration Settings record, then it cannot be used for another Team Integration Settings record because Backlog in Agile Development 2.0 can't be shared among multiple assignment groups.

    Stories or epics that don't have an Assignment group in Agile Development 2.0 will not be synced with Azure DevOps. This is because values from the Team Integration Setting record are used determine which ADO project a story or epic in Agile Development 2.0 belongs to.

4.  Click **Submit**.

    You can view the details of your settings in the Team Integration Settings in the Azure DevOps Project form.

    **Note:** You can associate an assignment group with only one Azure DevOps team.


### What to do next

[Import work items from Azure DevOps to Agile Development 2.0](bulk-import-agile-azure.md)

.

**Related topics**  


[Importing and exporting work items between Agile Development and Azure DevOps](../reference/import-export-issues-azure-agile-workflow.md#)

