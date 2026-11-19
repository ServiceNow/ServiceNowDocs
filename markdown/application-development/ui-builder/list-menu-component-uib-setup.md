---
title: List menu component setup
description: The List menu component enables you to navigate between lists and save and access personalized lists.Configure the List menu properties to navigate between lists and save and access personalized lists.Select event handlers to configure the actions \(events\) provided with the List menu component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/list-menu-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# List menu component setup

The List menu component enables you to navigate between lists and save and access personalized lists.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your List menu that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "list-menu-content-tree.png"\] Alt text: List Menu content tree.

2.  Select the List menu component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the List menu label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## List Menu component properties

Configure the List menu properties to navigate between lists and save and access personalized lists.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_cjl_3ln_4nb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show list menu\[listMenuOpen\]

</td><td>

Option to display the List Menu.Default: **true**

</td></tr><tr><td>

Hide tabs\[hideTabs\]

</td><td>

Show or hide the List and My List tabs. If hidden, users can't save lists to **My Lists**.**Note:** To prevent users from creating their own custom lists, this property and the **Hide option to save as** property in the list component must both be set to **true**. Hiding the tabs in List Menu alone doesn't restrict the user from saving their own lists from the options menu in the List component.

 Default: **false**

</td></tr><tr><td>

Hide 'My list' creation\[hideListCreation\]

</td><td>

Option to disable the ability to create lists under the My Lists tab.Default: **false**

</td></tr><tr><td>

Configuration\[configurationId\]

</td><td>

Configuration to use for your List Menu. This is a reference field to list categories configured in the **sys\_ux\_list\_menu\_config** table.Default:

-   Tasks
-   Incidents
-   Problems
-   Requests
-   Catalog Tasks

</td></tr><tr><td>

Selected list ID\[listId\]

</td><td>

ID of the list to be auto-selected from the menu.

</td></tr><tr><td>

List menu user access\[listMenuCrud\]

</td><td>

Object that defines the CRUD actions that users can perform in the **My Lists** tab.

</td></tr><tr><td>

Tiny ID\[tiny\]

</td><td>

A generated sys\_ID that represents a shared list and its applied conditions. Tiny IDs are used to hold URL parameters that are too long for a browser.

</td></tr></tbody>
</table>## List Menu component events

Select event handlers to configure the actions \(events\) provided with the List menu component.

The Events tab shows the events used by the List menu component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the List menu actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_lwb_vsw_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Menu item clicked

</td><td>

A user selects an item from the cell context menu. Payload:

-   **selectedListId**: ID of the list that was selected from the navigation menu
-   **targetTable**: Table name that the list record came from, such as `sys_ux_list` or `sys_ux_my_list`
-   **table**: Name of the table selected
-   **title**: Display value of the table selected
-   **conditions**: Encoded query string that filters results of the current table
-   **columns**: Columns that should be displayed for the table selected

</td></tr><tr><td>

Selected item updated

</td><td>

An item from the list menu is auto selected.Payload:

-   **selectedListId**: ID of the list that was selected from the nav menu
-   **targetTable**: Table name that the list record came from, such as sys\_ux\_list or sys\_ux\_my\_list
-   **table**: Name of the table selected
-   **title**: Display value of the table selected
-   **conditions**: Encoded query string that filters results of the current table
-   **columns**: Columns that should be displayed for the table selected

</td></tr><tr><td>

Content items selected

</td><td>

A user selects a menu item to dispatch admin configuration links. The array contains the labels, order, and links from the admin configuration menu.Payload:

-   **order**
-   **label**
-   **url**

</td></tr><tr><td>

Error

</td><td>

An error has occurred in the list menu.Payload contains **error**: Information to display when an error has occurred

</td></tr></tbody>
</table>