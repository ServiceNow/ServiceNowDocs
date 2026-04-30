---
title: Apply custom map configuration to multiple Jira projects
description: Add a custom table or field, which is applicable to all your Jira projects of a specific type, to the map configuration template in Agile Development 2.0.
locale: en-US
release: xanadu
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2024-09-06"
reading_time_minutes: 2
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Apply custom map configuration to multiple Jira projects

Add a custom table or field, which is applicable to all your Jira projects of a specific type, to the map configuration template in Agile Development 2.0.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md).
-   Role required: sn\_jira\_int.user

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  From the Project Style Mappings related list, select the project template to which you want to add the custom field.

    For example, if the field that you want to add is applicable to all Jira projects of the type Classic, then select **classic**.

4.  Add the custom table or field from Agile Development 2.0 to the existing map configuration in the **Default Mapping** field.

    You can copy the contents of the **Default Mapping** field into a JSON viewer to view the contents in a format of your preference. For example, as shown in the following figures, you can add a new table for Defect \[rm\_defect\] to map the Bug table from Jira or a new field in the existing Story \[rm\_story\] table to map story points.

    ![Custom table map for defects](../image/json-custom-table-map.png "Custom table map for Defects")

    ![Custom field map for story points in Story table](../image/json-custom-field.png "Custom field map for Story Points")

    ![Custom field map for Multi-select field](../image/multi-select.png "Custom field map for Multi-select fields")

    If you're adding a new field, ensure that the custom field configured is added to the default screen scheme of the issue.

5.  Click **Update**.


## What to do next

Apply the custom project style map to all its related Jira projects.

1.  Delete the existing map configuration of all the imported Jira projects.

    You can delete the map configuration of a project by making its **Mapping Config** field empty.

    **Tip:** From the Jira Projects related list, make a multiple select on the **Mapping Config** field of all the Jira project records and remove their value, making all these fields empty.

2.  If you've created a new table map, create a business rule to apply this new table map configuration. See [Create a business rule to apply a custom Agile Development 2.0 table map configuration](jira-create-business-rule-to-apply-custom-table-map.md).
3.  Import these projects from Jira by clicking **Discover Projects**.

    This would import all the Jira projects with their map configuration as per the customized project style map.


**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

