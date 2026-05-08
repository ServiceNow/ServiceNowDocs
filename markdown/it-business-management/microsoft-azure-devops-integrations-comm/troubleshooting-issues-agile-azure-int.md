---
title: Troubleshooting issues for Azure DevOps integration with Agile Development
description: Resolve common issues that you might face while working with the integration of Azure DevOps and Agile Development 2.0.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Troubleshooting issues for Azure DevOps integration with Agile Development

Resolve common issues that you might face while working with the integration of Azure DevOps and Agile Development 2.0.

<table id="table_gsp_wdx_hkb"><thead><tr><th>

Issue

</th><th>

Action

</th></tr></thead><tbody><tr><td>

The export action is not working.

</td><td>

-   Review your custom map configuration.

If your custom map configuration is invalid or if the required fields are not mapped for that work item, export does not work.

-   Ensure that the **Enable Export** check box is selected for the project.
-   Check to see if your Azure DevOps password has expired.

</td></tr><tr><td>

Sprint is not imported from Azure DevOps to Agile Development 2.0.

</td><td>

Sprints are not imported to Agile Development 2.0 for one of the following reasons:-   Any new iterations created in Azure DevOps do not create a corresponding sprint record in Agile Development 2.0 immediately.

When a work item is added for the first time to the new iteration in Azure DevOps, only then a corresponding sprint record is created in Agile Development 2.0.

To ensure consistent data across the two applications at all times, create sprints in Agile Development 2.0.

-   Ensure that there are no overlapping sprints.

</td></tr><tr><td>

An assignment group is not populated for a story or an epic.

</td><td>

If the team is not associated with an assignment group in Agile Development 2.0, it can result in assignment group not being populated. Verify that project integration settings exist for your Azure DevOps team.

 If the area of a work item is mapped to multiple teams, the assignment group for that work item in Agile Development 2.0 is empty. In such cases, you can manually select an assignment group for this work item.

</td></tr><tr><td>

A value from a field in Azure DevOps is not populated in Agile Development 2.0.

</td><td>

Verify if the custom field map is configured.

</td></tr><tr><td>

The value of **Priority** or **State** fields from Azure DevOps is not populated in Agile Development 2.0.

</td><td>

Verify if the custom state map is configured.

</td></tr><tr><td>

An update by a user in Azure DevOps is not updated in Agile Development 2.0.

</td><td>

Ensure that the user credentials that are used to set up the integration of Azure DevOps with Agile Development 2.0 are not used to perform record updates.

</td></tr><tr><td>

The work item is deleted in Azure DevOps but not deleted in Agile Development 2.0.

</td><td>

Ensure that the **Can Delete** field in the Application access of the respective tables is set to **true**.

 For details, see Table design and runtime settings.

</td></tr><tr><td>

Deleting a project, team, or area does not result in any action in Agile Development 2.0.

</td><td>

After deleting the project, team, or area in Azure DevOps, the Azure DevOps administrator must manually delete the corresponding Azure DevOps project and its associated stories in Agile Development 2.0.

</td></tr><tr><td>

New Azure DevOps projects are not imported automatically.

</td><td>

Manually discover projects from the Azure DevOps instance record to immediately synch the project updates or schedule a job to discover and import these updates on a daily basis.For more details on the scheduled jobs, see [Schedule jobs to import projects, teams, areas, and work items from Azure DevOps](../task/schedule-jobs-import-projects-azure.md).

</td></tr><tr><td>

Imported work items \(epics and stories\) of a project have no assignment group associated with them.

</td><td>

Ensure that you have team integration settings for this project. For more information, see [Associate Azure DevOps projects with assignment groups in Agile Development 2.0](../task/set-up-import-export-azure-agile.md#).

 The assignment group associated to any imported work item of an Azure DevOps project is based on the team integration settings of that project. If the project does not have any team integration setting, the imported work item will have an empty assignment group.

</td></tr><tr><td>

Changes made to iterations in Azure DevOps are not reflecting immediately in Agile Development 2.0.

</td><td>

Manually import iterations from the Azure DevOps project record or schedule a job to discover and import these updates daily. For more details on the scheduled jobs, see [Schedule jobs to import projects, teams, areas, and work items from Azure DevOps](../task/schedule-jobs-import-projects-azure.md).

</td></tr><tr><td>

The UI actions for Connect, Disconnect, and Validate and Fix result in an error when using for the first time.

</td><td>

This error is a known issue. Retry the UI action.

</td></tr><tr><td>

When the **Description** field has &amp; in Azure DevOps, it renders as &amp;amp; in Agile Development 2.0.

</td><td>

The field mapping between Agile Development 2.0 and Azure DevOps is not supported for HTML fields.

</td></tr><tr><td>

Export still works when the webhooks are de-registered.

</td><td>

Webhooks are only to import data from Azure DevOps to Agile Development 2.0. To stop the export of workitems, de-select the **Export Work Items** checkbox for the project.

</td></tr></tbody>
</table>## Enabling detailed project logs

To view all the details on project logging, enable the integration project logging property. For more information, see [Enable detailed project logging in Microsoft Azure DevOps Integration with Agile Development 2.0](../task/enable-integration-logs-azure.md).

