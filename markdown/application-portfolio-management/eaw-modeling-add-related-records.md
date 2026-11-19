---
title: Add related records in the modeling diagram
description: Fetch and add a related record to the selected shape in a diagram.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/eaw-modeling-add-related-records.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Enterprise Modeling and Visualization in the EA Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add related records in the modeling diagram

Fetch and add a related record to the selected shape in a diagram.

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

4.  Select a shape in the diagram and then open the context menu and then the More Actions menu \(\[Omitted image "eaw-icon-menu.png"\] Alt text: More actions menu icon\).

5.  Open the **Add related records** pop-up window by selecting the Add related records icon \(\[Omitted image "icon-add-related-records.png"\] Alt text: Add related records icon\).

6.  Select the entities that you want to add to the diagram.

    -   Select the Expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Upstream** or **Downstream** to view the list of available related entities.
    -   Select the check box next to the relevant entity.
7.  Select **Add**.


## Result

The selected entities are added to the diagram for the object.

**Parent Topic:**[Enterprise Modeling and Visualization in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling.md)

**Related topics**  


[Share a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-share-diagram.md)

[Commit diagram changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-sync-diagram-servicenow.md)

[Save as a new version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-save-as-new.md)

[Duplicate a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-duplicate.md)

[Submit a modeling diagram for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-submit-for-approval.md)

[Synchronize a shape to the database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-sync-shape.md)

[Delete a shape](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-delete-shape.md)

