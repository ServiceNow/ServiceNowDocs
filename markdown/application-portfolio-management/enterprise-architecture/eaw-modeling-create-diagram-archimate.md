---
title: Create diagram using ArchiMate shapes and add relationships
description: Use the industry standard ArchiMate shapes to create modeling diagrams for your enterprise in the Enterprise Architecture Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-create-diagram-archimate.html
release: xanadu
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: task
last_updated: "2024-10-08"
reading_time_minutes: 3
breadcrumb: [ArchiMate shapes support in the Enterprise Modeling and Visualization, Explore Enterprise Modeling and Visualization, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create diagram using ArchiMate shapes and add relationships

Use the industry standard ArchiMate shapes to create modeling diagrams for your enterprise in the Enterprise Architecture Workspace.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

You can create a diagram with the combination of CSDM and ArchiMate shapes or you can use only the ArchiMate shapes. If you want to create the diagram with only ArchiMate shapes, you can skip including the name of the Business Application in the Create a business hierarchy map form. It creates a blank canvas.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Modeling\).

3.  Select **New** drop-down menu.

4.  Select **Business hierarchy map**.

5.  On the Create a business capability map form, fill in the details.

    For field information, see [Create a business hierarchy map form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-create-ba-map-form.md).

6.  Select **Create diagram**.

    A blank canvas gets created for the artifact.

7.  Add ArchiMate shapes to the canvas.

8.  Associate a CI to the shape by selecting a radio button.

    -   **Choose existing**- Select this radio button to associate the shape with an existing CI.
    -   **Create new**- Select this radio button to create a new CI for the selected shape.
9.  Select a connector line to update the relationship type.

    The Relationship side panel opens. Select a **Value** and **ArchiMate relationship type**. For more information on the ArchiMate shapes and relationships, see [ArchiMate shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-archimate.md).

10. Select a shape and add related records for the shape by selecting the \[Omitted image "icon-add-related-records.png"\] Alt text: Add related records icon.

    Th Add related records window opens. It lists the Entities with the number and Relationship type \(CI relationship or a Reference\).

11. Select the **Entities** that you want to include and then select **Add**.

    The selected entities are added to the diagram with the relationship showing in ArchiMate format. In the diagram, the dotted lines represent the Reference links and the solid lines represent the CI relationships.

12. Select **Commit changes** to synchronize the diagram to the database.

    This option is available only when the diagram is approved. For more information, see [Synchronize a shape to the database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-sync-shape.md).

13. Select **Share** to share the diagram with individuals or groups.

    For more information, see [Share a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-share-diagram.md).

14. Select the More Actions menu \(\[Omitted image "icon-three-dot-menu-eaw.png"\] Alt text: More actions menu.\) to perform the following actions:

    -   **Save as new version**: Select this option to create a version for the selected diagram. The version number is automatically added in the Version number field, and it isn’t editable. For more information, see [Save as a new version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-save-as-new.md).
    -   **Duplicate**: Select this option to duplicate the diagram. For more information, see [Duplicate a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-duplicate.md).
    -   **Submit for approval**: Select this option to submit the diagram for approval. The approval process can be done through a configured workflow. By default, the approval request is submitted to the Enterprise Architect group. For more information, see [Submit a modeling diagram for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-submit-for-approval.md).

**Parent Topic:**[ArchiMate shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/enterprise-architecture/eaw-modeling-archimate.md)

