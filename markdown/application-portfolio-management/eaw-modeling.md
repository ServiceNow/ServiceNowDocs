---
title: Exploring Enterprise Modeling and Visualization in the EA Workspace
description: Enterprise Modeling and Visualization in EA Workspace helps you with diagramming and modeling capabilities and enable you to model the future state of your IT and its relationship to the business landscape.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Explore, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring Enterprise Modeling and Visualization in the EA Workspace

Enterprise Modeling and Visualization in EA Workspace helps you with diagramming and modeling capabilities and enable you to model the future state of your IT and its relationship to the business landscape.

Enterprise Modeling and Visualization overview 

You can use the Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\] functionality in EA Workspace to create diagrams for your applications hierarchy and associate them with architectural artifacts. These diagrams enable decision makers to make informed decisions.

Creating diagrams for your applications hierarchy helps you in the following:

-   Visual representation: The diagrams and models provide a visual representation of complex enterprise structures, processes, and relationships. This visual representation helps your stakeholders, including executives and IT to understand the complexities of the organization.
-   Effective communication: Diagrams serve as a common language that bridges the gap between technical and non-technical stakeholders. They enable effective communication and collaboration between different teams and departments within an organization.
-   Improved decision making: The diagramming and modeling capabilities enable decision makers to make informed decisions. They can assess the impact of proposed changes, evaluate different scenarios, and identify potential risks before implementing strategies or projects.
-   Alignment with business goals: Diagrams and models help you align your IT initiatives with overall business goals. They provide a holistic view of the business and confirm that IT 's investments are strategically aligned with business goals.
-   Change management: The modeling capabilities facilitate change management by illustrating how changes impact the entire enterprise. This helps plan and execute transformations that run smoothly and with minimal disruption.
-   Regulatory and governance compliance: Many regulatory agencies and standards organizations require documentation and adherence to architectural guidelines. Modeling helps you verify compliance and governance by providing a structured framework for managing architectural artifacts.
-   Efficiency and cost reduction: By identifying redundancies, optimizing processes, and streamlining operations, modeling and diagramming can lead to cost reductions and improvements in operational efficiency.

![Modeling page](../../image/eaw-image/modeling/modeling-home.jpg)

## Installing the Enterprise Modeling and Visualization application

You can install the Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\] from the ServiceNow Store.

## Working with diagrams

-   **Shapes**: This section enables you to use different kinds of shapes to create a diagram. Available shapes are:

    -   General shapes
    -   AWS shapes
    -   CSDM shapes
    -   EA Extended shapes
    -   ArchiMate® shapes \(ArchiMate is a registered trademark of The Open Group\)
    -   BPMN shapes
    ![Shapes library](../../image/eaw-image/modeling/modeling-shapes-library.png)

    Use the Toggle Shape Library icon to show or hide the shapes panel on the canvas.

    Use the Switch to List or Grid view icon to switch between list view and grid view of the shapes for all the shape libraries.

    You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.

    You can also adjust the size of shapes by selecting a shape and then drag any of its edges or corner handles. Pulling outward increases the shape dimensions, while dragging inward reduces its size.

-   **Label connector lines**: Select a connector line between shapes in a diagram to add a label for the connector line by selecting the **Select to add text** icon or double‑clicking the relationship line.

    You can perform the following actions for the labels:

    -   Add multiple labels on a single relationship line
    -   Drag and move labels
    -   Delete individual labels without deleting the relationship
    -   Use undo or redo action for a label
    **Note:** After submitting the diagram for approval or in read-only mode, you cannot perform any action on the labels.

    ![Click to add text button highlighted.](../../image/eaw-image/modeling/add-text-button-connector-line.png)

-   **Version**: This field enables you to view and open a different version of the diagram.

    ![Version drop-down](../../image/eaw-image/modeling/modeling-version-selection.png)

-   **View details**: Use this option to view version-specific details of your diagram such as version label, description, and planned rollout day.

    ![View details pop-up window](../../image/eaw-image/modeling/version-details-diagram.png)

-   **Undo** and **Redo**: Use this option to revert or reinstate recent changes made to a diagram. You can also use the keyboard shortcuts to perform the undo and redo action.

    ![Undo and Redo buttons highlighted on a diagram page.](../../image/eaw-image/modeling/diagram-changes-undo-redo.png)

-   **Share**: Use this option to share the diagram with your peers.
-   **Commit changes**: Use this option to synchronize the diagram to the repository. This option is available only when the diagram is approved.
-   **Save as new version**: Use this option to create a version of the diagram within the same artifact.
-   **Duplicate**: Use this option to duplicate an existing diagram and save it as a new artifact.

    ![Modeling options](../../image/eaw-image/modeling/modeling-options.png)

-   **Open side panel**: Select a shape in the diagram to see this option. Use this option to open the selected object details in a side panel. If the shape is connected to an existing ServiceNow element, the details are fetched from the database and shown in the side panel. Update the details as required. You can select the Full details link to open the full form.

    ![Side panel](../../image/eaw-image/modeling/modeling-open-side-panel.png)

-   **Add related records**- Select a shape in the diagram to see this option. Use this option to fetch and add the objects and their relationships with reference to the selected object.

    ![Add related records](../../image/eaw-image/modeling/modeling-add-related-records.png)

-   **More actions**- Select the three dots menu to see the following options:

    ![More actions on diagram](../../image/eaw-image/modeling/modeling-more-actions.png)

    -   **Delete shape from canvas** to remove the selected shape from the canvas.
    -   **Add relation** to add relationships with reference to the selected object.

## Keyboard navigation on the diagram page

Enterprise Modeling and Visualization supports keyboard navigation across the diagram canvas, panels, shapes, and dialogs.

You can use the keyboard to move between shapes, groups, pools, swimlanes, and nested elements on the canvas. Focus indicators clearly show the currently selected item. You can access shape and relationship context menu using the keyboard to open the side panel, view related records, add or edit relationship text, and perform actions such as delete or add relations.

The following table lists the keyboard shortcuts available for navigating:

|Key|Action|
|---|------|
|Tab or Shift + Tab|Move focus forward or backward between canvas elements, panels, and controls.|
|Arrow keys \(↑ ↓ ← →\)|Navigate between shapes, nested elements, libraries, lists, pools, and swimlanes.|
|Enter|Select the focused shape, relationship, or control.|
|Shift + Enter|Move focus to shape or relationship adornments.|

-   **[Shapes to create a modeling diagram](../../reference/eaw-reference/eaw-modeling-shapes.md)**  
The shapes available in Enterprise Modeling and Visualization help you create diagrams. You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.
-   **[ArchiMate shapes support in the Enterprise Modeling and Visualization](eaw-modeling-archimate.md)**  
ArchiMate® shapes are industry-standard elements used by enterprise architects to create diagrams that represent relationships across different domains of an enterprise. ArchiMate is a registered trademark of The Open Group. Enterprise Modeling and Visualization supports ArchiMate shapes along with General and Enterprise Architecture shapes.
-   **[AWS shapes support in the Enterprise Modeling and Visualization](ea-modeling-aws.md)**  
Enterprise Modeling and Visualization supports Amazon Web Services \(AWS\) shape libraries for modeling cloud architectures. These shapes enable architects to design future-state cloud diagrams aligned with CMDB and CSDM standards.
-   **[CSDM shapes support in the Enterprise Modeling and Visualization](align-with-csdm5.md)**  
ServiceNow CSDM data model defines standardized relationships between service-related objects in the CMDB. It ensures consistency across ITSM, ITOM, and EA practices. In Enterprise Architecture Workspace, CSDM shapes represent these objects visually in diagrams, enabling architects to model business capabilities, applications, services, and technical components in alignment with the Now Platform.
-   **[Custom shapes support in the Enterprise Modeling and Visualization](eaw-modeling-custom-shapes.md)**  
Custom shapes are the user-defined graphical elements that can be used to represent specific concepts, processes, systems, or roles in your diagrams. These shapes can be tailored to fit the unique needs of your organization, making your diagrams more meaningful and easier to understand.
-   **[Business process modeling](business-process-modeling.md)**  
Business processes are a structured sequence of tasks that are grouped, helping to accomplish specific business outcomes. A business process modeling diagram or a BPMN \(Business Process Model and Notation\) diagram is a visual representation of a business process.

**Parent Topic:**[Exploring Enterprise Architecture Workspace](../explore-eaw.md)

**Related topics**  


[Working with Enterprise Modeling and Visualization](eaw-work-with-ent-model-and-visual.md)

[Configure Enterprise Modeling and Visualization](eaw-setup-modeling.md)

[Add or edit diagram version details](../../task/eaw-task/eaw-add-or-edit-diagram-version-details.md)

[Add labels to connector lines between shapes in a diagram](../../task/eaw-task/eaw-modeling-add-labels-to-connector-lines.md)

[Approve or reject a modeling diagram request](../../task/eaw-task/eaw-approve-diagram-req.md)

[Delete a shape](../../task/eaw-task/eaw-modeling-delete-shape.md)

[Delete Enterprise Modeling and Visualization diagrams](../../task/eaw-task/eaw-modeling-delete-diagram.md)

