---
title: Node map Experience Component release notes
description: Version history for the Node map Experience Component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-node-map-experience.html
release: store
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Node map Experience Component release notes

Version history for the Node map Experience Component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.3.0 - December 2025**
    -   Feature: Radial Layout for Node Map
    -   Description: The radial layout introduces a new way to visualize connections between nodes. It arranges nodes in a circular, ring-like pattern to highlight relationships and dependencies. Each node is positioned based on its connection to a related node, creating a clear and balanced visual representation of the network structure
    -   Use Case: Use the radial layout to illustrate relationships between enities such as tables in a database or interconnected systems where a circular visualization provides a clearer understanding of how nodes are connected to each other
-   **Version 25.6.0 - August 2025**
    -   Key features added:
        -   New layout type: Horizontal. Horizontal layout supports all key capabilities such as custom nodes, node animation, and supports all edge types
        -   Updated spacing behavior to improve space utilization.
    -   Removed unified node from the UI builder. Admins can still use it as a custom node in supported layouts
-   **Version 25.1.0 - February 2025**
    -   Suspend re-layout support in the Force layout
    -   Ability to control space between nodes in the Force layout
    -   Support for node shape to improve the connecting edges
    -   Support of reduced animation in Force layout
    -   Fixed bugs to improve popover and edge stability
-   **Version 24.10.1 - November 2024**
    -   Introduced a new 'force' layout to allow users to visualize any data in a force layout
    -   Support for multiple edges &amp; self referencing edges in the new layout
    -   Support for custom nodes in the new force layout
    -   Allowing configuration of custom popovers for nodes and edges
    -   Support to export a map as a PNG
    -   Added support for search on map on all layouts
    -   Addressed multiple defects to improve the experience
-   **Version 24.9.2 - August 2024**
    -   More configuration options for the control panel to allow customization
    -   Top down layout improvements:
        -   Node repositioning
        -   Added option to suspend relayout
        -   Visualization for adding a connection
-   **Version 22.1.3 - November 2022**
    -   New:
        -   New rich text multi-line tooltip
        -   Merging edges when too many edges between the same set of nodes
        -   Compact mode on nodemap
-   **Version 22.0.2 - August 2022**
    -   New layout layered-groups
        -   Group nodes expand as containers. Supporting nested group containers.
        -   Orthogonal edges: 90 degrees lines with more optimal edge routing
    -   Merging of edge ports
        -   Reducing the number of lines that enter/leave a node.
    -   More status colors for the default node macroponent
        -   Added support for now-icon for the node status
    -   Programmatic selection of nodes and edges
    -   Programmatic fit-to-screen

