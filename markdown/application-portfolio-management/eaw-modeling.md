---
title: Exploring Enterprise Modeling and Visualization in the EA Workspace
description: The Enterprise Modeling and Visualization functionality in EA Workspace helps you with diagramming and modeling capabilities and enable you to model the future state of your IT and its relationship to the business landscape.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring Enterprise Modeling and Visualization in the EA Workspace

The Enterprise Modeling and Visualization functionality in EA Workspace helps you with diagramming and modeling capabilities and enable you to model the future state of your IT and its relationship to the business landscape.

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

![Modeling page](../../image/eaw-image/modeling/modeling-home.png)

## Installing the Enterprise Modeling and Visualization application

You can install the Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\] from the ServiceNow Store.

## Working with diagrams

-   **Shapes**: This section enables you to use different kinds of shapes to create a diagram. Available shapes are:

    -   General shapes
    -   Enterprise Architecture shapes
    -   ArchiMate® shapes \(ArchiMate is a registered trademark of The Open Group\)
    ![Shapes](../../image/eaw-image/modeling/modeling-shapes-section.png)

    You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.

    You can also adjust the size of shapes by selecting a shape and then drag any of its edges or corner handles. Pulling outward increases the shape's dimensions, while dragging inward reduces its size.

-   **Labels connector lines**: Select a connector line between shapes in a diagram to add a label for the connector line by selecting the **Select to add text** icon.

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

-   **[Shapes to create a modeling diagram](../../reference/eaw-reference/eaw-modeling-shapes.md)**  
The shapes available in the Enterprise Modeling and Visualization helps you create diagrams. You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.
-   **[Search shapes in a diagram](../../task/eaw-task/eaw-filter-shapes.md)**  
Search for a shape in the Shapes palette of a diagram.
-   **[Add labels to connector lines between shapes in a diagram](../../task/eaw-task/eaw-modeling-add-labels-to-connector-lines.md)**  
You can enhance diagram clarity in Enterprise Modeling and Visualization by adding a descriptive text on the connector line between shapes. Connector line labels clarify the nature of the relationship between shapes, annotate the data flow direction, and provide contextual information.
-   **[Create a diagram using modeling in the EA Workspace](../../task/eaw-task/eaw-modeling-create-diagram.md)**  
Create a hierarchical diagram and synchronize it to the ServiceNow database.
-   **[Create a diagram for a business capability map](../../task/eaw-task/eaw-modeling-bc-map.md)**  
Create and model your business capability map using the Enterprise Modeling and Visualization.
-   **[Update a business capability map](../../task/eaw-task/eaw-modeling-update-bc-map.md)**  
Modify an existing business capability map by adding new capabilities, business applications, or changing the hierarchy of the existing capabilities.
-   **[Add a business capability or business application to the capability map](../../task/eaw-task/eaw-modeling-bcmap-add-bc-ba.md)**  
Add a new or existing business capability or business application to the capability map using the Enterprise Modeling and Visualization.
-   **[Create diagram for a business hierarchy map](../../task/eaw-task/eaw-modeling-ba-map.md)**  
Create and model your business application hierarchy map using the Enterprise Modeling and Visualization.
-   **[Update a business application hierarchy map](../../task/eaw-task/eaw-modeling-update-ba-map.md)**  
Modify an existing business application hierarchy map by adding or removing shapes and relationships.
-   **[Business process modeling](business-process-modeling.md)**  
Business processes are a structured sequence of tasks that are grouped, helping to accomplish specific outcomes. A business process modeling diagram or a BPMN \(Business Process Model and Notation\) diagram is a visual representation of a business process.
-   **[ArchiMate shapes support in the Enterprise Modeling and Visualization](eaw-modeling-archimate.md)**  
ArchiMate® shapes are the industry standard shapes used by the Enterprise Architects to create diagrams with relationships among with different domains in the enterprise. ArchiMate is a registered trademark of The Open Group. Enterprise Modeling and Visualization supports ArchiMate shapes along with General and Enterprise Architecture shapes.
-   **[Custom shapes support in the Enterprise Modeling and Visualization](eaw-modeling-custom-shapes.md)**  
Custom shapes are the user-defined graphical elements that can be used to represent specific concepts, processes, systems, or roles in your diagrams. These shapes can be tailored to fit the unique needs of your organization, making your diagrams more meaningful and easier to understand.
-   **[Add related records in the modeling diagram](../../task/eaw-task/eaw-modeling-add-related-records.md)**  
Fetch and add a related record to the selected object in the diagram.
-   **[Share a modeling diagram](../../task/eaw-task/eaw-modeling-share-diagram.md)**  
Share your draft diagrams with individuals and groups and define access levels for them to view and modify the diagram.
-   **[Commit diagram changes](../../task/eaw-task/eaw-modeling-sync-diagram-servicenow.md)**  
Synchronize an approved diagram and all its elements to the database.
-   **[Save as a new version](../../task/eaw-task/eaw-modeling-save-as-new.md)**  
Copy an existing diagram and create a version for it within the selected architectural artifact. You can update the new version as required.
-   **[Add or edit diagram version details](../../task/eaw-task/eaw-add-or-edit-diagram-version-details.md)**  
You can add or edit version-specific details for a diagram to improve change management and compliance. Adding diagram version details ensures better clarity between all stakeholders in the context of the diagram and timelines.
-   **[Duplicate a modeling diagram](../../task/eaw-task/eaw-modeling-duplicate.md)**  
Make a copy of an existing diagram that you created and change according to your requirement.
-   **[Submit a modeling diagram for approval](../../task/eaw-task/eaw-modeling-submit-for-approval.md)**  
Send your draft modeling diagrams for approval. After receiving the approval, you can commit the diagram to the database. The approval process can be done through a configured workflow. By default, the approval request is submitted to the Enterprise Architect group.
-   **[Synchronize a shape to the database](../../task/eaw-task/eaw-modeling-sync-shape.md)**  
Add a shape to a diagram. Synchronize the shape to the database by mapping the shape to an existing CI or adding a CI.
-   **[Delete a shape](../../task/eaw-task/eaw-modeling-delete-shape.md)**  
Delete a shape and all of its relationships from a diagram.
-   **[Delete Enterprise Modeling and Visualization diagrams](../../task/eaw-task/eaw-modeling-delete-diagram.md)**  
You can delete diagrams from the Enterprise Modeling and Visualization All Diagrams page, confirming only the relevant and current diagrams are available.

**Parent Topic:**[Enterprise Architecture Workspace](../ea-workspace.md)

**Related topics**  


[Add or edit diagram version details](../../task/eaw-task/eaw-add-or-edit-diagram-version-details.md)

[Add labels to connector lines between shapes in a diagram](../../task/eaw-task/eaw-modeling-add-labels-to-connector-lines.md)

