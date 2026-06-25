---
title: Add related records in the modeling diagram
description: Fetch and add specific related records to the selected shape in a diagram.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling-add-related-records.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Enterprise Modeling and Visualization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Add related records in the modeling diagram

Fetch and add specific related records to the selected shape in a diagram.

## Before you begin

Role required: sn\_apm.apm\_user and Owner or Editor access to the artifact or diagram

## About this task

You can add both upstream and downstream related entities to a shape in a diagram.

-   Upstream entities appear as the parents of a selected shape. They represent inputs, dependencies, or higher-level components that influence the selected shape. For example, for a business process, an upstream entity can be a business capability.
-   Downstream entities appear as children of the selected shape. They represent the outputs or consequences that are influenced by the selected shape. For example, for a business capability, a downstream entity can be a business application.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Enterprise Modeling and Visualization icon\).

3.  Select an existing diagram from the Diagrams page.

4.  Select a shape in the diagram and open the context menu.

5.  Open the Add related records pop-up window by selecting the Add related records icon \(\[Omitted image "icon-add-related-records.png"\] Alt text: Add related records icon\).

6.  Select the specific entities that you want to add to the diagram.

    -   Select the Expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Upstream** or **Downstream** to view the list of available related entities.
    -   Select the Expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to an entity type to view the individual records within that type.
    -   Select the check box next to the individual records that you want to add.
7.  Select **Add**.


## Result

The selected entities are added to the diagram for the object.

**Parent Topic:**[Working with Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-ent-model-and-visual.md)

**Related topics**  


[Share a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-share-diagram.md)

[Commit diagram changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-sync-diagram-servicenow.md)

[Save as a version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-save-as-new.md)

[Duplicate a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-duplicate.md)

[Submit a modeling diagram for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-submit-for-approval.md)

[Synchronize a shape to the database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-sync-shape.md)

[Delete a shape](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-delete-shape.md)

