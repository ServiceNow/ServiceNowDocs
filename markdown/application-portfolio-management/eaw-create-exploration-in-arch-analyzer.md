---
title: Create an exploration in the architecture analyzer
description: You can create an exploration to begin analyzing relationships between architectural entities using the architecture analyzer in the Enterprise Architecture Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-create-exploration-in-arch-analyzer.html
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
-   To hide the left navigation pane and the **Add to canvas** boxes, select the toggle full-screen icon \(\[Omitted image "arch-anlyzer-expand-canvas.png"\] Alt text: Toggle full-screen icon\)
-   To hide just the left navigation pane, select the toggle sidebar icon \(\[Omitted image "arch-anlyzer-hide-side-panel.png"\] Alt text: Toggle sidebar icon\)
-   To clear all entities from the canvas and the selections made in the **Add to canvas** boxes, select the **Clear** button \(\[Omitted image "arch-anlyzer-clear-canvas.png"\] Alt text: Clear button icon\)
-   To download the exploration canvas in image format, select the download as an image icon \(\[Omitted image "arch-anlyzer-download-exploration.png"\] Alt text: Download icon\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Architecture Analyzer page by selecting the architecture analyzer icon \(\[Omitted image "arch-anlyzer-icon.png"\] Alt text: Architecture analyzer icon.\).

3.  Select **New** or select **+ New exploration**.

    An untitled exploration with an empty canvas is created.

    \[Omitted image "arch-anlyzer-blank-canvas.png"\] Alt text: Blank canvas in Architecture Analyzer.

    **Note:**

    -   You can double click an existing exploration and then select **+ New exploration** to createn an exploration.
    -   You can select an existing exploration to view the details.
4.  To add an entity to the canvas, perform the following:

    1.  Select the first **Add to canvas** box and then select the relevant entity.
    2.  Select the second box and then select the specific entity that you want to explore.

        \[Omitted image "arch-anlyzer-add-entity.png"\] Alt text: The architecture analyzer screen with the Add to canvas boxes highlighted.

5.  Select **Add**.

    The selected entity is displayed on the canvas.

6.  Select the added entity and then select the add related records icon \(\[Omitted image "icon-add-related-records.png"\] Alt text: Add related records icon\).

    The **Add related records** pop-up window appears.

    \[Omitted image "arch-anlyzer-add-rel-entities.png"\] Alt text: Add related records pop-up window on Architecture Analyzer page.

7.  Select the entities that you want to add.

    -   Select the Expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Upstream** or **Downstream** to view the list of available related entities.
    -   Select the check box next to the relevant entity.
    **Note:** If an entity has no associated upstream or downstream entities, the **Add related records** pop-up window displays no related entities.

8.  Select **Add**.

    The selected entities are added to the diagram for the original entity.

    \[Omitted image "arch-anlyzer.png"\] Alt text: Architecture analyzer screen with exploration on canvas.

    **Note:**

    -   To rename an exploration, select the more actions icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text: More actions menu icon\) and then select **Rename**.

        \[Omitted image "arch-anlyzer-rename.png"\] Alt text: Screenshot displaying the Rename button for an exploration in the architecture analyzer.

    -   To remove an exploration, perform the following:
        1.  Select the more actions icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text: More actions menu icon\) and then select **Delete**.

            \[Omitted image "arch-anlyzer-delete.png"\] Alt text: Screenshot displaying the Delete button for an exploration in the architecture analyzer.

        2.  In the **Delete** pop-up window, select **Delete**. The exploration is permanently deleted.

**Parent Topic:**[Working with architecture analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-architecture-analyzer.md)

**Related topics**  


[Exploring the architecture analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-explore-arch-analyzer.md)

