---
title: Flyout menu component setup
description: The Flyout menu component enables users to configure nested submenus, providing multiple levels of options or actions without leaving the current context.Configure the items and actions of Flyout menu and its nested submenus by setting these properties.Select event handlers to configure the events provided with the Flyout menu component. Event handlers work with data resources to link the Flyout menu actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/flyout-menu-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Flyout menu component setup

The Flyout menu component enables users to configure nested submenus, providing multiple levels of options or actions without leaving the current context.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Flyout menu that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "flyout-menu-content-tree.png"\] Alt text: Flyout menu component in the UI Builder content tree.

2.  Select the Flyout menu component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "flyout-menu-config.png"\] Alt text: Flyout menu component in the UI Builder configuration panel.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Flyout menu component properties

Configure the items and actions of Flyout menu and its nested submenus by setting these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Sets the size of the menu list in either small or medium.Default: **Medium**

</td></tr><tr><td>

List header\[listHeader\]

</td><td>

A header for the overall menu list with an optional icon.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables user interactions with the menu.Default: **False**

</td></tr></tbody>
</table><table id="table_ql2_d21_x2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List items\[items\]

</td><td>

An array of items or sections to include in the menu list.

</td></tr></tbody>
</table><table id="table_k3x_g21_x2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected items\[selectedItems\]

</td><td>

An array of IDs representing selected menu list items.

</td></tr><tr><td>

Manage selected items\[manageSelectedItems\]

</td><td>

If set to **True**, overrides automatic updates to the **Selected items** property. Use the **Flyout menu selected items set** event to intercept the requested change and handle it manually.Default: **False**.

</td></tr></tbody>
</table><table id="table_vqb_t21_x2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Constrain\[constrain\]

</td><td>

Optional sizing constraints to enforce on the flyout menu content. See API for details.

</td></tr><tr><td>

Opened\[opened\]

</td><td>

Updates when a user opens or closes the menu.Default: **False**

</td></tr><tr><td>

Manage opened\[manageOpened\]

</td><td>

If set to **True**, overrides automatic updates to the **Opened** property. Use the **Flyout menu opened set** event to intercept the requested change and handle it manually.Default: **False**.

</td></tr></tbody>
</table>## Flyout menu component events

Select event handlers to configure the events provided with the Flyout menu component. Event handlers work with data resources to link the Flyout menu actions to the data you want to display to your users.

The Events tab shows the events used by the Flyout menu component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Flyout menu actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flyout menu opened set\[NOW\_FLYOUT\_MENU\#OPENED\_SET\]

</td><td>

The user opens or closes the flyout menu.Payload contains:

`Value`

-   `true`: Flyout menu opens
-   `false`: Flyout menu closes

</td></tr><tr><td>

Flyout menu selected items set\[NOW\_FLYOUT\_MENU\#SELECTED\_ITEMS\_SET\]

</td><td>

The user changes the selected items.Payload contains:

`Value`: An array containing either a single ID or multiple IDs of the selected items.

</td></tr></tbody>
</table>