---
title: Create an exploration in the architecture analyzer
description: You can create an exploration to begin analyzing relationships between architectural entities using the architecture analyzer in the Enterprise Architecture Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with architecture analyzer, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create an exploration in the architecture analyzer

You can create an exploration to begin analyzing relationships between architectural entities using the architecture analyzer in the Enterprise Architecture Workspace.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

In the Architecture Analyzer you can also perform the following:

-   You can add both upstream and downstream related entities to an entity on the architecture analyzer canvas.
    -   Upstream entities appear as the parents of a selected entity. They represent inputs, dependencies, or higher-level components that influence the selected entity. For example, for a business process, an upstream entity can be a business capability.
    -   Downstream entities appear as children of the selected entity. They represent the outputs or consequences that are influenced by the selected entity. For example, for a business capability, a downstream entity can be a business application.
-   To hide the left navigation pane and the **Add to canvas** boxes, select the toggle full-screen icon \(![Toggle full-screen icon](../../image/eaw-image/arch-anlyzer-expand-canvas.png)\)
-   To hide just the left navigation pane, select the toggle sidebar icon \(![Toggle sidebar icon](../../image/eaw-image/arch-anlyzer-hide-side-panel.png)\)
-   To clear all entities from the canvas and the selections made in the **Add to canvas** boxes, select the **Clear** button \(![Clear button icon](../../image/eaw-image/arch-anlyzer-clear-canvas.png)\)
-   To download the exploration canvas in image format, select the download as an image icon \(![Download icon](../../image/eaw-image/arch-anlyzer-download-exploration.png)\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Architecture Analyzer page by selecting the architecture analyzer icon \(![Architecture analyzer icon.](../../image/eaw-image/arch-anlyzer-icon.png)\).

3.  Select **New** or select **+ New exploration**.

    An untitled exploration with an empty canvas is created.

    ![Blank canvas in Architecture Analyzer.](../../image/eaw-image/arch-anlyzer-blank-canvas.png)

    **Note:**

    -   You can double click an existing exploration and then select **+ New exploration** to createn an exploration.
    -   You can select an existing exploration to view the details.
4.  To add an entity to the canvas, perform the following:

    1.  Select the first **Add to canvas** box and then select the relevant entity.
    2.  Select the second box and then select the specific entity that you want to explore.

        ![The architecture analyzer screen with the Add to canvas boxes highlighted.](../../image/eaw-image/arch-anlyzer-add-entity.png)

5.  Select **Add**.

    The selected entity is displayed on the canvas.

6.  Select the added entity and then select the add related records icon \(![Add related records icon](../../image/eaw-image/modeling/icon-add-related-records.png)\).

    The **Add related records** pop-up window appears.

    ![Add related records pop-up window on Architecture Analyzer page.](../../image/eaw-image/arch-anlyzer-add-rel-entities.png)

7.  Select the entities that you want to add.

    -   Select the Expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Upstream** or **Downstream** to view the list of available related entities.
    -   Select the check box next to the relevant entity.
    **Note:** If an entity has no associated upstream or downstream entities, the **Add related records** pop-up window displays no related entities.

8.  Select **Add**.

    The selected entities are added to the diagram for the original entity.

    ![Architecture analyzer screen with exploration on canvas.](../../image/eaw-image/arch-anlyzer.png)

    **Note:**

    -   To rename an exploration, select the more actions icon \(![More actions menu icon](../../image/eaw-image/eaw-icon-menu.png)\) and then select **Rename**.

        ![Screenshot displaying the Rename button for an exploration in the architecture analyzer.](../../image/eaw-image/arch-anlyzer-rename.png)

    -   To remove an exploration, perform the following:
        1.  Select the more actions icon \(![More actions menu icon](../../image/eaw-image/eaw-icon-menu.png)\) and then select **Delete**.

            ![Screenshot displaying the Delete button for an exploration in the architecture analyzer.](../../image/eaw-image/arch-anlyzer-delete.png)

        2.  In the **Delete** pop-up window, select **Delete**. The exploration is permanently deleted.

**Parent Topic:**[Working with architecture analyzer](../../concept/eaw-concept/eaw-work-with-architecture-analyzer.md)

**Related topics**  


[Exploring the architecture analyzer](../../concept/eaw-concept/eaw-explore-arch-analyzer.md)

