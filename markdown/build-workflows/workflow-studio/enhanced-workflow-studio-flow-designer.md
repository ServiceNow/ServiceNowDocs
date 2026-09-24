---
title: Enhanced Workflow Studio flow designer
description: Create and manage flows from the enhanced Workflow Studio flow designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/enhanced-workflow-studio-flow-designer.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [workflow studio, flow designer]
breadcrumb: [Explore flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Enhanced Workflow Studio flow designer

Create and manage flows from the enhanced Workflow Studio flow designer.

## Benefits

We've enhanced Workflow Studio flow designer for speed, clarity, and control.

-   Faster rendering. Experience smooth, responsive interactions across actions.
-   Improved interface. Create and manage flows using a refined design and improved user experience.
-   Unified picker. Select actions, flow logic, subflow, AI skills, and AI agents all from one place.

## UI elements

\[Omitted image "enhanced-fd-ui-components-01.png"\] Alt text: Components one through seven of the enhanced UI

The enhanced Workflow Studio UI includes these new elements.

-   **1. Status messages**

    See status messages at the top of the design page.

-   **2. Return to standard UI button**

    Select this button to exit the enhanced UI and return to the standard UI.

-   **3. Data search**

    Search for data pills by name. The data pane displays the pills that contain your search query.

-   **4. Unified picker**

    Select any flow component from a single picker menu.

-   **5. Picker categories**

    Select a category to see the available components of that type. Options include Otto, Action, Subflow, and Logic.

-   **6. Component search**

    Search for flow components by name.

-   **7. Components search results**

    See the flow components that match your search results.


\[Omitted image "enhanced-fd-ui-components-02.png"\] Alt text: Components eight through eleven of the enhanced UI

-   **8. Highlighted input configuration**

    See the inputs available for configuration for the currently selected flow step.

-   **9. Add a step**

    Add a step to the end of a flow.

-   **10. Current data search**

    See the current name used to filter the Data pane. Select the X icon to clear the search.

-   **11. Data search results**

    See the data pills that match your search query. See the parent components of the data pill search.


## Supported flow components

As of the Brazil release, the enhanced Workflow Studio flow designer supports these flow components.

-   **Actions**

    The enhanced designer supports adding and editing all action types.

-   **Annotations**

    The enhanced designer supports adding and editing annotations to actions, flow logic, and subflows.

-   **Data Stream Actions**

    The enhanced designer supports adding and editing data stream actions.

-   **Flow logic**

    The enhanced designer only displays flows containing these flow logic types.

    -   Call a Workflow
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

    The enhnaced designer displays the stages available to a flow.

-   **Subflows**

    The enhanced designer supports adding and configuring subflows.

-   **Triggers**

    The enhanced designer only displays flows with these trigger types.

    -   Record triggers
    -   Date triggers
    -   Inbound email
    -   Kafka Message
    -   MetricBase
    -   REST API - Asynchronous
    -   Service Catalog
    -   SLA Task

## Unsupported features

As of Australia Patch 6, the enhanced Workflow Studio flow designer does not support creating flows and subflows. In addition, the Do the following in parallel flow logic is unsupported.

