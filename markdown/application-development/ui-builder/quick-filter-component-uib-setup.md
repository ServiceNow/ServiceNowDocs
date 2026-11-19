---
title: Quick Filter component setup
description: The Quick Filter component is a light condition builder that enables you to create multiple filters quickly from a data source in your page and select the best subset of those filters for your users.Configure the visibility of the Quick Filter component and the filters to show your users.Select event handlers to configure the events provided with the Quick Filter component. Event handlers work with data resources to link the Quick Filter actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/quick-filter-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Quick Filter component setup

The Quick Filter component is a light condition builder that enables you to create multiple filters quickly from a data source in your page and select the best subset of those filters for your users.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Quick Filter that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).\[Omitted image "quick-filter-conent-tree.png"\] Alt text: Shows the quick filter component in the UI Builder content tree

2.  Select the Quick Filter component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "quick-filter-config.png"\] Alt text: Shows the configurable properties for the quick filter component in UI Builder


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Quick Filter component properties

Configure the visibility of the Quick Filter component and the filters to show your users.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Links the property to data from another component by using data resources. For details, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_b5l_2zl_wxb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filters\[filters\]

</td><td>

Object containing all filters and values for a configured data source.

</td></tr><tr><td>

Selected filters\[selectedFilters\]

</td><td>

An array of filters and values that you preselect for the user. Preselected filters can help your users search records more efficiently but don't prevent the user from selecting other filters.

</td></tr><tr><td>

Default filters to display\[defaultFilters\]

</td><td>

An array of default filters that enables users to reset their filter conditions. This list should match the list in the **Selected filters** property if you have configured preselected filters.

</td></tr><tr><td>

Open filter dropdown\[autoOpenDropdown\]

</td><td>

Opens the filter dropdown automatically when the user clicks **Add Filter**.Default: **false**

</td></tr><tr><td>

Footer action \[footerActions\]

</td><td>

Allows a configurable footer action button. Currently only one button is expected \(Apply/Submit button\). If more than one button config is passed to this array, it will be ignored. Render position is bottom left.

</td></tr></tbody>
</table>## Quick Filter component events

Select event handlers to configure the events provided with the Quick Filter component. Event handlers work with data resources to link the Quick Filter actions to the data you want to display to your users.

The Events tab shows the events used by the Quick Filter component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Quick Filter actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "quick-filter-events.png"\] Alt text: Shows the configurable events available for the quick filter component

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected filters set

</td><td>

The user makes a change to **selectedFilters**, and the results on the page are updated with the new selection.Payload:

-   name: **value**
-   label: **Value**
-   fieldType: **json**
-   typeMetadata: **array**

</td></tr></tbody>
</table>