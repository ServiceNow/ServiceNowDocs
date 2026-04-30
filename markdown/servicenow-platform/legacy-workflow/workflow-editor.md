---
title: Workflow editor
description: The Workflow Editor is an interface for creating and modifying workflows by arranging and connecting activities to drive processes.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow editor

The Workflow Editor is an interface for creating and modifying workflows by arranging and connecting activities to drive processes.

**Important:** As of the Zurich release, new customers no longer receive the legacy workflows created and published by ServiceNow, Inc.. All legacy workflow functionality has been replaced by Workflow Studio content. Only customers who upgraded from prior versions retain the ability to use and edit existing legacy workflows. While all customers retain the ability to create legacy workflows, you are strongly encouraged to instead use Workflow Studio to create process automation content. Only Workflow Studio will receive new features and enhancements.

You can manage multiple workflows in the same screen, create custom workflow activities, and use existing activities as data sources. Users with the workflow\_creator role can create workflows. Users with the workflow\_admin role can create, modify, delete, and publish workflows.

To open the Workflow Editor, navigate to **Workflow** &gt; **Workflow Editor**. For information about using the editor, see [Create a workflow](../../workflow-administration/task/t_CreateAWorkflow.md).

## Welcome screen

The editor opens with the **Welcome** page, which displays a list of active, published workflows. From this tab, you can open existing workflows, create new workflows, and open help resources related to workflow.

![Workflow welcome screen](../image/WorkflowWelcomeTab.png)

-   **![Number 1 icon](../image/no-1-icon.png)List display filters**

    **Published**: Click to view list of published workflows

    **Checked Out**: Click to view list of workflows checked out to current user

    **Help**: Click to view links to help resources for workflow

-   **![Number 2 icon](../image/no-2-icon.png)New Workflow button**

    Click to create a new workflow

-   **![Number 3 icon](../image/no-3-icon.png)Palette tabs**

    **Workflows**: Workflow activities and workflows you can use as subflows.

    **Core**: Available workflow activities appropriate for the selected workflow. Contents can include activities provided by the base system and those purchased with orchestration.

    **Packs**: Orchestration activity packs downloaded from the ServiceNow® App Store, organized by vendor and scope. Custom activities and workflows that you scope also appear as packs. Only visible if the orchestration plugin is installed.

    **Custom**: Orchestration custom activities available. Only visible if the orchestration plugin is installed.

    **Data**: Activities in the current workflow that output data. You can use these activities as data sources for other activities. Only visible if the orchestration plugin is installed.


**Note:** If your workflow welcome page does not look like this example, you may have customized the workflow welcome page before upgrading to Zurich. You can update the workflow welcome page to the latest version by editing the [UI pages](https://www.servicenow.com/docs/access?context=r_UIPages&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) .

Navigate to **System UI** &gt; **UI Pages** &gt; **Workflow Editor welcome**. In the UI page record for workflow\_editor\_welcome, scroll to the **Versions** related list. Select the row for the version corresponding to the upgrade to Zurich, right-click and select **Revert to this version**.

## Workflow canvas

After you open or create a new workflow, the system displays the workflow canvas. On the canvas you interact with the Workflow Editor through several different elements: the canvas itself, the canvas tabs, the title bar, the palette, and the palette tabs.

The drawing canvas is where you add activities and configure transitions for checked out workflows. Add an activity by dragging it from the palette to the workflow in the canvas. For more information, see [Create a workflow](../../workflow-administration/task/t_CreateAWorkflow.md).

-   **Canvas tabs**: Contains tabs for accessing workflows being edited or created.
-   **Title bar:** Displays the workflow name and status. Provides a menu and controls for configuring, testing, and validating workflows.
-   **Canvas**: Provides the working surface for creating new workflows or editing existing ones.
-   **Palette tabs**: Contains tabs for accessing activities being edited or created.
-   **Palette**: Contains all available workflow activities and existing workflows you can use as subflows. Drag activities and subflows to the canvas to create new workflows or edit existing ones.

![](../image/WorkflowEditor.png "Workflow user interface")

-   **[Workflow palette](r_WorkflowPalette.md)**  
The default workflow palette contains workflow activities and existing workflows you can use as subflows.
-   **[Workflow editor title bar](r_WorkflowEditorTitleBar.md)**  
When a workflow is opened in the canvas, the title bar displays the workflow title and the workflow status in italics. Possible states are **Checked out by &lt;name&gt;** and **Published**.
-   **[Workflow editor keyboard navigation](workflow-keyboard-access.md)**  
The platform includes accessibility features that makes the interface accessible to users with disabilities.

**Parent Topic:**[Classic Workflow](../concept/c_WorkflowOverview.md)

