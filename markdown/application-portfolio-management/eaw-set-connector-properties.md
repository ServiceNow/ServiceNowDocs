---
title: Set shape connector properties in Enterprise Modeling and Visualization
description: Configure the relationship type or visual style of a connector between shapes in an enterprise modeling diagram.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-set-connector-properties.html
release: australia
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [connector, connector properties, relationship type, ArchiMate, line style]
breadcrumb: [Working with Enterprise Modeling and Visualization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Set shape connector properties in Enterprise Modeling and Visualization

Configure the relationship type or visual style of a connector between shapes in an enterprise modeling diagram.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Enterprise Modeling and Visualization icon.\).

3.  Select a diagram from the Diagrams page or create a diagram.

4.  Select a connector between two shapes.

    A toolbar appears above the connector.

5.  In the toolbar, configure the connector based on the notation of the connected shapes.

    -   For ArchiMate connectors \(both shapes are ArchiMate shapes\), open the **Link type** drop-down and select a relationship type.

        \[Omitted image "connector-line-archimate-drop-down.png"\] Alt text: Drop-down list showing ArchiMate relationship types, including Access, Serving, Association, Triggering, Influence, and other relationship variants.

    -   For non-ArchiMate and mixed connectors \(at least one shape is non-ArchiMate\), set the connector line properties using the toolbar controls.
    |Control|Option|
    |-------|------|
    |**Line style**|Solid|
    |Dashed|
    |Dotted|
    |**Start arrow** and **End arrow**|None|
    |Arrow|
    |Open arrow|
    |Open diamond|
    |Circle|
    |Bar|
    |**Icon**|None|
    |Initiating message flow|
    |Non-initiating message flow|

    \[Omitted image "connector-line-non-archimate.png"\] Alt text: Non-ArchiMate connector toolbar showing line style, start arrow, Flip, end arrow, icon, and T+ controls above a connector linking two shapes.

    |Number|Control|Description|
    |------|-------|-----------|
    |1|**Line style**|Sets the connector line to solid, dashed, or dotted.|
    |2|**Start arrow**|Sets the arrowhead style at the starting end of the connector.|
    |3|**Swap direction**|Reverses the connector orientation, switching the left and right sides.|
    |4|**End arrow**|Sets the arrowhead style at the ending end of the connector.|
    |5|**Icon**|Adds a BPMN message flow decorator icon to the connector.|
    |6|**T+**|Adds a text label to the connector.|

6.  To reverse the connector direction, select **Swap direction**.

7.  To add a text label to the connector, select **T+**.

    For details, see [Add labels to connector lines between shapes in a diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-add-labels-to-connector-lines.md).


**Parent Topic:**[Working with Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-ent-model-and-visual.md)

**Related topics**  


[Create a blank diagram using modeling in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-create-diagram.md)

[Shape connector properties in Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-connector-properties.md)

[Add labels to connector lines between shapes in a diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-add-labels-to-connector-lines.md)

[Working with ArchiMate Shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-archimate-shapes.md)

[Exploring Enterprise Modeling and Visualization in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling.md)

