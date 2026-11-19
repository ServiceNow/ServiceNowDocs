---
title: Resizable Panes component setup
description: The Resizable Panes component enables users to expand and reduce the size of panes in Workspace, both horizontally and vertically.Properties in the Resizable Panes component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/resizable-panes-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 13
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Resizable Panes component setup

The Resizable Panes component enables users to expand and reduce the size of panes in Workspace, both horizontally and vertically.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Resizable Panes that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Work with pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "resizable-panes-content-tree.png"\] Alt text: Shows the Resizable Panes component and its panes listed in the content tree.

2.  Select the Resizable Panes component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Resizable Panes label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "resizable-panes-presets.png"\] Alt text: Shows the list of presets in UI Builder for the Resizable Panes component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "resizable-panes-preset-config.png"\] Alt text: Shows the configuration panel for connecting the preset to it required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Resizable Panes component properties

Properties in the Resizable Panes component have preset configuration values. You can accept these values or override them manually.

Presets are designed to suit a specific use case. However, you can override a property that has a preset value with a custom configuration, if you find it necessary for your design. For details on overriding and resetting presets, see [Override a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record resizable panes__**

    Provides adjustable content slots for other components that can be adjusted vertically and horizontally. This preset requires the **Form** controller.

    Properties included in this preset are:

    -   Panes position
    -   Default displayed pane
    -   Display action bar
    -   Action bar configuration
    -   Minimum width of left pane
    -   Minimum height of top pane
    -   Minimum height of bottom pane
    -   Divider styles
    -   Bare
-   **__Playbook Resizable Panes Left/Right__**

    Provides a left and right resizable panes layout for Playbook. This preset requires the **Playbook Custom Layout** controller. Provide the following values for the **Playbook Custom Layout** controller:

    -   **Parent SysID**
    -   **Parent Table**
    -   **Playbook Experience**
    Properties included in this preset are:

    -   Panes position
    -   Default displayed pane
    -   Bare
    -   Default divider position
    -   Divider styles
    -   Minimum height of bottom pane
    -   Minimum height of top pane
    -   Minimum width of left pane
    -   Minimum width of right pane
-   **__Horizontal list pane__**

    Displays list panes in a side-by-side format. This preset requires the **List Controller** controller.

    Properties included in this preset are:

    -   Default displayed pane
    -   Panes position
    -   Fixed
    -   Display action bar
    -   Action bar configuration
    -   Display divider button
    -   Divider button configuration
    -   Default divider position
    -   Minimum width of left pane
    -   Minimum width of right pane
    -   Minimum height of top pane
    -   Minimum height of bottom pane
    -   Divider styles
    -   Bare
    -   Left pane aria label
    -   Right pane aria label
    -   Top pane aria label
    -   Bottom pane aria label
    -   Divider aria label
    -   Divider handle tooltip
-   **__List menu resizable pane__**

    Displays the list menu side by side with the list. This preset requires the **List Controller** controller. Requires additional information about the table data to display in the list to set up the controller data. Default table is **Task**.

    Properties included in this preset are:

    -   Default displayed pane
    -   Panes position
    -   Display divider button
    -   Fixed
    -   Display action bar
    -   Default divider position
    -   Divider button configuration
    -   Minimum width of left pane
    -   Bare
    -   Divider aria label
    -   Divider handle tooltip
    -   Right pane aria label
    -   Left pane aria label
    -   Action bar configuration
    -   Minimum width of right pane
    -   Minimum height of top pane
    -   Minimum height of bottom pane
    -   Divider styles
    -   Top pane aria label
    -   Bottom pane aria label
-   **__Standard record page resizable panes__**

    Provides a resizable pane for use in a standard record page. This preset requires the **Form** controller.

    Properties included in this preset are:

    -   Panes position
    -   Default displayed pane
    -   Display action bar
    -   Action bar configuration
    -   Minimum width of left pane
    -   Minimum height of top pane
    -   Minimum height of bottom pane
    -   Divider styles
    -   Bare
-   **__Vertical List Pane__**

    Displays the list panes in a vertical orientation. This preset requires the **List Controller** controller. Requires additional information about the table data to display in the list to set up the controller data. Default table is **Task**.

    Properties included in this preset are:

    -   Default displayed pane
    -   Panes position
    -   Fixed
    -   Display action bar
    -   Action bar configuration
    -   Display divider button
    -   Divider button configuration
    -   Default divider position
    -   Minimum width of left pane
    -   Minimum width of right pane
    -   Minimum height of top pane
    -   Minimum height of bottom pane
    -   Divider styles
    -   Bare
    -   Left pane aria label
    -   Right pane aria label
    -   Top pane aria label
    -   Bottom pane aria label
    -   Divider aria label
    -   Divider handle tooltip

### Properties

<table id="table_qx5_txv_j3c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Panes position\[panesPosition\]

</td><td>

Layout of the resizable panes to use. Available options are:-   **Left and right**: Arranges the panes side-by-side horizontally.
-   **Top and bottom**: Arranges the panes top and bottom, stacked vertically.
-   **Left &amp; right with split-stack**: Arranges the panes side-by-side horizontally with a split/stack action bar at the bottom.

Default: **Left and right**

</td></tr><tr><td>

Default displayed pane\[defaultDisplayedPane\]

</td><td>

Panes displayed when rendered on a page for the first time. Available options depend on the Panes position property's configuration.Available options when **Panes position** is **Left and right** or **Left &amp; right with split-stack**:

-   Left pane
-   Right pane
-   Both panes

Available options when **Panes position** is **Top and bottom**:

-   Top pane
-   Bottom pane
-   Both panes

Default: **Both Panes**

</td></tr><tr><td>

Stack resizable panes\[singleColumn\]

</td><td>

Available when **Panes position** is **Left and right**.To stack the panes vertically, left pane at the top and right pane at the bottom, set to **true**. This property is controlled by auto reflow rules when responsive authoring is not enabled. Ignores the configuration of the **Default displayed pane**.

Default: **false**

</td></tr><tr><td>

Fixed\[disabled\]

</td><td>

To prevent users from resizing panes using the divider, set to **true**. Hides the **Display action bar** property when enabled.Default: **false**

</td></tr><tr><td>

Default pane mode\[splitStackMode\]

</td><td>

Available when **Panes position** is set to **Left &amp; right with split-stack**.The default position mode of the panes when rendering for the first time. Post initial render, the user can switch the pane position mode using the pane mode button in the action bar. Available options are:

-   **Split position**: Arranges the panes side-by-side horizontally.
-   **Stack position**: Stacks the panes vertically, the left pane at the top and the right pane at the bottom.

Default: **Split position**

</td></tr><tr><td>

Display action bar\[actionBar\]

</td><td>

Available when **Panes position** is set to **Left and right** or **Top and bottom**. Not available when the **Fixed** property is set to **true**.To display the action bar, set to **true**. Action bar enables users to switch between view modes \(one pane, or both panes\).

Default: **false**

</td></tr><tr><td>

Action bar configuration\[actionBarConfig\]

</td><td>

Available when **Display action bar** is set to **true**.JSON object containing the icons and tooltips used by the action bar to switch between different view modes.

Schema:

-   `leftIcon`: String identifier for the icon of the button that shows left pane.
-   `middleIcon`: String identifier for the icon of the button that shows both panes.
-   `rightIcon`: String identifier for the icon of the button that shows right pane.
-   `leftTooltip`: Tooltip text for the left pane button.
-   `middleTooltip`: Tooltip text for the button that shows both panes.
-   `rightTooltip`: Tooltip text for the right pane button.

Default:

```json
{
                           "leftIcon": "record-activity-details-fill",
                           "middleIcon": "record-activity-stream-vertical-outline",
                           "rightIcon": "record-activity-outline",
                           "leftTooltip": "Show left pane",
                           "middleTooltip": "Show both panes",
                           "rightTooltip": "Show right pane"
                           }
```

</td></tr><tr><td>

Display divider button\[displayDividerButton\]

</td><td>

To show an iconic button on the divider that the user can select to drag and resize the panes, set to **true**. The appearance of the divider button can be configured using the **Divider button configuration** property.Default: **false**

</td></tr><tr><td>

Divider button configuration\[dividerButtonConfig\]

</td><td>

Available when **Display divider button** is set to **true**.JSON object containing the configuration of the divider button.

Schema:

-   `position`: Position of the button on the divider bar. Accepted values are: `top`, `bottom`, `left`, `right`, and `center`.
-   `buttonProps`: Properties of the divider button.
    -   `icon`: Icon identifier for the button.
    -   `tooltip-content`: Tooltip text to display for the button.
    -   `config-aria`: ARIA configuration of the button.

Default:

```json
{
                           "position": "left",
                           "buttonProps": {
                           "icon": "chevron-left-outline",
                           "config-aria": {}
                           }
                           }
```

</td></tr><tr><td>

Default divider position\[defaultDividerPosition\]

</td><td>

Default position for the divider separating the two panes expressed as an integer between 0 and 100. 0 places the divider at the left-most \(or top-most\) position, 100 places the divider at the right-most \(or bottom-most\) position.The position is also influenced by the `minRatio` and `minPixesls` values in the **Layout and styling**.

Default: **50**

</td></tr></tbody>
</table><table id="table_i5t_vxv_j3c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Left pane aria label\[leftPaneAriaLabel\]

</td><td>

Available when **Panes position** is set to **Left and right** or **Left &amp; right with split-stack**.ARIA label for the left pane.

Default: **Left pane**

</td></tr><tr><td>

Right pane aria label\[rightPaneAriaLabel\]

</td><td>

Available when **Panes position** is set to **Left and right** or **Left &amp; right with split-stack**.ARIA label for the right pane.

Default: **Right pane**

</td></tr><tr><td>

Top pane aria label\[topPaneAriaLabel\]

</td><td>

Available when **Panes position** is set to **Top and bottom**.ARIA label for the top pane.

Default: **Top pane**

</td></tr><tr><td>

Bottom pane aria label\[bottomPaneAriaLabel\]

</td><td>

Available when **Panes position** is set to **Top and bottom**.ARIA label for the bottom pane.

Default: **Bottom pane**

</td></tr><tr><td>

Divider aria label\[dividerAriaLabel\]

</td><td>

ARIA label for the pane divider.Default: Resizable panes divider

</td></tr><tr><td>

Divider handle tooltip\[dividerHandleTooltip\]

</td><td>

Tooltip to display on the divider handle.Default: Adjust Pane

</td></tr></tbody>
</table><table id="table_s4k_wxv_j3c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum width of left pane\[leftPaneConstraints\]

</td><td>

Available when **Panes position** is set to **Left and right** or **Left &amp; right with split-stack**.Width size constraints for the left pane with a minimum size ratio between 0 and 100, and a minimum pixel size. The ratio here is the ratio of the left and right panes' widths.

Configure this property as a JSON string with the format `{ minRatio:number, minPixels:number }`.

Default: `{minRatio: 20, minPixels: 100}`

</td></tr><tr><td>

Minimum width of right pane\[rightPaneConstraints\]

</td><td>

Available when **Panes position** is set to **Left and right** or **Left &amp; right with split-stack**.Width size constraints for the right pane with a minimum size ratio between 0 and 100, and a minimum pixel size. The ratio here is the ratio of the right and left panes' widths.

Configure this property as a JSON string with the format `{ minRatio:number, minPixels:number }`.

Default: `{minRatio: 20, minPixels: 100}`

</td></tr><tr><td>

Minimum height of top pane\[topPaneConstraints\]

</td><td>

Available when **Panes position** is set to **Top and bottom**.Height size constraints for the top pane with a minimum size ratio between 0 and 100, and a minimum pixel size. The ratio here's the ratio of the top and bottom panes' heights.

Configure this property as a JSON string with the format `{ minRatio:number, minPixels:number }`.

Default: `{minRatio: 20, minPixels: 100}`

</td></tr><tr><td>

Minimum height of bottom pane\[bottomPaneConstraints\]

</td><td>

Available when **Panes position** is set to **Top and bottom**.Height size constraints for the top pane with a minimum size ratio between 0 and 100, and a minimum pixel size. The ratio here's the ratio of the bottom and top panes' heights.

Configure this property as a JSON string with the format `{ minRatio:number, minPixels:number }`.

Default: `{minRatio: 20, minPixels: 100}`

</td></tr><tr><td>

Divider styles\[dividerStyles\]

</td><td>

Custom CSS styles for the divider expressed as JSON.For example, to add padding and set a background color, enter:

```
{
                              "padding":10px,
                              "background-color":"blue"
                              }
```

Default: `{}`

</td></tr><tr><td>

Bare\[bare\]

</td><td>

To remove borders from the pane display, set to **true**.Default: **false**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Links the property to data from another component, using data resources. For details, see [Connect data to your components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/connect-data.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Define and bind client scripts to components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/define-client-scripts.md).

## Resizable Panes component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Resizable Panes component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "resizable-panes-event-handler.png"\] Alt text: Shows the events available with Resizable Panes. No preset events are included

### Event handlers

Event handlers work with data resources to link the Resizable Panes actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

\[Omitted image "resizable-panes-mapped-events.png"\] Alt text: Shows the events for Resizable Panes that have event handlers defined

### Preset events

-   **__Record resizable panes__**

    This preset doesn't include any events.


### Event descriptions

|Event|Description|
|-----|-----------|
|Pane displayed changed|Pane displayed has changed to left, right or both. The payload contains the updated`displayedPane` value.|
|Pane sizes changed|Pane sizes have changed. The payload contains the updated `dividerPosition` value.|
|Divider button clicked|Divider button selected. This event doesn't have a payload.|

