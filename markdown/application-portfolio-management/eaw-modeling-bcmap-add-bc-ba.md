---
title: Add a business capability or business application to the capability map
description: Add a new or existing business capability or business application to the capability map using the Enterprise Modeling and Visualization.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Enterprise Modeling and Visualization in the EA Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add a business capability or business application to the capability map

Add a new or existing business capability or business application to the capability map using the Enterprise Modeling and Visualization.

## Before you begin

Role required: sn\_apm.apm\_user

**Note:** You must have the Owner or Editor access to the artifact or diagram.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Modeling icon \(![Modeling](../../image/eaw-image/modeling/icon-modeling-logo.png)\).

3.  Create a new diagram or select an existing diagram from the Diagrams page.

    By default, two levels of capability hierarchy are displayed. Use the down arrow in a capability box to expand and see the next level capabilities and associated business applications.

4.  Select the **Add** drop-down menu and then select **Business Capability** or **Business Application**.

    ![add a business capability or business application to a capability map](../../image/eaw-image/modeling/add-ba-or-bc-to-bcmap.png)A new business capability or business application shape gets added to the canvas.

5.  Select the newly added shape and select the Open the side panel icon \(![Open side panel](../../image/eaw-image/modeling/icon-open-side-panel.png)\) to open the side panel in the canvas.

6.  Select and map an existing business capability or business application or create a new one.

    -   To map an existing CI, select the **Choose Existing** button and select a CI from the drop-down list.

        **Note:** For capabilities, only level 0 capabilities are displayed in the list. Capabilities that are already available in the map aren’t displayed in the list to select.

    -   To create a CI, select the **Create New** button and enter the details.
7.  Drag the configuration item \(CI\) to capability to create a relationship.

    The border of the configuration item \(CI\) box changes to dotted lines. After you commit the diagram successfully, the border line of the box changes to a solid line.

8.  Apply colors to the capabilities as required.

9.  Send the diagram for approval.

    After receiving the approval, you can see the **Commit changes** button. Use the **Commit changes** button to synchronize the diagram to the database.

10. Select **Commit changes** to synchronize the diagram to the database.

    This option is available only when the diagram is approved. For more information, see [Synchronize a shape to the database](eaw-modeling-sync-shape.md).

11. Select **Share** to share the diagram with individuals or groups.

    For more information, see [Share a modeling diagram](eaw-modeling-share-diagram.md).

12. Select the More Actions menu \(![More actions menu.](../../image/icon-three-dot-menu-eaw.png)\) to perform the following actions:

    -   **Save as new version**: Select this option to create a version for the selected diagram. The version number is automatically added in the Version number field, and it isn’t editable.
    -   **Duplicate**: Select this option to duplicate the diagram.
    -   **Submit for approval**: Select this option to submit the diagram for approval. The approval process can be done through a configured workflow. By default, the approval request is submitted to the Enterprise Architect group.

**Parent Topic:**[Enterprise Modeling and Visualization in the EA Workspace](../../concept/eaw-concept/eaw-modeling.md)

**Related topics**  


[Create a diagram for a business capability map](eaw-modeling-bc-map.md)

[Update a business capability map](eaw-modeling-update-bc-map.md)

