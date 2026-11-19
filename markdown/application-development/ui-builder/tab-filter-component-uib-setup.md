---
title: Tab filter component setup
description: The Tab filter component enables users to filter search results based on defined sources and sort the results based on configured fields.Define the search and sort filters for the Tab filter component.Select event handlers to configure the events provided with the Tab filter component. Event handlers work with data resources to link the Tab filter actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/tab-filter-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Tab filter component setup

The Tab filter component enables users to filter search results based on defined sources and sort the results based on configured fields.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Tab filter that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "tab-filter-content-tree.png"\] Alt text: Shows the tab filter component in the UIB content tree

2.  Select the Tab filter component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "tab-filter-properties.png"\] Alt text: Shows the Config panel with the tab filter component properties


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Tab filter component properties

Define the search and sort filters for the Tab filter component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_p2l_qdp_45b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search filters\[searchFilters\]

</td><td>

The searchFilters response from the Search Filter GraphQL API; it contains the data for tab items with a sysId and a label.

</td></tr><tr><td>

Selected filter tab\[selectedFilters\]

</td><td>

Specifies the ID of the selected filter tab. If this property is not passed in, the **All** filter tab is selected by default.

</td></tr><tr><td>

Sort filters\[sortFilters\]

</td><td>

Response from the Search Filter GraphQL API; it contains the data for sort by filter items with sysId and label.

</td></tr><tr><td>

Selected sort filter\[selectedSortFilters\]

</td><td>

Specifies the ID of the selected sort filter. If this property is not passed in, the Relevancy filter is selected in the sort by filter dropdown by default.

</td></tr></tbody>
</table>## Tab filter component events

Select event handlers to configure the events provided with the Tab filter component. Event handlers work with data resources to link the Tab filter actions to the data you want to display to your users.

The Events tab shows the events used by the Tab filter component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Tab filter actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "tab-filter-events.png"\] Alt text: Shows tab filter events with event handlers defined

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tab filter selected

</td><td>

Dispatched when the user selects a tab filter.The payload includes `selectedFilter`, which contains the JSON stringified array containing the sys\_id of the tab filter selected by the user.

</td></tr><tr><td>

Sort filter selected

</td><td>

Dispatched when the user selects a sort filter.The payload includes the `selectedFilter`, which contains the JSON stringified array containing the sys\_id of the sort filter selected by the user.

</td></tr></tbody>
</table>