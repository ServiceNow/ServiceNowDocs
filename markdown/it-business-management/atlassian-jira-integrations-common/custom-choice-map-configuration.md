---
title: Customize your workflow state configuration
description: Create a custom workflow state map of your preference for a Jira project.
locale: en-US
release: yokohama
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Customize your workflow state configuration

Create a custom workflow state map of your preference for a Jira project.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md).
-   Role required: sn\_jira\_int.user

## About this task

Map a custom workflow state from Jira to Agile Development 2.0.

You can map a workflow state in Jira to multiple workflow states in Agile Development 2.0. In such cases, the state in Agile Development 2.0 for an issue type depends on the choice order value that you provide for this state configuration.

For example, the **In Progress** state in Jira is mapped to multiple states such as **Work in progress**, **Ready for testing**, and **Testing** in Agile Development 2.0 using a choice order of 10, 20, and 30.

So, when an **In Progress** issue from Jira is imported, the **State** field in Agile Development 2.0 is set to **Work in progress** as it has the lowest choice order value.

You can also map multiple workflow states in Jira to a single workflow state in Agile Development 2.0.

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  From the Jira Projects related list, open a Jira project for which you want to customize the choice map configuration.

4.  Open the workflow state map for this project.

    1.  From the Table Maps related list, click **Story**.

    2.  From the Field Maps related list, click **Status**.

5.  From the Choice Maps related list, click **New**.

6.  On the form, fill in the fields.

<table id="table_snv_hpt_bkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal Choice

</td><td>

Value of the workflow state in Agile Development 2.0. This value is an integer.

</td></tr><tr><td>

External Choice

</td><td>

ID of the workflow transition in Jira.**Note:** In case there is no transition, insert the ID of the workflow state.

</td></tr><tr><td>

External Choice Name

</td><td>

Display name of the workflow transition in Jira.**Note:** In case there is no transition, insert the display name of the workflow state.

</td></tr></tbody>
</table>7.  Click **Update**.


## What to do next

1.  Validate your choice map configuration by clicking **Validate and fix mapping** from your project form.
2.  From the Table maps related list of your project, navigate to your new choice map configuration. If the Valid column for your configuration shows:
    -   true, validation of your map configuration is successful.
    -   false, validation of your map configuration failed. Ensure that you enter correct values for all fields and validate again.

**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

