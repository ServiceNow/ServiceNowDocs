---
title: Node Map component setup
description: The Node Map provides an interactive graph with nodes and edges. This component is available only on the ServiceNow Store.Specify the nodes and edges that the Node Map component displays. Configure the style, persisted state, context menus, and other aspects of how the nodes and edges are displayed.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.The Node Map requires a node macro component to render the nodes view. You can use the default node macro component or select a custom macro component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/node-map-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 27
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Node Map component setup

The Node Map provides an interactive graph with nodes and edges. This component is available only on the ServiceNow Store.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Node Map that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "node-map-content-tree.png"\] Alt text: Node map component in the page content tree.

2.  Select the Node Map component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Node Map label you created for your component in the content tree.
    The configuration options appear in the setup panel on the right.

    \[Omitted image "node-map-config-tab.png"\] Alt text: Shows the config panel for node map


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Node Map component properties

Specify the nodes and edges that the Node Map component displays. Configure the style, persisted state, context menus, and other aspects of how the nodes and edges are displayed.

### Available presets

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

-   **__Unified map__**

    This preset connects user interactions to the node map with expand/collapse, programmatic selection, and home node. This preset requires the **Unified map** controller.

    **Note:** This preset is intended for use with Configuration Management Database \(CMDB\) data and may not be suitable for other data.

    Properties included in this preset are:

    -   Node items
    -   Edge items
    -   Map layout
    -   Home node
    -   Fit to screen
    -   Expanded group nodes
    -   Hidden nodes
    -   Hidden edges
    -   Selected Element Id
    -   Disable edges context menu
    -   Disable 'show hidden connections'
    -   Control panel buttons
    -   Disable Collapse All
    -   Show error state
    -   Reduce motion

### Properties

<table id="table_fv5_2nm_fsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node items\[nodes\]

</td><td>

The node elements to draw on the map. Each node has its own node data object. For more information, see the example [Node items and edge items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/node-map-component-uib-setup.md).Object structure:

-   `id` \{String\} \(Required\): Unique ID for the node.
-   `groupIds` \{Array\}: Tells which groups this node is a member of. Currently only one group is supported.
-   `isInactive` \{Boolean\}: Sets the node as inactive/disabled. Special style is applied and interactions are blocked.
-   `isGroup` \{Boolean\}: Sets the node as being a group. A special style for groups is applied in runtime.
-   `hideExpandCollapse` \{Boolean\}: Hides the expand/collapse button on the actions bar for a group node.
-   `partition` \{Integer\}: Sets the relative order of node layers. Nodes with a lower partition number appear above nodes with higher numbers. To optimize the layout, the node map might automatically split nodes with the same partition value into multiple layers. The default value is `0`. This property applies only if the map layout is **layered-groups**.
-   `fixedLayer` \{number\}: Negative or positive integer defining the order of node layers. This property applies only if the map layout is **unified-vertical**.
-   `tooltipContent` \{String\}: Custom tooltip content in valid HTML that displays when moving a cursor over the node.
-   `width` \{Number\}: Sets fixed width in pixels for this node, overriding the global setting.
-   `height` \{Number\}: Sets fixed height in pixels for this node, overriding the global setting.
-   `viewData` \{Object\}: Contains any properties that the Node macro component receives. For an example, see [Choosing the node macro component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/node-map-component-uib-setup.md).

The `primaryLabel` and `secondaryLabel` properties are reserved for the primary and secondary labels of the node, respectively.


 **Note:**

-   The Node data object isn’t restrictive. Add any more properties that you need.
-   You can also set the node items through data binding. When doing so, bear in mind that the parameters of the nodes and of the edges must match to avoid UI Builder timing issues when updating client state variables. Therefore, wrap node and edge client state variables into one JSON object. For example, here you wrap the variables into the `data` object, which you would put into the client state script:

    ```
data = { "nodes":{}, "edges":{} }
    ```

When you update the state, also update the data client state and bind it to the properties. For example, bind the properties to the `data` client state like this:

    ```
nodes: @state.data.nodes 
edges: @state.data.edges 
    ```

And update the state in the client state script with this:

    ```
setState('data', data);
    ```

Here is a client script showing both the construction of the `data` object and the update to the state and the bound data client state:

    ```json
const nodes = []; // new nodes data
const edges = []; // new edges data
const data = {
        nodes,
        edges
    };
api.setState('data', data);
    ```


</td></tr><tr><td>

Edge items\[edges\]

</td><td>

Connection elements to draw as edges between the nodes. For more information, see the example [Node items and edge items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/node-map-component-uib-setup.md).Object structure:

-   `id` \{String\} \(Required\): Unique ID for the edge.
-   `style` \{solid\|dashed\}: The style of the edge line.
-   `direction` \{original\|reverse\|none\}: The arrow direction. The `none` direction hides the arrow.
-   `sourceId` \{String\} \(Required\): The ID of the source node.
-   `targetId` \{String\} \(Required\): The ID of the target node.
-   `label` \{String\}: The textual label.
-   `tooltipContent` \{String\}: Custom tooltip content in valid HTML that displays when moving a cursor over the edge.
-   `status` \{String\}: The status of an edge shown with a color. The choices are primary \(dark purple\), critical \(red\), selection-primary \(gray\), high \(orange\), warning \(gold\), moderate \(lilac\), info \(blue\), positive \(green\), teal, brown, gray, green, green-yellow, magenta, orange, pink, purple, yellow, and none \(gray\). The choices are associated with CSS properties in the theme, and their colors can be customized.

 **Note:**

-   The Edge data object isn’t restrictive. Add any more properties that you need.
-   You can also set this property through data binding. When doing so, bear in mind that the parameters of the nodes and of the edges must match to avoid UI Builder timing issues when updating client state variables. For more information, see the note for the nodes property.

</td></tr><tr><td>

Map layout\[layout\]

</td><td>

The layout for calculating the position of nodes and edges.Choices are:

-   **hierarchical-topdown** \(default\)
-   **layered-groups**
-   **unified-force**
-   **unified-vertical**
-   **horizontal**

**Note:** The "unified" layouts are optimized for use with Configuration Management Database \(CMDB\) data. They may not be suitable for other data.

</td></tr><tr><td>

Hide edge arrows\[hideEdgeArrows\]

</td><td>

When true, displays all edges as non-directional, without arrows.Default: **false**

</td></tr><tr><td>

Reduce spacing between nodes\[reduceNodeSpacing\]

</td><td>

Reduce vertical/horizontal space between nodes.Default: **false**

</td></tr><tr><td>

Merged edge segments\[mergeEdgeSegments\]

</td><td>

Merge edge lines for a more compact map view. This property applies only if the map layout is **layered-groups**.Default: **false**

</td></tr><tr><td>

Label scaling\[canLabelScale\]

</td><td>

Enables the label scaling.Default: **true**

</td></tr><tr><td>

Re-layout requested\[reLayoutRequested\]

</td><td>

An object that contains a timestamp that can be passed down to trigger a map re-layout.Default: **\{\\"timestamp\\": 1699889486659\}**

</td></tr></tbody>
</table><table id="table_rw4_qym_fsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node view macrocomponent\[nodeMacroponent\]

</td><td>

Reference or sys\_id of a macro component to use as a custom node representation. You can choose from any Next Experience Components or a page in your workspace. If you don’t make a choice, the default node is used. For more information, see [Choosing the node macro component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/node-map-component-uib-setup.md).Type: string

 Default: Node map default node

</td></tr><tr><td>

Node shape\[nodeShape\]

</td><td>

The shape of the nodes. Node map calculates edge length based on the node shape.Choices are:

-   Circle
-   Rectangle

Default: Rectangle

</td></tr><tr><td>

Width\[nodeWidthMode\]

</td><td>

Select how the widths of node macro components are defined globally. The choices are:-   **Fixed node width**: As specified in `nodeWidth`.
-   **Max node width**: Width set automatically but with the upper limit specified in `maxNodeWidth`. When a node exceeds this width, a horizontal scrollbar appears.
-   **Auto width**: Width set automatically with no limit. See the note after this table.

 Default: **Fixed node width**

</td></tr><tr><td>

Node width\[nodeWidth\]

</td><td>

The global node width in pixels when Width is set to **Fixed node width**.Default: **150**

</td></tr><tr><td>

Max node width\[maxNodeWidth\]

</td><td>

The maximum allowed width for nodes, defined in pixels.

</td></tr><tr><td>

Height\[nodeHeightMode\]

</td><td>

Select how the heights of node macro components are defined globally. The choices are:-   **Fixed node height**: As specified in `nodeHeight`.
-   **Max node height**: Automatic node height with the upper limit specified in `maxNodeHeight`. When a node exceeds this height, a vertical scrollbar appears.
-   **Auto height**: Automatic unrestricted node height \(auto\). See the note after this table.

 Default: **Fixed node height**

</td></tr><tr><td>

Node height\[nodeHeight\]

</td><td>

The fixed node height in pixels when **Height** is set to **Fixed node height**.Default: **123**

</td></tr><tr><td>

Node spacing\[nodeSpacing\]

</td><td>

Space between nodes in the Force layout. Use values between 1 and 1000.Default: 250

</td></tr><tr><td>

Max node height\[maxNodeHeight\]

</td><td>

The maximum height for all nodes, defined in pixels.

</td></tr><tr><td>

Default size\[nodeSize\]

</td><td>

The default size for nodes. Can be overridden in the node configuration.

</td></tr></tbody>
</table>**Note:** Regarding automatic node width and height:

-   Automatic sizing can only be used if nodes have their own size derived from the inner content. If the node macro component has a layout that stretches it to fit the container size, use the fixed size mode instead.
-   When the automatic node size is enabled, individual nodes can still be set to fixed size. To do that, set both `nodes[*].width` and `nodes[*].height` in pixel units for each fixed size node.
-   When the automatic node size is enabled, Node Map takes more time to render the entire graph. All node macro components have to finish rendering before Node Map can adjust the overall layout of the graph. This takes an amount of time proportional to the number of visible nodes.
-   Upon the initial loading, a temporary graph preview appears, which rearranges the nodes after they all have finished rendering. Similar behavior is expected when new nodes are added to a Node Map dynamically in the runtime.

<table id="table_eg4_wdn_fsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Home node\[homeNodeId\]

</td><td>

ID of the node to be set as 'Home.' In runtime, a special style is applied to identify the node.

</td></tr><tr><td>

Align to node ID\[alignToNodeId\]

</td><td>

Centers the viewport around the specified node.

</td></tr><tr><td>

Expanded group nodes\[expandedGroupNodeIds\]

</td><td>

Indicates which group nodes are expanded. These group nodes have a **Collapse** action in the action bar instead of an **Expand** action.

</td></tr><tr><td>

Hidden nodes\[hiddenNodeIds\]

</td><td>

IDs of nodes to hide. Hidden nodes participate in map layout but aren’t drawn and aren’t reachable on the map.

</td></tr><tr><td>

Hidden edges\[hiddenEdgeIds\]

</td><td>

IDs of edges to hide. Hidden edges participate in map layout but aren’t drawn and aren’t reachable on the map.

</td></tr><tr><td>

Inactive nodes \[inactiveNodeIds\]

</td><td>

A JSON array of nodes that you specify as inactive. Inactive nodes participate in map layout, but appear as inactive \(disabled\).

</td></tr><tr><td>

Inactive edges\[inactiveEdgeIds\]

</td><td>

A JSON array of edges that you specify as inactive. Inactive edges participate in map layout, but appear as inactive \(disabled\).

</td></tr><tr><td>

Manage element selection \[manageElementSelection\]

</td><td>

When turned on, nodes and edges can only be selected programmatically, using the selectedElementId property. Default: turned off \(false\)

</td></tr><tr><td>

Fit to screen \[fitToScreen\]

</td><td>

Resizes the map to fit into the view port.Default: false

</td></tr><tr><td>

Selected Element Id \[selectedElementId\]

</td><td>

ID of selected node or edge. This feature is only activated when the `manageElementSelection` property is turned on.\(Deprecated: Use `selectedElements` instead\)

</td></tr><tr><td>

Selected Elements\[selectedElements\]

</td><td>

JSON array that contains the elements IDs to be auto selected. This feature is only activated when the `manageElementSelection` property is turned on.

</td></tr></tbody>
</table><table id="table_lsx_qgn_fsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable nodes context menu\[disableNodesContextMenu\]

</td><td>

Disables the **More actions** context menu on the action bar for nodes.Default: **false**

</td></tr><tr><td>

Selection mode\[selectionMode\]

</td><td>

Sets the map selection mode. Only available when `manageElementSelection` is set to **false**.Choices:

-   Single
-   Multiple
-   \{\["single","multiple"\]\}

Default: **single**

</td></tr><tr><td>

Suspend re-layout\[suspendReLayout\]

</td><td>

Prevent map elements from repositioning while new data is being added.Default: **false**

</td></tr><tr><td>

Disable edges context menu\[disableEdgesContextMenu\]

</td><td>

Disables the **More actions** context menu on the action bar for edges.Default: **false**

</td></tr><tr><td>

Contextual menu items\[contextualActions\]

</td><td>

Array of DropdownItems in the **More actions** contextual menu in the action bar. The array follows anyOf logic and can contain any number of items with or without children. Items without children have the following properties:-   `id` \(string \| number\): Unique identifier for the item.
-   `label` \{string\}: Text that describes the item.
-   `count` \{number\}: Numeric indicator displayed next to the item.
-   `icon` \{string\}: Name of the icon to display next to the item. See the `now-icon` API and icon gallery for the list of valid names. Cannot be used with `presence`.
-   `presence` enum: \["available" \| "away" \| "busy" \| "offline"\]: Online status of a user to display in a list of users or statuses. Cannot be used with `icon`.
-   `disabled` \{Boolean\}: When true, the item is visible but not selectable by the user.
-   `keepMenuOpen` \{Boolean\}: Option for a menu item to stay open after selecting it to display a multi-level menu.
-   `type` \{string\} enum: \["node" \| "edge"\]: Whether the item is a node or an edge.
-   `behavior` \{string\} enum: \["default" \| "connection" \| "mousePosition"\]: A predefined behavior for the action. The default behavior is to dispatch an event when an item is clicked. The connection behavior is specific to type="node" and starts the process of adding connections between nodes. The mousePosition behavior is to use the last known open map menu position for adding new nodes.

Items with children have only the `id` and `label`properties from this list directly in their subschema. They also contain a `children` array of items with the following properties:

-   `id`
-   `label`
-   `count`
-   `icon`
-   `presence`
-   `disabled`

The `required` keys for each array identify the id and label pairs of required items and child items or entire `children` arrays that are required.

</td></tr><tr><td>

Map contextual menu items\[mapContextualActions\]

</td><td>

Array of contextual menu items to present in the map contextual menu. The contents are identical to the `contextualActions` property.

</td></tr><tr><td>

Disable expand\[disableExpand\]

</td><td>

When true, disables the "Expand/Collapse this group" action on all group nodes.Default: **false**

</td></tr><tr><td>

Disable 'home'\[disableHome\]

</td><td>

When true, disables the Home action on all nodes. Users are then unable to select a node as 'home.'Default: **false**

</td></tr><tr><td>

Disable 'show hidden connections'\[disableHiddenConnections\]

</td><td>

When true, turns off the hidden connections action on all nodes.Default: **false**

</td></tr><tr><td>

Disable control panel menu\[disableControlPanel\]

</td><td>

When true, turns off the control panel menu and its related events.Default: **false**

</td></tr><tr><td>

Control panel buttons \[controlPanelButtons\]

</td><td>

Array of additional buttons to present in the control panel.Array item properties:

-   `id` \{string\}: Unique identifier for the button.
-   `tooltipContent` \{string\}: Translatable tooltip text for the button.
-   `icon` \{string\}: Icon to use for the button. See the `now-icon` API and icon gallery for the list of valid names.
-   `order` \{integer\}: Relative position of the button on the control panel.
-   `disabled` \{boolean\}: When true, the button is visible but not selectable by the user.
-   `separator` \{boolean\}: When true, the button is separated by lines.

</td></tr><tr><td>

Disable align home node \[disableAlignHomeNode\]

</td><td>

Disable the 'Align to home node' feature and remove its button from control panel.Default: **false**

</td></tr><tr><td>

Disable Collapse All\[disableCollapseAll\]

</td><td>

Disable collapse all, remove its button from control panel. Can be bound to data, such as `@data.unified_map_1.disableControlPanelCollapseAll`.Default: **true**

</td></tr><tr><td>

Disable find on map \[disableFind\]

</td><td>

When turned on, hides the find on map input control.Default: **false**

</td></tr><tr><td>

Disable minimap \[disableMinimap\]

</td><td>

Removes the minimap view and functionality.Default: **false**

</td></tr><tr><td>

Manage auto group edges\[manageAutoGroupEdges\]

</td><td>

Overrides the automatic creation of edges between group and its direct children. An edges array must be supplied when enabling this property.Default: **false**

</td></tr><tr><td>

Enable magnification effect\[enableMagnificationEffect\]

</td><td>

When turned on, the user sees a magnification effect when they hover over a node.Default: **false**

</td></tr></tbody>
</table>**Note:** Many of these properties hide buttons in the action bars. If all buttons in an action bar are hidden, the action bar itself is hidden.

<table id="table_vfj_yjn_fsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show loading state\[isLoading\]

</td><td>

When true, enables loading spinner.Default: **false**

</td></tr><tr><td>

Override loading state message\[loadingMessage\]

</td><td>

\(Optional\) A message to show with the loading spinner in place of the default message, when `isLoading=true`.

</td></tr><tr><td>

Show empty state\[isEmpty\]

</td><td>

When true, shows the empty state placeholder message.Default: **false**

</td></tr><tr><td>

Override empty state message\[emptyMessage\]

</td><td>

\(Optional\) A message to show with the empty state banner instead of the default message, when `isEmpty=true`.

</td></tr><tr><td>

Show error state\[isError\]

</td><td>

When true, shows error state banner.Default: **false**

</td></tr><tr><td>

Override error state message\[errorMessage\]

</td><td>

\(Optional\) A message to show with the error state banner in place of the default message, when `isEmpty=true`.

</td></tr><tr><td>

Controls position\[controlsPosition\]

</td><td>

An object containing a positioning of minimap, control panel, and finder controls.Default: `{\"minimap\": \"bottom-end\", \"controlPanel\": \"end\", \"find\": \"top-start\"}`

</td></tr></tbody>
</table><table id="table_ijj_2zk_qwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reduce Motion \[reduceMotion\]

</td><td>

Enables accessibility mode where animations are not allowed. This property is sent to the component by sn-node-map.Default: **false**

</td></tr><tr><td>

Always show invisible controls \[showHiddenControls\]

</td><td>

When turned on, reveals all invisible controls inside the component. When off, some controls may be hidden until the relevant element is hovered over or focused.Default: **false**

</td></tr></tbody>
</table>### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Node items and edge items

The following JSON data defines five nodes.

```
[
   {
      "id":"n1",
      "viewData":{
         "primaryLabel":"Node 1",
         "secondaryLabel":"Node 1",
         "image":"https://picsum.photos/50"
      }
   },
   {
      "id":"n2",
      "viewData":{
         "primaryLabel":"Node 2",
         "secondaryLabel":"Node 2",
         "icon":"configuration-item-outline",
         "status":"warning"
      }
   },
   {
      "id":"n3",
      "isGroup":true,
      "viewData":{
         "primaryLabel":"Node 3",
         "secondaryLabel":"Node 3",
         "userName":"Abel Tuter",
         "groupCount":3
      }
   },
   {
      "id":"n4",
      "viewData":{
         "primaryLabel":"Node 4",
         "secondaryLabel":"Node 4"
      }
   },
   {
      "id":"n5",
      "viewData":{
         "primaryLabel":"Node 5",
         "secondaryLabel":"Node 5"
      }
   }
]
```

The following JSON data defines a set of edges that connect these nodes.

```
[
   {
      "id":"e1",
      "sourceId":"n1",
      "targetId":"n2"
   },
   {
      "id":"e2",
      "sourceId":"n1",
      "targetId":"n3"
   },
   {
      "id":"e3",
      "sourceId":"n3",
      "targetId":"n4"
   },
   {
      "id":"e4",
      "sourceId":"n3",
      "targetId":"n5"
   }
]
```

When these node and edge items use the **Node map default node** macro component, the Node map resolves in runtime as shown in the following image.

\[Omitted image "node-map-runtime1.png"\] Alt text: Simple five-node map in runtime

## Node Map component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Node Map component.

To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

\[Omitted image "node-map-events.png"\] Alt text: Shows some of the events available with node map

### Preset events

-   **__Unified map__**

    This preset provides data handlers for the following events:

    -   Map element selected
    -   Map element selection requested
    -   Home node requested
    -   Node expand requested
    -   Node collapse requested
    -   Collapse all
    -   Contextual menu opened
    -   Contextual menu item clicked
    -   Fit to screen
    -   Control panel custom action clicked
    -   Find on map requested

\[Omitted image "node-map-preset-events.png"\] Alt text: Events with event handlers from the Unified Map preset

### Event handlers

Event handlers work with data resources to link the Node Map actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

**Important:** The action bar buttons each throw an event. To implement functionality for a button, you must configure a handler to catch its event.

### Events

<table id="table_k1d_mln_fsb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map view readySN\_NODE\_MAP\#MAP\_VIEW\_READY

</td><td>

The map view has finished rendering. No set payload.

</td></tr><tr><td>

Wrapped node eventSN\_NODE\_MAP\#WRAPPED\_NODE\_EVENT

</td><td>

Wrapping event for any custom COMPONENT\_NODE\_EVENT action inside the node.Payload:

-   Source node `node`: Data object of the node that triggered this action.
-   Wrapped action `wrappedAction`: Original COMPONENT\_NODE\_EVENT dispatched from the node component.

</td></tr><tr><td>

Map elements selectedSN\_NODE\_MAP\#ELEMENTS\_SELECTED

</td><td>

Contains current nodes and edges that are selected.Payload:

-   Selected nodes `nodes`: Array of the selected nodes, if any exist.
-   Selected edge `edge`: Array of the selected edges, if any.

</td></tr><tr><td>

Map element selectedSN\_NODE\_MAP\#ELEMENT\_SELECTED

</td><td>

A specific node or edge is selected. If the selection is reset, so that nothing is selected, the event dispatches with an empty payload.Payload:

-   Selected node `node`: Data object of the selected node \(if a node was selected\).
-   Selected edge `edge`: Data object of the selected edge \(if an edge was selected\).

</td></tr><tr><td>

Map element selection requestedSN\_NODE\_MAP\#ELEMENT\_SELECTION\_REQUESTED

</td><td>

A node or edge was requested to be selected or deselected.Payload:

-   Requested node `node`: Data object of the requested node to select \(if a node was requested\).
-   Requested edge `edge`: Data object of the requested edge \(if an edge was requested\).

</td></tr><tr><td>

Home node requestedSN\_NODE\_MAP\#HOME\_NODE\_REQUESTED

</td><td>

Dispatched when the Home button on the action bar for a node is clicked. Configure a handler to set that node as Home.Payload: Source node `node`: Data object of the node that triggered this action.

</td></tr><tr><td>

Show hidden connections requestedSN\_NODE\_MAP\#SHOW\_HIDDEN\_CONNECTIONS\_REQUESTED

</td><td>

Dispatched when the Hidden connection button on the action bar is clicked. Configure a handler to show hidden connections or hide them if they currently are shown.Payload: Source node `node`: Data object of the node that triggered this action.

</td></tr><tr><td>

Node expand requestedSN\_NODE\_MAP\#EXPAND\_REQUESTED

</td><td>

On a collapsed group node, dispatched when the Expand button on the action bar is clicked. Configure a handler to show the child nodes.Payload: Source node `node`: Data object of the node that triggered this action.

</td></tr><tr><td>

Node collapse requestedSN\_NODE\_MAP\#COLLAPSE\_REQUESTED

</td><td>

On an expanded group node, dispatched when the Collapse button on the action bar is clicked. Configure a handler to hide the child nodes.Payload: Source node `node`: Data object of the node that triggered this action.

</td></tr><tr><td>

Collapse allSN\_NODE\_MAP\#COLLAPSE\_ALL\_REQUESTED

</td><td>

The **Collapse all** button was clicked in the control panel. No payload.

</td></tr><tr><td>

Contextual menu openedSN\_NODE\_MAP\#CONTEXT\_MENU\_OPENED

</td><td>

The "More actions" menu is opened in the action bar on a node or an edge.Payload:

-   Selected node `node`: Data object of the selected node \(if a node was selected\).
-   Selected edge `edge`: Data object of the selected edge \(if an edge was selected\).
-   Item type `type`: The item type: node or edge.
-   Is selected `isSelected`: A flag to indicate whether the item is selected.

</td></tr><tr><td>

Contextual menu item clickedSN\_NODE\_MAP\#CONTEXT\_MENU\_ITEM\_CLICKED

</td><td>

An action item is clicked in the "More actions" contextual menu. The payload identifies the item as well as the node or edge.Payload:

-   Selected node `node`: Data object of the selected node \(if a node was selected\).
-   Selected edge `edge`: Data object of the selected edge \(if an edge was selected\).
-   Clicked menu item `item`: The DropdownItem that was clicked in the contextual menu.

</td></tr><tr><td>

Map center aligned to a nodeSN\_NODE\_MAP\#MAP\_ALIGNED\_TO\_NODE

</td><td>

The map is aligned to center around a selected node. The node is selected with the `alignToNodeId` property.Payload: Selected node `node`: Data object of the aligned node.

</td></tr><tr><td>

Export map was clickedSN\_NODE\_MAP\#EXPORT\_REQUESTED

</td><td>

Notifies when the export map button was clicked. No payload.

</td></tr><tr><td>

Export map was savedSN\_NODE\_MAP\#EXPORT\_COMPLETED

</td><td>

Notifies when the map export is completed. No payload.

</td></tr><tr><td>

Fit to screenSN\_NODE\_MAP\#FIT\_TO\_SCREEN\_COMPLETED

</td><td>

Notification that the map has finished fitting itself to the screen size. No payload.

</td></tr><tr><td>

Control panel custom action clickedSN\_NODE\_MAP\#CONTROL\_PANEL\_CUSTOM\_BUTTON\_CLICKED

</td><td>

Notification that a custom button on the control panel was clicked.Payload: Button id `buttonId`, the id of the custom action that was clicked.

</td></tr><tr><td>

Find on map requestedSN\_NODE\_MAP\#FIND\_REQUESTED

</td><td>

Notification that the user has tried to find an element.Payload:

-   Find term `term`: The find term string that the user typed
-   Element id `id`: The id of the element being sought
-   Element type `type`: The type of the element being sought, either node or edge

</td></tr><tr><td>

Connection target node selectedSN\_NODE\_MAP\#CONNECTION\_TARGET\_SELECTED

</td><td>

Notifies the user when a target node was selected for the new connection.Payload:

-   Clicked menu item `item`: The DropdownItem that was clicked in the contextual menu.
-   Source node `sourceNode`: The source node of the new connection.
-   Target node `targetNode`: The target node of the new connection.

</td></tr></tbody>
</table>### Home node requested event handler

The Home node requested event dispatches a notification when a node is selected to be Home. In this example, a client script serves as the event handler. This script sets a State parameter when the event is triggered. In turn, this State parameter populates the `homeNodeId` configuration property.

Here is the script, which is named `setHome`. It sets the value of the **State.homeNodeId** parameter.

```
/**
* @param {params} params
* @param {api} params.api
* @param {any} params.event
* @param {any} params.imports
* @param {ApiHelpers} params.helpers
*/
function handler({api, event, helpers, imports}) {
			const {payload: {node: {id}}} = event;
			api.setState('homeNodeId' , id);
}
```

The `setHome` script is selected as the event handler for the Home node requested event.

\[Omitted image "node-map-home-node-req-handler.png"\] Alt text: Home node requested event showing setHome client script as handler.

In the configuration properties, the **@state.homeNodeId** parameter is used to define the Home node.

\[Omitted image "node-map-homeNodeId.png"\] Alt text: Configuration properties showing @State.homeNodeId for the Home node property.

## Choosing the node macro component

The Node Map requires a node macro component to render the nodes view. You can use the default node macro component or select a custom macro component.

A node macro component defines the styles to apply to nodes on the Node Map for various property values. Each node on the Node Map has its own instance of the macro component, with its own property values. For example, when a user selects a node, the map sets the property `isSelected=true` for that node. The Node Map notifies the node macro component of this property change. \(The macro component must have **isSelected** as an input parameter for it to receive the notification.\) The macro component applies the style defined for `isSelected=true` to the selected node. For all the other nodes, `isSelected=false`. Because each node has its own instance of the macro component, those nodes do not have the `isSelected=true` style applied. If no style is defined for either value of **isSelected**, there is no difference in the appearance of the nodes whether they are selected or not.

### Node Map default node

If you don't select a value in the **Node view macro component** \(**nodeMacroponent**\) property, the **Node map default node** macro component is used. The sizing properties are set to a predetermined, optimal fixed width and height for this macro component.

You can define the following properties on the Node Map `nodes[*].viewData` object for individual nodes from the default macro component:

-   **__icon__**

    Name of the icon in dash-case, including the `-fill` or `-outline` suffix to indicate whether the icon is filled or outlined. This icon is input for the now\_icon component, therefore should follow the same rules.

    Type: `string`

    Default: `"wrench-outline"`

-   **__image__**

    Path to the user image to display in the avatar

    Type: `string`

-   **__status__**

    The node's status, displayed with an indicator icon in the corner of the avatar.

    Type: `("none" | "positive" | "error" | "warning")`

    Default: `"none"`

-   **__groupCount__**

    Represents the number of nodes in the node's group. If a value is not supplied or equals zero, the number badge for group elements is not displayed.

    Type: `number`

    Default: `0`

-   **__userName__**

    Name of the user that the avatar represents. If no `image` is provided, then the initials of the first two names that are provided in the string appear in the avatar. If no name and no image are provided, an icon is displayed.

    Type: `string`

-   **__primaryLabel__**

    A string that represents the node primary label \(title\). This property name is reserved for this purpose regardless of node macro component.

    Type: `string`

-   **__secondaryLabel__**

    A string that represents the node secondary label \(subtitle\). This property name is reserved for this purpose regardless of node macro component.

    Type: `string`


None of the `viewData` properties are required for **Node map default node**. Therefore, regardless of whether or how you have configured the `viewData` objects, the nodes from the default macro component always render.

### Available custom node macro components

In the **Node view macrocomponent** \(**nodeMacroponent**\) field, you can choose any UI Builder component or page. The list is populated from the UX Macroponents Definitions \[sys\_ux\_macroponent\] table. The choice should be consistent with the expected node component API and functionality. The node must also fulfill these minimal requirements:

-   All the necessary component functionality has to be supported with the component properties. Slots inside the node macro component are not currently supported.
-   A node macro component cannot use internally any kind of floating popover component, such as dropdown, tooltip, popover, modal, or similar. This restriction exists because each node appearance on Node Map is strictly limited inside a container of an optimal size.
-   The node macro component's internal logic must not depend on any of the following reserved properties. The internal logic of Node Map overrides these properties. Adding any of these properties to `nodes[*].viewData` has no effect:
    -   **isFocused**
    -   **isGroup**
    -   **isSelected**
    -   **isInactive**
    -   **isHome**

### Requirements for the full support of a node macro component

Beyond the minimal requirements for a macro component to serve as a node macro component, these requirements enable full Node Map functionality:

-   Because a Node Map notifies each node macro component on visual state changes, a node macro component should implement visualizations for each of these states:
    -   **__isFocused__**

        When `true`, the node should apply a CSS style for the 'focused' state. This focused state doesn't cover the mouse ':hover' event. It's triggered during keyboard navigation over the map elements.

    -   **__isSelected__**

        When `true`, the node should apply a CSS style for the 'selected' state.

    -   **__isGroup__**

        When `true`, the node should apply a distinctive visualization for a group node. This state is a pass-thru property from `nodes[*].isGroup`.

    -   **__isInactive__**

        When `true`, the node should apply a CSS style for the 'inactive/disabled' state. This state is a pass-thru property from `nodes[*].isInactive`.

    -   **__isHome__**

        When `true`, the node should apply a distinctive visualization for the Home node.

-   The node macro component should use the CSS pseudo-selector ':hover' to implement mouse-over style.

### Tips for working with a custom node macro component

-   Consider reducing any internal interactions of the node macro component with the server side. Move data fetching/updates to the level of the page that contains the Node Map. Consider using only visual non-connected components for the node macro component.
-   To notify the parent page about an update on any of the nodes, use the `SN_NODE_MAP#COMPONENT_NODE_EVENT` action. On the Node Map, configure a handler for the **Wrapped node event** \(SN\_NODE\_MAP\#WRAPPED\_NODE\_EVENT\) action to encapsulate the original COMPONENT\_NODE\_EVENT and the data object for the node that triggered the action.
-   For compliance with WCAG accessibility standards, to allow screen readers to read out all the relevant internal states and labels inside the custom node macro component, add the attribute **aria-label** or **aria-labelledby** on the first element inside the **shadowRoot** of the custom node component.
-   Be certain to select appropriate **Width** \(**nodeWidthMode**\) and **Height** \(**nodeHeightMode**\) properties and any associated value properties.

