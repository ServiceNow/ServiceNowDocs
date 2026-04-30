---
title: Configure impact metrics
description: Configure the Key Performance Indicators \(KPIs\) for this process.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure impact metrics

Configure the Key Performance Indicators \(KPIs\) for this process.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side of the page, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. Select **Impact metrics** from the side panel.

    If you’re proceeding from the **Investigative features** page, then you come to this page. For more information, see [Configure investigative features](investigative-features.md).

    The **Impact metrics** page has four sections:

    -   **Idle time analysis**: Idle time analysis focuses on the periods when a case is assigned to a team but not yet assigned to a specific resource. This is the time during which the case remains inactive, waiting for someone to take action.

        Analyzing idle time helps identify inefficiencies, such as delays in task assignment or workflow bottlenecks, enabling teams to improve coordination and reduce waiting times within processes.

        **Note:** Idle time analysis not available without configuring in process configuration. Idle time analysis is available for the field that is set in the **Team definition** section in the Process details page.

    -   **Touchpoint analysis**: Touchpoint analysis studies specific interactions within a process to identify areas of high interaction, particularly spotlighting inefficient, redundant, or excessive activities. By pinpointing these areas, it enables process optimization through automation or other improvements, enhancing performance and reducing operational costs.

        **Note:** Touchpoint analysis not available without configuring in process configuration.

    -   **KPI dashboard**: KPI dashboards include data visualizations, filters, and other components to track Key Performance Indicators \(KPIs\) for the process. They leverage Platform Analytics dashboards to deliver insights directly within process mining projects.
    -   **KPI categories**: KPI categories are predefined categories that organize KPIs into groups based on common process objectives.
    ![Impact metrics in process configuration](../image/impact-metrics-proc-con.png)

4.  Fill the details in the **Idle time analysis** section.

    Before providing the details, ensure that:

    -   The state, team, and agent definitions are fully completed on the Process details page.
    -   The mapping of states to stakeholders is complete as part of the State definition.
    1.  Service provided is selected by default for the **Related state responsibility** field.

    2.  Filter any team you want to exclude from the idle time calculation in the **Teams excluded from the selection** field.

        Select **Edit filter** and set a filter.

    3.  Select any user where if the case is assigned to this user, it's excluded from the idle time calculation in the **Users excluded from analysis** field.

        Select **Edit filter** and set a filter.

5.  Fill the details in the **Touchpoint analysis** section.

    1.  Select fields in the **Fields that are frequently updated** field.

        Unique updates in any of the selected fields count as touchpoints.

        Recommendations are provided based on the inputs in the **Agent definition** section in the **Process details** page and the **Work notes analysis** settings in the **Investigative features** page.

        **Note:** You can set a maximum of five fields.

    2.  Select **Include touchpoint metrics in new projects by default** if you want to include the fields selected here are added to the projects automatically.

    3.  Select users whose updates you want to exclude in the **Exclude updates made by these users** field.

        It’s a good idea to exclude system users to improve your analysis.

    4.  Provide a value for the **Time interval in seconds to group updates** field.

        Multiple updates of the same record are grouped into a single touchpoint if they occur within the defined time interval. Set it to 0 to turn off the grouping.

6.  Select a Platform Analytics Key Performance Indicators \(KPIs\) dashboard.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    If you want to create a KPI dashboard, select **New Dashboard**. For more information, see [Create a dashboard with the in-line editor](../../../use/dashboards/task/create-db-in-ac.md).

7.  Provide values for each KPI categories.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    **Note:** The KPI categories are dynamic and are retrieved from the sys\_choice table, which includes category order and hint information.

8.  Select **Continue to improvement opportunities**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](process-config-builder.md)

