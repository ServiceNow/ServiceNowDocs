---
title: Shape connector properties in Enterprise Modeling and Visualization
description: When you select a connector between two shapes in an enterprise modeling diagram, a toolbar appears above the connector. Use the toolbar to define the relationship type or visual style of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-connector-properties.html
release: australia
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [connector, connector properties, relationship type, ArchiMate]
breadcrumb: [Exploring Enterprise Modeling and Visualization in the EA Workspace, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Shape connector properties in Enterprise Modeling and Visualization

When you select a connector between two shapes in an enterprise modeling diagram, a toolbar appears above the connector. Use the toolbar to define the relationship type or visual style of the connector.

The toolbar has two forms depending on the notation of the connected shapes. You can also add a label to a connector to clarify the relationship between shapes, annotate the data flow direction, or provide contextual information.

## ArchiMate connectors

When both connected shapes are ArchiMate shapes, the toolbar shows the following controls:

|Control|Description|
|-------|-----------|
|**Relationship type**|Sets the ArchiMate relationship type from a predefined list.|
|**Swap direction**|Reverses the connector orientation, switching the left and right sides.|
|**T+**|Adds a text label to the connector.|

\[Omitted image "connector-line-archimate.png"\] Alt text: ArchiMate connector toolbar showing the relationship type list, Flip control, and T+ button above a connector linking two shapes.

The **Relationship type** drop-down provides the standard ArchiMate 3.2 relationship types, including Access, Aggregation, Assignment, Association, Composition, Flow, Influence, Realization, Serving, Specialization, Triggering, and Used by.

The **Access** relationship type is available in three variants: single-direction, bidirectional, and unspecified \(dotted\). The Association relationship type is available in two variants: directed and undirected.

## Non-ArchiMate and mixed connectors

When at least one connected shape is a non-ArchiMate shape \(for example, a CSDM or AWS shape\), or when connecting shapes from two different notations, the toolbar shows the following controls:

\[Omitted image "connector-line-non-archimate.png"\] Alt text: Non-ArchiMate connector toolbar showing line style, start arrow, Flip, end arrow, icon, and T+ controls above a connector linking two shapes.

|Number|Control|Description|
|------|-------|-----------|
|1|**Line style**|Sets the connector line to solid, dashed, or dotted.|
|2|**Start arrow**|Sets the arrowhead style at the starting end of the connector.|
|3|**Swap direction**|Reverses the connector orientation, switching the left and right sides.|
|4|**End arrow**|Sets the arrowhead style at the ending end of the connector.|
|5|**Icon**|Adds a BPMN message flow decorator icon to the connector.|
|6|**T+**|Adds a text label to the connector.|

**Parent Topic:**[Exploring Enterprise Modeling and Visualization in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling.md)

**Related topics**  


[Set shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-set-connector-properties.md)

[Create a blank diagram using modeling in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-create-diagram.md)

[Working with ArchiMate Shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-archimate-shapes.md)

[Working with CSDM shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-csdm-shapes.md)

[Working with custom shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-working-custom-shapes.md)

