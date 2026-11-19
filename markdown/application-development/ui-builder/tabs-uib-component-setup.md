---
title: Tabs component setup
description: The Tabs component comprises a set of tabs, each displaying different components. Tabs can be arranged horizontally or vertically. This component was named Tab Set in versions prior to Tokyo.Configure the tabs displayed in your Tabs component.Select event handlers to configure the actions \(events\) provided with the Tabs component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/tabs-uib-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Tabs component setup

The Tabs component comprises a set of tabs, each displaying different components. Tabs can be arranged horizontally or vertically. This component was named Tab Set in versions prior to Tokyo.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

For instructions on overriding styles using the Styles pane, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-styling-to-component.md)

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Tabs that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "tabs-content-tree.png"\] Alt text: Shows the Tabs component in the UI Builder content tree

2.  Select the Tabs component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "tabs-properties.png"\] Alt text: Shows the properties for the Tabs component in the Config panel


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Tabs component properties

Configure the tabs displayed in your Tabs component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_bwt_nsz_xnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tabs\[items\]

</td><td>

Area of the component that a user can configure like a page, by adding layout, components, and other elements for a specified tab. Contains the following fields \[properties\]:-   **Tab label \[label\]**

Text label to be displayed in the tab body and/or provided to assistive technologies \(required\).

-   **Icon \[icon\]**

Name of icon name to display in the tab label.

-   **Hide tab \[conditional\]**

A value of 'true' hides the tab. You can bind this property to a client state parameter or write a script that would hide the tab only in certain conditions.

Default: **false**


</td></tr><tr><td>

Default tab\[defaultRoute\]

</td><td>

Statically sets the tab that is selected when the page loads.

</td></tr><tr><td>

Selected tab index\[selectedTabIndex\]

</td><td>

Dynamically sets the tab that is open by default when bound to data by string queries or data resources. To set the default tab statically, use **defaultTabProperty**​.

</td></tr><tr><td>

Label size\[size\]

</td><td>

Sets the size of the tab labels, Small \(sm\) or Medium \(md\).

</td></tr><tr><td>

Hide tab labels\[hideLabel\]

</td><td>

When enabled, hides the tab labels. This setting doesn't affect tab icons.Default value: **false**

</td></tr><tr><td>

Tab CSS styles\[tabStyles\]

</td><td>

Field for custom CSS to apply to the tab bar or the tab container. Use `.tabset-tabs` and `.tabset-container` classes to style these regions.Default value: `.tabset-tabs{\n\n}\n.tabset-container{\n\n}`

</td></tr><tr><td>

Tab position\[position\]

</td><td>

Sets the position of the tabs and determines if they display horizontally or vertically. The choices are:-   **Top**: Displays the tabs horizontally at the top of the content
-   **Start**: Displays the tabs vertically at the beginning of the content
-   **End**: Displays the tabs vertically at the end of the content

Default value: **Top**

**Note:** Configuring vertical tabs displays additional properties.

</td></tr><tr><td>

Maximum width\[maxWidth\]

</td><td>

Maximum width \(in pixels\) of each tab. Text is truncated if it's longer than the tab width.Default value: **240**

</td></tr><tr><td>

Span tabs\[fixedWidth\]

</td><td>

When enabled, horizontal tabs are spaced evenly \(justified\) in the available space. When disabled, the tabs adjust dynamically, based on the amount of available space. This property is available when the tab position is set to **Top**.Default value: **false**

</td></tr><tr><td>

Space between items\[spaceBetweenItems\]

</td><td>

Sets the space between the tabs: None, xxs, xs, sm, md, lg, xl, xxl, 3xl. This property is available when the tab position is set to **Start** or **End**\).Default value: **None**

</td></tr><tr><td>

Allow user to collapse tabs\[enableCollapsing\]

</td><td>

When enabled, allows users to collapse the content in a selected tab by clicking the tab icon. This property is available when the tab position is set to **Start** or **End**\).Default value: **false**

</td></tr><tr><td>

Collapse tabs by default\[initiallyCollapsed\]

</td><td>

When enabled, collapses all tab content when the page first loads. This property is available when the tab position is set to **Start** or **End**\).Default value: **false**

</td></tr><tr><td>

Show inline padding\[showInlinePadding\]

</td><td>

When enabled, adds additional inline padding to vertical tab buttons. This property is available when the tab position is set to **Start** or **End**\).Default value: **false**

</td></tr></tbody>
</table>## Tabs component events

Select event handlers to configure the actions \(events\) provided with the Tabs component.

The Events tab shows the events used by the Tabs component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Tabs actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "tabs-events.png"\] Alt text: Shows the available events for Tabs

### Event descriptions

<table id="table_dmb_h5z_xnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tab item selected

</td><td>

Action that is fired when a tab is selected.Payload includes `selectedTabIndex`: Tab index identifying the route of the tab that was selected.

</td></tr><tr><td>

Tab collapsed

</td><td>

Action that is fired when a tab is collapsed.Payload includes `collapsed`: Flag indicating the collapsed state of the selected tab.

</td></tr></tbody>
</table>