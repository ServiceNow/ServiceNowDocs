---
title: Exploring Enterprise Modeling and Visualization in the EA Workspace
description: Enterprise Modeling and Visualization in EA Workspace helps you with diagramming and modeling capabilities and enable you to model the future state of your IT and its relationship to the business landscape.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling.html
release: australia
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 10
breadcrumb: [Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Exploring Enterprise Modeling and Visualization in the EA Workspace

Enterprise Modeling and Visualization in EA Workspace helps you with diagramming and modeling capabilities and enable you to model the future state of your IT and its relationship to the business landscape.

\[Omitted video\] Description: Enterprise Modeling and Visualization overview

You can use the Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\] functionality in EA Workspace to create diagrams for your applications hierarchy and associate them with architectural artifacts. These diagrams enable decision makers to make informed decisions.

Creating diagrams helps you in the following:

-   Visual representation: Diagrams and models represent complex enterprise structures, processes, and relationships for stakeholders including executives and IT teams.
-   Effective communication: Diagrams provide a shared visual language for technical and non-technical stakeholders, supporting collaboration across teams and departments.
-   Improved decision making: Decision makers can assess the impact of proposed changes, evaluate scenarios, and identify potential risks before implementing strategies or projects.
-   Alignment with business goals: Diagrams and models help align IT initiatives with overall business goals, providing a view of the business and verifying that IT investments are strategically aligned with business goals.
-   Change management: Modeling capabilities illustrate how changes affect the enterprise, supporting planning and execution of transformations with minimal disruption.
-   Regulatory and governance: Modeling provides a structured framework for managing architectural artifacts and documenting adherence to architectural guidelines.
-   Efficiency and cost reduction: Identifying redundancies, optimizing processes, and streamlining operations can help reduce costs and improve operational efficiency.

\[Omitted image "modeling-home.png"\] Alt text: Modeling page

**Note:** You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

## Install the Enterprise Modeling and Visualization application

You can install the Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\] from the ServiceNow Store.

## Working with diagrams

-   **Shapes**: Use different shapes to create a diagram. Available shapes are:

    -   General shapes
    -   AWS shapes
    -   CSDM shapes
    -   EA Extended shapes
    -   ArchiMate® shapes \(ArchiMate is a registered trademark of The Open Group\)
    -   BPMN shapes
    \[Omitted image "modeling-shapes-library.png"\] Alt text: Shapes libray

    Use the Toggle Shape Library icon to show or hide the shapes panel on the canvas.

    Use the Switch to List or Grid view icon to switch between list view and grid view of the shapes for all the shape libraries.

    You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.

    You can also adjust the size of shapes by selecting a shape and then drag any of its edges or corner handles. Dragging outward increases the shape dimensions; dragging inward reduces its size.

    When you hover over a shape icon in the **Shapes** panel, a preview popover appears to the right of the panel showing a larger view of the shape and its label. Moving to a different shape icon, using either the mouse or the arrow keys, updates the popover to the new shape. The popover closes when you move the mouse away from the icon, press Tab on the keyboard, start dragging a shape, or scroll the panel.

-   **Label connector lines**: Select a connector line between shapes in a diagram and select **T+** in the connector toolbar to add a label. For more information, see [Add labels to connector lines between shapes in a diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-add-labels-to-connector-lines.md).

    You can perform the following actions for the labels:

    -   Add multiple labels on a single relationship line
    -   Drag and move labels
    -   Delete individual labels without deleting the relationship
    -   Use undo or redo action for a label
    **Note:** In read-only mode or after the diagram is submitted for approval, label actions are unavailable.

-   **Connector line properties**: Select a connector between two shapes to display a toolbar above the connector. The toolbar has two forms depending on the notation of the connected shapes:

    -   If both connected shapes are ArchiMate shapes, the toolbar shows the following controls:

        -   **Relationship type**: Sets the ArchiMate relationship type from a predefined list, including Access, Aggregation, Assignment, Association, Composition, Flow, Influence, Realization, Serving, Specialization, Triggering, and Used by.
        -   **Swap direction**: Reverses the connector orientation, switching the left and right sides.
        -   **T+**: Adds a text label to the connector.
        \[Omitted image "connector-line-archimate.png"\] Alt text: ArchiMate connector toolbar showing the relationship type list, Flip control, and T+ button above a connector linking two shapes.

    -   If at least one connected shape is a non-ArchiMate shape \(for example, a CSDM or AWS shape\), or when connecting shapes from two different notations, the toolbar shows the following controls:

        -   **Line style**: Sets the connector line to solid, dashed, or dotted.
        -   **Start arrow**: Sets the arrowhead style at the starting end of the connector.
        -   **Swap direction**: Reverses the connector orientation, switching the left and right sides.
        -   **End arrow**: Sets the arrowhead style at the ending end of the connector.
        -   **Icon**: Adds a BPMN message flow decorator icon to the connector.
        -   **T+**: Adds a text label to the connector.
        \[Omitted image "connector-line-non-archimate.png"\] Alt text: Non-ArchiMate connector toolbar showing line style, start arrow, Flip, end arrow, icon, and T+ controls above a connector linking two shapes.

    For more information, see [Shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-connector-properties.md) and [Set shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-set-connector-properties.md).

-   **Version**: This field enables you to view and open a different version of the diagram.

    \[Omitted image "modeling-version-selection.png"\] Alt text: Version drop-down

-   **View details**: Use this option to view version-specific details of your diagram such as version label, description, and planned rollout date.

    \[Omitted image "version-details-diagram.png"\] Alt text: View details pop-up window

-   **Undo** and **Redo**: Use this option to revert or reinstate recent changes made to a diagram. You can also use the keyboard shortcuts to perform the undo and redo action.

    \[Omitted image "diagram-changes-undo-redo.png"\] Alt text: Undo and Redo buttons highlighted on a diagram page.

-   **Align and distribute shapes**: Select two or more shapes on the canvas to align them to a common edge or center. Select three or more shapes to also distribute them at equal spacing. For more information, see [Align and distribute shapes in a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-align-distribute-shapes.md).

    \[Omitted image "modeling-align-options.png"\] Alt text: The alignment and distribution options available on the diagram canvas page.

-   **Share**: Use this option to share the diagram with your peers.
-   **Commit changes**: Use this option to synchronize the diagram to the repository. This option is available only when the diagram is approved.
-   **Save as new version**: Use this option to create a version of the diagram within the same artifact.
-   **Duplicate**: Use this option to duplicate an existing diagram and save it as a new artifact.

    \[Omitted image "modeling-options.png"\] Alt text: Modeling options

-   **Open side panel**: Select a shape in the diagram to see this option. Use this option to open the selected object details in a side panel. If the shape is connected to an existing ServiceNow element, the details are fetched from the database and shown in the side panel. Update the details as required. You can select the Full details link to open the full form.

    \[Omitted image "modeling-open-side-panel.png"\] Alt text: Side panel

-   **Add related records**- Select a shape in the diagram to see this option. Use this option to fetch and add the objects and their relationships with reference to the selected object.

    \[Omitted image "modeling-add-related-records.png"\] Alt text: Add related records

-   **More actions**- Select the three dots menu to see the following options:

    \[Omitted image "modeling-more-actions.png"\] Alt text: More actions on diagram

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

-   **[Shapes to create a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-shapes.md)**  
The shapes available in Enterprise Modeling and Visualization help you create diagrams. You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.
-   **[Shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-connector-properties.md)**  
When you select a connector between two shapes in an enterprise modeling diagram, a toolbar appears above the connector. Use the toolbar to define the relationship type or visual style of the connector.
-   **[ArchiMate shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-archimate.md)**  
ArchiMate® shapes are industry-standard elements used by enterprise architects to create diagrams that represent relationships across different domains of an enterprise. ArchiMate is a registered trademark of The Open Group. Enterprise Modeling and Visualization supports ArchiMate shapes along with General and Enterprise Architecture shapes.
-   **[AWS shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-modeling-aws.md)**  
Enterprise Modeling and Visualization supports Amazon Web Services \(AWS\) shape libraries for modeling cloud architectures. These shapes enable architects to design future-state cloud diagrams aligned with CMDB and CSDM standards.
-   **[CSDM shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/align-with-csdm5.md)**  
ServiceNow CSDM data model defines standardized relationships between service-related objects in the CMDB. It ensures consistency across ITSM, ITOM, and EA practices. In Enterprise Architecture Workspace, CSDM shapes represent these objects visually in diagrams, enabling architects to model business capabilities, applications, services, and technical components in alignment with the Now Platform.
-   **[Custom shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-custom-shapes.md)**  
Custom shapes are the user-defined graphical elements that can be used to represent specific concepts, processes, systems, or roles in your diagrams. These shapes can be tailored to fit the unique needs of your organization, making your diagrams more meaningful and easier to understand.
-   **[Business process modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/business-process-modeling.md)**  
Business processes are a structured sequence of tasks that are grouped, helping to accomplish specific business outcomes. A business process modeling diagram or a BPMN \(Business Process Model and Notation\) diagram is a visual representation of a business process.

**Parent Topic:**[Exploring Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/explore-eaw.md)

**Related topics**  


[Working with Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-ent-model-and-visual.md)

[Configure Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-setup-modeling.md)

[Add or edit diagram version details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-or-edit-diagram-version-details.md)

[Shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-connector-properties.md)

[Set shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-set-connector-properties.md)

[Add labels to connector lines between shapes in a diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-add-labels-to-connector-lines.md)

[Approve or reject a modeling diagram request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-approve-diagram-req.md)

[Delete a shape](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-delete-shape.md)

[Delete Enterprise Modeling and Visualization diagrams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-delete-diagram.md)

