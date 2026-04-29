---
title: Working with Enterprise Modeling and Visualization
description: Enterprise Modeling and Visualization provides a structured, visual framework for managing the complex relationships between IT systems, business processes, and organizational goals.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Working with Enterprise Modeling and Visualization

Enterprise Modeling and Visualization provides a structured, visual framework for managing the complex relationships between IT systems, business processes, and organizational goals.

With Enterprise Modeling and Visualization, you can create and maintain architecture diagrams using built‑in shape libraries such as General, Common Service Data Model, Amazon Web Services, Enterprise Architecture Extended, ArchiMate, and Business Process Model and Notation. You can connect shapes with relationship lines and label connectors to represent architectural relationships.

Associate shapes with existing records, such as business applications, capabilities, and application services, and use the side panel to view or update record details directly from the canvas.

You can manage diagram evolution by saving changes as new versions. Versioning enables you to maintain a history of architecture decisions and switch between versions using the version selector. You can also compare different versions of a diagram and generate a summary of the changes.

The workspace supports collaboration and governance by enabling you to share diagrams with stakeholders and submit them for review and approval using the built‑in approval workflow. After approval, you can synchronize the diagram with your repository to update the underlying records.

**Note:**

After upgrading from Q2 2025 or Q3 2025 releases to the Q4 2025 release of Enterprise Architecture Workspace, you might observe that newly created shapes display color, while existing shapes for the same entity don’t.

The Q4 2025 release of Enterprise Architecture Workspace release introduced color styling to the shape library. Consequently, diagrams created in Q3 don’t display color. Following the upgrade, new shapes added to these older diagrams display color, but the previously existing shapes remain uncolored.

To update the shapes in the previously created diagrams, do the following:

-   For upgrades from Q3 to Q4- You must explicitly run the relevant fix script \(script name: Clean edges and synchronize shape names and met", sys\_id: "2a63972eff22621076fdffffffffffbe\). This is because the script was present in the Q3 release and has been modified for Q4.
-   The script runs automatically as part of the upgrade process.

-   **[View all shape libraries](../../task/eaw-task/eaw-view-shape-libraries.md)**  
View all shape libraries available for the Enterprise Modeling and Visualization in the Enterprise Architecture Workspace.
-   **[View configuration for Enterprise Architecture Workspace](../../task/eaw-task/eaw-view-modeling-config.md)**  
View all the configuration details of Enterprise Architecture Workspace.
-   **[View all entities](../../task/eaw-task/eaw-view-entity-config.md)**  
View all entities available for the Enterprise Modeling and Visualization in the Enterprise Architecture Workspace.
-   **[View relationships configurations](../../task/eaw-task/eaw-view-relationships.md)**  
View all relationship configurations available for the Enterprise Modeling and Visualization in the Enterprise Architecture Workspace.
-   **[Create a blank diagram using modeling in the EA Workspace](../../task/eaw-task/eaw-modeling-create-diagram.md)**  
Create a diagram and synchronize it to the ServiceNow database.
-   **[Add labels to connector lines between shapes in a diagram](../../task/eaw-task/eaw-modeling-add-labels-to-connector-lines.md)**  
You can enhance diagram clarity in Enterprise Modeling and Visualization by adding a descriptive text on the connector line between shapes. Connector line labels clarify the nature of the relationship between shapes, annotate the data flow direction, and provide contextual information.
-   **[Working with business capability map](eaw-work-with-bc-map.md)**  
Model your business capabilities map using the Enterprise Modeling and Visualization. Update existing capability maps by adding other business capabilities and business applications.
-   **[Working with business hierarchy map](eaw-work-with-ba-map.md)**  
Model your business application hierarchy using the Enterprise Modeling and Visualization. Update an existing business hierarchy map by adding more shapes and relationships.
-   **[Working with business process map](eaw-work-with-bp-map.md)**  
Working with business process diagrams in Enterprise Modeling and Visualization.A business process modeling BPMN \(Business Process Model and Notation\) diagram is a visual representation of a structured sequence of tasks aimed at achieving specific outcomes. It helps you to establish a shared understanding of processes, identify inefficiencies or bottlenecks, optimize and streamline workflows.
-   **[Working with ArchiMate Shapes](eaw-work-with-archimate-shapes.md)**  
ArchiMate® shapes are the industry-standard elements used by enterprise architects to create diagrams that represent relationship across different domains of an enterprise. These shapes are used to model business, application, motivation, physical, strategy, and technology layers.
-   **[Working with Amazon Web Services \(AWS\) shapes](eaw-work-with-aws-shapes.md)**  
AWS is a cloud computing platform, used for cloud migration, application hosting, and digital transformation, making it critical for enterprise architecture planning. AWS shapes are part of the Cloud Architecture modeling capability. They enable architects to visualize AWS cloud components, model hybrid architectures, and support cloud migration planning and future-state architecture design.
-   **[Working with CSDM shapes](eaw-work-with-csdm-shapes.md)**  
Common Service Data Model \(CSDM\) is a standardized framework and CMDB data model provided by ServiceNow. It defines service-related terms, tables, and relationships across the Now Platform to ensure consistency in how services, applications, and infrastructure are represented. In Enterprise Architecture Workspace, CSDM shapes are visual elements that represent entities on diagrams for modeling and analysis.
-   **[Working with custom shapes](eaw-working-custom-shapes.md)**  
Custom shapes represent specific elements that are unique to your organization. Manage custom shapes, create diagram actions for the shapes in the Enterprise Architecture Workspace.
-   **[Convert a shape to a group shape](../../task/eaw-task/eaw-modeling-group-ungroup-shape.md)**  
Group shapes enable you to combine multiple related shapes into a single container for better organization and clarity in diagrams. It’s useful for representing logical groupings such as a set of applications under a business capability, related processes under a value stream stage.
-   **[Expand or collapse a group shape](../../task/eaw-task/eaw-modeling-expand-collapse-shape.md)**  
The expand and collapse functionality for a group shape helps in simplifying visualization, improves focus, and supports hierarchical modeling.
-   **[Download a modeling diagram as an image](../../task/eaw-task/eaw-modeling-download-diagram.md)**  
Download a diagram as an image to share it with other stakeholders with offline access or use it in the presentations.
-   **[Reorder shapes categories](../../task/eaw-task/eaw-modeling-reorder-shapes-cat.md)**  
Reordering shape categories helps architects customize the panel for faster access to frequently used shapes.
-   **[Show or hide shapes panel](../../task/eaw-task/eaw-modeling-show-hide-shapes-panel.md)**  
Show or hide the Shapes Panel to optimize your workspace for different tasks.
-   **[Switch to list or grid view of shapes panel](../../task/eaw-task/eaw-modeling-shapes-grid-list-view.md)**  
Switch between List View and Grid View in the shapes panel according to your modeling needs.
-   **[Search shapes in a diagram](../../task/eaw-task/eaw-filter-shapes.md)**  
Search for a shape in the Shapes palette of a diagram.
-   **[Add related records in the modeling diagram](../../task/eaw-task/eaw-modeling-add-related-records.md)**  
Fetch and add a related record to the selected shape in a diagram.
-   **[Share a modeling diagram](../../task/eaw-task/eaw-modeling-share-diagram.md)**  
Share your draft diagrams with individuals and groups and define access levels for them to view and modify the diagram.
-   **[Commit diagram changes](../../task/eaw-task/eaw-modeling-sync-diagram-servicenow.md)**  
Synchronize an approved diagram and all its elements to the database.
-   **[Save as a new version](../../task/eaw-task/eaw-modeling-save-as-new.md)**  
Copy an existing diagram and create a version for it within the selected architectural artifact. You can update the new version as required.
-   **[Add or edit diagram version details](../../task/eaw-task/eaw-add-or-edit-diagram-version-details.md)**  
You can add or edit version-specific details for a diagram to improve change management and compliance. Adding diagram version details ensures better clarity between all stakeholders in the context of the diagram and timelines.
-   **[Duplicate a modeling diagram](../../task/eaw-task/eaw-modeling-duplicate.md)**  
You can make a copy of an existing diagram that you created and modify the duplicate diagram according to your requirement.
-   **[Submit a modeling diagram for approval](../../task/eaw-task/eaw-modeling-submit-for-approval.md)**  
Send your draft modeling diagrams for approval. After receiving the approval, you can commit the diagram to the database. The approval process can be done through a configured workflow. By default, the approval request is submitted to the Enterprise Architect group.
-   **[Synchronize a shape to the database](../../task/eaw-task/eaw-modeling-sync-shape.md)**  
Add a shape to a diagram. Synchronize the shape to the database by mapping the shape to an existing CI or adding a CI.
-   **[Approve or reject a modeling diagram request](../../task/eaw-task/eaw-approve-diagram-req.md)**  
As an Enterprise Architect, approve or reject a Enterprise Modeling and Visualization diagram requests submitted by other users.
-   **[Delete a shape](../../task/eaw-task/eaw-modeling-delete-shape.md)**  
Delete a shape and all of its relationships from a diagram.
-   **[Delete Enterprise Modeling and Visualization diagrams](../../task/eaw-task/eaw-modeling-delete-diagram.md)**  
You can delete diagrams from the Enterprise Modeling and Visualization All Diagrams page, confirming only the relevant and current diagrams are available.
-   **[Generate a document from a diagram](../../task/eaw-task/create-documents-for-diagrams.md)**  
Generate documents from the Enterprise Modeling and Visualization diagrams page.
-   **[View documents for a diagram](../../task/eaw-task/view-docs-for-diagram.md)**  
View documents that are generated for a diagram from the Enterprise Modeling and Visualization diagrams page.

**Parent Topic:**[Managing Enterprise Architecture Workspace](eaw-managing-ea-workspace.md)

**Related topics**  


[Exploring Enterprise Modeling and Visualization in the EA Workspace](eaw-modeling.md)

[Configure Enterprise Modeling and Visualization](eaw-setup-modeling.md)

[Compare Enterprise Modeling and Visualization diagrams](../../../now-assist-ea/task/compare-modeling-diagrams.md)

