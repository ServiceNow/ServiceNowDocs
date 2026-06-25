---
title: Update a business process map
description: Modify an existing business process map by adding new events, activities, or gateways.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling-update-bp-map.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with business process map, Working with Enterprise Modeling and Visualization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Update a business process map

Modify an existing business process map by adding new events, activities, or gateways.

## Before you begin

Role required: sn\_apm.apm\_user

**Note:** To update a diagram, you must have Owner or Editor access to the artifact or diagram.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Enterprise Modeling and Visualization icon\).

3.  Open an existing business process map from the Diagrams page.

4.  Add the required shapes and connections.

    Drag shapes from the **Shapes** palette to the canvas. BPMN shapes are organized into sub-categories — **Gateway**, **Event**, **Activity**, and **General**. For a full list of available shapes, see [Business Process Modeling Notation \(BPMN\) shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-bpmn-shapes.md).

    For activity shapes such as user task or service task, select the Open the side panel icon \(\[Omitted image "icon-open-side-panel.png"\] Alt text: Open side panel\) to update the details of the associated record.

    To change the style of a connector, select the relationship line and choose a line type from the list that appears directly on the line. BPMN shapes and general shapes have their own sets of line types.

5.  Select the More Actions context menu \(\[Omitted image "eaw-icon-menu.png"\] Alt text: More actions menu\) to delete a shape from the canvas.

6.  Select **Share** to share the diagram with individuals or groups.

    For more information, see [Share a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-share-diagram.md).

7.  Select the More Actions menu \(\[Omitted image "icon-three-dot-menu-eaw.png"\] Alt text: More actions menu.\) to perform the following actions:

    -   **Save as new version**: Select this option to create a version for the selected diagram. The version number is automatically added in the Version number field, and it is read-only. For more information, see [Save as a version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-save-as-new.md).
    -   **Duplicate**: Select this option to duplicate the diagram. For more information, see [Duplicate a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-duplicate.md).
    -   **Submit for approval**: Select this option to submit the diagram for approval. The approval process can be done through a configured workflow. By default, the approval request is submitted to the Enterprise Architect group. For more information, see [Submit a modeling diagram for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-submit-for-approval.md).
8.  Select **Commit changes** to synchronize the diagram to the database.

    This option is available only when the diagram is approved. For more information, see [Synchronize a shape to the database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-sync-shape.md).


**Parent Topic:**[Working with business process map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-bp-map.md)

**Related topics**  


[Create a diagram for a business process map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-bp-map.md)

[View all shape libraries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-shape-libraries.md)

[Business Process Modeling Notation \(BPMN\) shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-bpmn-shapes.md)

[Business process modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/business-process-modeling.md)

[Business process map diagrams from images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-bpm-diagram-from-image.md)

[Create a business process map diagram from an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-bpm-diag-from-image.md)

[Review and accept a Now Assist-generated business process map diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-review-ai-generated-bpm-diag.md)

