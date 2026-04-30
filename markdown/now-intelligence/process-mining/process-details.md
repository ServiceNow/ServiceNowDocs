---
title: Configure process details
description: Describe the process to get help with further configuration and enhance the quality of the project setup and analysis.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure process details

Describe the process to get help with further configuration and enhance the quality of the project setup and analysis.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## About this task

Providing the information in the Process details page helps you in the following ways:

-   Guides you to create projects by providing recommendations for the fields for your analysis. The fields that you specify for state and team definitions are provided as recommendations for activity definitions when creating a project. For more information about how the recommended fields are displayed when setting activity definitions, see the table in the [Set activity definitions](set-activity-def.md) section.
-   Unlocks different impact metrics like idle time. The mapping of the state with the stake holders helps in identifying idle time in the process.
-   Helps in configuring the next steps in the process configuration. Based on the settings here, recommendations are provided in the Automation opportunities page.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side panel, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. This page has three sections:

    -   State definition
    -   Team definition
    -   Agent definition
    **Note:** Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

4.  Fill the details in the **State definition** section.

    ![State definition section in Process details for process configuration](../image/process-det-1.png)

    State represents the status of a record within a workflow. It shows how the record progresses toward completion.

    1.  Select a field.

        Defining a state improves analysis by revealing domain-specific insights, such as idle time. It also helps by providing recommendations for activity definitions when creating a project. For more information about how the recommended fields are displayed when setting activity definitions, see the table in the [Set activity definitions](set-activity-def.md) section.

        If you select `State` for this field, then in the process graph you’ll see how records moved from one state to another state.

    2.  Select **Automatically add as an activity to new projects** if you want the selected field to add automatically as an activity in every new project.

        This simplifies the setup. If you don’t need a field for analysis, you can remove it.

    3.  Select **Map state reponsibilities** to map each state with a stakeholder who is responsible for moving the records to the next process state.

        Mapping states with stakeholders enables you to take advantage of advanced process mining features, such as idle-time analysis.

        -   Assign each process state to the appropriate stakeholder responsibility.
        -   Look for the required fields marked with an asterisk \(\*\) to ensure completeness.
        -   The tooltips provide more information to help you.
    4.  Select **Save**.

5.  Fill the details in the **Team definition** section.

    **Note:** If you select a field in the Process details page that is selected in the promin.blocked.tables list, then the Idle time metrics is not available to set up.

    ![Team definition section in Process details for process configuration](../image/process-det-team.png)

    Team refers to a group of individuals who are responsible for a task in your workflow.

    1.  Select a field.

        Defining a team helps to evaluate team efficiency, track handover of work, and analyze metrics like idle time. It also helps by providing recommendations for activity definitions when creating a project. For more information about how the recommended fields are displayed when setting activity definitions, see the table in the [Set activity definitions](set-activity-def.md) section.

        If you select `Assignment group` for this field, then in the process graph you’ll see how records moved from one group to another group.

    2.  Select **Automatically add as an activity to new projects** if you want the selected field to add automatically as an activity in every new project.

        This simplifies the setup. You can remove the field if it's not needed for analysis.

6.  Fill the details in the **Agent definition** section.

    ![Agent definition section in Process details for process configuration](../image/process-det-agent.png)

    Agent refers to an individual who is responsible for a task in your workflow.

    1.  Select a field.

        Defining an agent helps to analyze idle time and handover of work, and improving process efficiency. It also helps by providing recommendations for activity definitions when creating a project. For more information about how the recommended fields are displayed when setting activity definitions, see the table in the [Set activity definitions](set-activity-def.md) section.

        If you select `Assigned to` for this field, then in the process graph you’ll see how records moved from one assignee to another.

7.  Select **Continue to recommendations setup**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](process-config-builder.md)

