---
title: Reset mapping configuration of Jira projects
description: Reset the existing mapping configuration for multiple Jira projects to a default mapping configuration.
locale: en-US
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Strategic Portfolio Management]
---

# Reset mapping configuration of Jira projects

Reset the existing mapping configuration for multiple Jira projects to a default mapping configuration.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md)
-   Role required: sn\_jira\_int.user

## About this task

Apply a default mapping configuration to all or a few Jira projects. Any existing custom mapping configuration for these projects will be deleted after you reset the mappings.

If you've cleared the **Mapping Config** field or deleted the existing table maps for this project, resetting the mappings for this project will restore the mapping configuration to the default configuration.

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  Reset the mappings of multiple Jira projects using one of the following ways.

<table id="choicetable_evm_cms_ymb"><thead><tr><th align="left" id="d75674e102">

Choice

</th><th align="left" id="d75674e105">

Action

</th></tr></thead><tbody><tr><td id="d75674e111">

**Reset mappings for a single project**

</td><td>

1.  From the Jira From the Jira Projects related list, open the required project.
2.  Click **Reset Mappings**.


</td></tr><tr><td id="d75674e132">

**Reset mappings of multiple projects that belong to different project styles**

</td><td>

1.  From the Jira Projects related list, select the required projects.
2.  Click the **Actions on selected rows** list.
3.  Click **Reset Mappings**.


</td></tr><tr><td id="d75674e159">

**Reset mappings of multiple projects that belong to the same project style**

</td><td>

From the Project Style Mappings related list, open a project template.For example, if you want to reset the mappings of Jira Cloud Classic projects, select **classic**.

 1.  Verify the mapping configuration in the **Default Mapping** field and update it if required.
2.  Select the required projects from the list.
3.  Click the **Actions on selected rows** list.
4.  Click **Reset Mappings**.


</td></tr><tr><td id="d75674e198">

**Reset mappings of all projects that belong to the same project style**

</td><td>

From the Project Style Mappings form, click **Reset Mappings**.

</td></tr></tbody>
</table>
## Result

The mapping configuration of the projects is updated to as per the **Default Mapping** field in the Project Style Mappings form that the selected projects belong to.

**Parent Topic:**[Setting up the integration between Jira and Agile Development 2.0](setting-up-the-integration-between-jira-and-agile-development.md)

