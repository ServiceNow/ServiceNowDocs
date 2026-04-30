---
title: Create process configuration using Process Configuration Builder
description: Process configurations include process preferences that activate features in the Process Mining workspace and assist in the creation of projects. Having complete process configurations enables you to independently create projects and quickly gain insights, even without prior process mining knowledge. This enhances the scalability of process mining across the organization.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Create process configuration using Process Configuration Builder

Process configurations include process preferences that activate features in the Process Mining workspace and assist in the creation of projects. Having complete process configurations enables you to independently create projects and quickly gain insights, even without prior process mining knowledge. This enhances the scalability of process mining across the organization.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

    ![Process configuration builder](../image/process-config-1.png)

    The page displays the following information:

    -   ![Label for section A](../image/icon-a.png): Process configurations icon
    -   ![Label for section B](../image/icon-b.png): Process configurations help icon
    -   ![Label for section C](../image/icon-c.png): Read-only process configuration templates from content pack applications
    -   ![Label for section D](../image/icon-d.png): List of tables for which the configuration is created
    -   ![Label for section E](../image/icon-e.png): Button that enables you to create a new configuration
    -   ![Label for section F](../image/icon-f.png): Information displayed after selecting the information icon \(![Label for section B](../image/icon-b.png)\)
3.  Select **Create New**.

    The New process configuration dialog box is displayed.

    ![New process configuration dialog box](../image/new-pr-config.png)

    If a content pack application is installed for a process, the following dialog box is displayed.

    ![New process configuration dialog box](../image/new-pr-config-cp.png)

4.  Select a table.

5.  Select the **Start with pre-built content pack template** option if you want to use the content pack template.

    **Note:** This option is available only if a content pack application is installed for a process.

    For more information about process configurations using content packs, see [Create process configurations using content packs](process-config-content-pack.md).

6.  Select **Get started**.

    **Important:**

    Only one process configuration is allowed per table. Before creating a process configuration for a table, ensure that process configuration isn’t yet created for that table. If a configuration is available for the table, use the configuration. You can edit the configuration by opening the table from the **Configurations** list.

    The **Process details** page is displayed.


-   **[Configure process details](process-details.md)**  
Describe the process to get help with further configuration and enhance the quality of the project setup and analysis.
-   **[Configure recommendations setup](reco-setup.md)**  
Set up recommendations to simplify project creation and get help in the analysis.
-   **[Configure investigative features](investigative-features.md)**  
Configure investigative features to set advanced analytics features for a process.
-   **[Configure impact metrics](impact-metrics.md)**  
Configure the Key Performance Indicators \(KPIs\) for this process.
-   **[Configure improvement opportunities](improvement-opportunities.md)**  
Create a library of inefficiencies to identify the improvement opportunities for your project.

**Parent Topic:**[Creating process configuration](../concept/creating-process-config.md)

