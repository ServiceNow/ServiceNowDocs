---
title: Flow diagramming view
description: Create and view flows as diagrams. See the paths a flow can follow and the connections between elements.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Flow diagramming view

Create and view flows as diagrams. See the paths a flow can follow and the connections between elements.

## Activation

Install Flow Diagramming from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

Enable the flow diagramming view of a flow to gain these benefits.

-   Add and edit Workflow Studio components within specific paths of a flow.
-   See the branches and paths a flow can follow.
-   See the relationships between Workflow Studio components.

## Flow Diagramming components

![Example flow displaying the eight user interface components of the flow diagramming view](../images/flow-diagramming-view-ui.png "Flow Diagramming user interface components")

The Flow diagramming view consists of these components.

-   **1. View selector**

    Switch between the flow diagramming view and the flow description view.

-   **2. Add a trigger**

    Select and configure a flow trigger. Flow diagramming view does not support some trigger types.

-   **3. Flow nodes**

    View and configure a flow component as a node. Each node displays these elements.

    -   The sequence of the flow component in the flow
    -   The icon representing the spoke or component type
    -   The name of the flow component
    -   The menu of available options for the flow component
    -   The paths available from this node
    **Note:** The flow diagramming view only displays nodes for supported flow components.

-   **4. Plus icons**

    Select and configure an action, flow logic, or subflow to insert along a specific path of the flow.

    **Note:** The flow diagramming view only displays options for supported flow components.

-   **5. Add a node**

    Select and configure an action, flow logic, or subflow at the end of the flow.

    **Note:** The flow diagramming view only displays options for supported flow components.

-   **6. Search nodes**

    Find all nodes that match your search criteria.

-   **7. Diagram view controls**

    Select the current focus of the view, set the zoom level, download the diagram, and select view options.

    -   Preview and zoom controls
    -   Download diagram as an image
    -   View options
-   **8. Node properties**

    Configure the properties of the currently selected node.


## Preview and zoom controls

Set the current focus of the view by selecting a region of the thumbnail image. Zoom in and out to see specific portions of the flow structure.

## Download diagram as an image

Download the current flow as an image in the Portable Network Graphic \(PNG\) format. Opens a dialog window to choose the location to save the file. The image only shows the nodes, connection lines, and order numbering. If the image is too big to fit into one file, the system creates multiple images for each section of the flow.

## View options

Set how nodes appear in the diagramming view.

-   **Details**

    Show or hide configuration details in a box beneath each node. The configuration details include conditions and data pill paths.

-   **Annotations**

    Show or hide the annotations available for each node. Annotations appear as italic text beneath each node.


## Supported flow components

The flow diagramming view supports a limited selection of flow components. Workflow Studio disables the flow diagramming view when a flow contains unsupported flow components.

-   **Annotations**

    The flow diagramming view supports adding and editing annotations to actions, flow logic, and subflows.

-   **Data Stream Actions**

    The flow diagramming view supports adding and editing data stream actions.

-   **Flow logic**

    The flow diagramming view only displays flows containing these flow logic types.

    -   Call a Workflow
    -   Do the following in parallel
    -   Do the following until
    -   Dynamic Flows
    -   Else If
    -   End Flow
    -   Exit Loop
    -   For Each
    -   Get Flow Outputs
    -   If
    -   Make a decision
    -   Placeholder
    -   Set Flow Variables
    -   Skip Iteration
    -   Try
    -   Wait for a duration of time
-   **Stages**

    The flow diagramming view displays the stages available to a flow.

-   **Subflows**

    The flow diagramming view supports adding and configuring subflows.

-   **Triggers**

    The flow diagramming view only displays flows with these trigger types.

    -   Record triggers
    -   Date triggers
    -   Inbound email
    -   Kafka Message
    -   MetricBase
    -   REST API - Asynchronous
    -   Service Catalog
    -   SLA Task

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

