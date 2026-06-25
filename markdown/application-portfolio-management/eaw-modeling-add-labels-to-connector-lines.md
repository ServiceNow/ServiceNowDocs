---
title: Add labels to connector lines between shapes in a diagram
description: You can enhance diagram clarity in Enterprise Modeling and Visualization by adding a descriptive text on the connector line between shapes. Connector line labels clarify the nature of the relationship between shapes, annotate the data flow direction, and provide contextual information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling-add-labels-to-connector-lines.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 1
keywords: [connector, connector label, label]
breadcrumb: [Working with Enterprise Modeling and Visualization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Add labels to connector lines between shapes in a diagram

You can enhance diagram clarity in Enterprise Modeling and Visualization by adding a descriptive text on the connector line between shapes. Connector line labels clarify the nature of the relationship between shapes, annotate the data flow direction, and provide contextual information.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Enterprise Modeling and Visualization icon.\).

3.  Select a diagram from the Diagrams page where you want to add labels to the connector lines.

4.  Select a connector line.

    A toolbar appears above the connector. The toolbar shows different controls depending on the notation of the connected shapes:

    -   If both connected shapes are ArchiMate shapes, the toolbar shows the **Relationship type** drop-down, the **Swap direction** control, and the **T+** button.

        \[Omitted image "connector-line-archimate.png"\] Alt text: ArchiMate connector toolbar showing the relationship type list, Flip control, and T+ button.

    -   If at least one connected shape is non-ArchiMate, the toolbar shows the **Line style**, **Start arrow**, **Swap direction**, **End arrow**, **Icon**, and **T+** controls.

        \[Omitted image "connector-line-non-archimate.png"\] Alt text: Non-ArchiMate connector toolbar showing line style, start arrow, Flip, end arrow, icon, and T+ controls.

5.  Select **T+** in the toolbar and enter a label for the connector line.


## Result

The connector line label is added to the diagram.\[Omitted image "text-added-connector-line.png"\] Alt text: Label added to connector line.

**Parent Topic:**[Working with Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-ent-model-and-visual.md)

**Related topics**  


[Exploring Enterprise Modeling and Visualization in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling.md)

[Shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-connector-properties.md)

[Set shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-set-connector-properties.md)

