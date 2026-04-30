---
title: Importing and exporting issues between Agile Development 2.0 and Jira
description: Understand the workflow for the import and export of issues between Agile Development 2.0 and Jira.
locale: en-US
release: yokohama
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Importing and exporting issues between Agile Development 2.0 and Jira

Understand the workflow for the import and export of issues between Agile Development 2.0 and Jira.

To export and import issues between Agile Development 2.0 and Jira, you must complete the [team integration settings](../task/project-integration-settings.md) for your Jira projects.

## Importing to Agile Development 2.0 from Jira

-   When you create an issue of type epic in a Jira project, an epic is created for the assignment group according to the team integration settings that you configured.
-   When you create an issue of type story in a Jira project, a story is created for the assignment group according to the team integration settings that you configured.
    -   The relationship between the story and its epic is retained as it is in Jira.
    -   The **Assigned To** field in the story displays the user from Jira, only if a user with the same email address is found in Agile Development 2.0.
-   Only the fields that are defined in the field map are retained in the story or epic. For details of the default mapping configuration, see [Default mapping configuration between Agile Development 2.0 and Jira](jira-sn-field-mapping.md).
-   When you add an attachment to an issue in Jira, the same attachment is added to the corresponding story or epic in Agile Development 2.0.
-   When you add comments for an issue in Jira, they are updated in the **Work notes** field of the story or epic in Agile Development 2.0, based on the map configuration.

    **Note:** The images added in the comments appear as attachments.

-   When you delete an issue in Jira, the corresponding record is deleted in Agile Development 2.0.

    **Note:** To delete records in Agile Development 2.0, set the **Can Delete** field to **true** in the Application access of the respective tables. For details, see [Table design and runtime settings](https://www.servicenow.com/docs/access?context=r_TableApplicationAccessFields&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

-   When you start a sprint in Jira, a sprint is created for the assignment group in Agile Development 2.0, if the Jira board is configured in the team integration settings.

<table id="table_qcf_mxs_hkb"><tbody><tr><td>

![Import for issue created in Jira](../image/issue-created-in-jira.png "Import workflow for issue created in Jira")

</td><td>

![Import for issue updated in Jira](../image/issue-updated-in-jira.png "Import workflow for issue updated in Jira")

</td></tr></tbody>
</table>## Exporting from Agile Development to Jira

-   When you create an epic for an assignment group, it is exported to the project in Jira according to the team integration settings that you configured.
-   When you create a story for an assignment group, it is exported to the project in Jira according to the team integration settings that you configured.
    -   The relationship between the story and its epic is retained in Jira.
    -   Updates to the **Assigned To** field in the ServiceNow platform is exported to Jira.
-   When you add an attachment to a story or an epic, the same attachment is added to the corresponding issue in Jira.
-   When you add work notes to a story or an epic, they are updated in the corresponding issue in Jira as comments.
-   When you update the assignment group of an existing story in Agile Development 2.0, the issue is recreated in the Jira project that is associated with the updated assignment group.
-   When you create a sprint for an assignment group in Agile Development 2.0, it is exported to Jira only if you configured the Jira board in the team integration settings.

    **Note:** If your Jira instance has state transition rules, the export sync from Agile Development 2.0 to Jira might fail. For example, if a transition rule in Jira restricts a story or work item from moving directly to a **Complete** state without first passing through an **In Progress** state, and the story is marked **Complete** without that intermediate step, the sync fails.


**Parent Topic:**[Atlassian Jira Integration for Agile Development](../concept/agile-jira-integration-overview.md)

