---
title: Dashboard Overview component setup
description: Dashboard Overview enables users to navigate between Next Experience dashboards they own or that are shared with them. Users can see all these dashboards or only those that are bookmarked or certified, or that they created.Configure what information to show on the Dashboard Overview with these properties.Select event handlers to configure the actions \(events\) provided with the Dashboard Overview component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/dashboards-overview-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Dashboard Overview component setup

Dashboard Overview enables users to navigate between Next Experience dashboards they own or that are shared with them. Users can see all these dashboards or only those that are bookmarked or certified, or that they created.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Dashboard Overview that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "dashboards-overview-content-tree.png"\] Alt text: Content tree showing one Dashboards Overview component

2.  Select the Dashboard Overview component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Dashboard Overview label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Dashboard Overview component properties

Configure what information to show on the Dashboard Overview with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_vz4_m3m_mnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

heading

</td><td>

Sets the name that is shown at the top of the component, above the dashboard cards.Default: Dashboards

</td></tr><tr><td>

Number of dashboard cards

</td><td>

limit

</td><td>

Sets the number of dashboard cards that the dashboard overview displays.Default: 6

</td></tr><tr><td>

Display all dashboards

</td><td>

displayAllDashboards

</td><td>

Replaces the limited number of large dashboard cards with dashboard previews. When true, displays simple cards listing all the available dashboards, along with a filter and a button to create a new dashboard.Default: False

</td></tr><tr><td>

User Info

</td><td>

userInfo

</td><td>

\(Hidden, read-only\) Stores information about which user is logged in. This information determines which dashboards are displayed.Default: @context.session.user

</td></tr></tbody>
</table>## Dashboards Overview component events

Select event handlers to configure the actions \(events\) provided with the Dashboard Overview component.

The Events tab shows the events used by the Dashboard Overview component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Dashboard Overview actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_wjz_msm_mnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

'See all' Clicked

</td><td>

Dispatched when you click on See all and replaces the card view with a list of all available dashboards.Event handler: Link to Destination

 Suggested app route: All dashboards

 Sub-navigation route: `current`

</td></tr><tr><td>

Dashboard card clicked

</td><td>

Dispatched when you click on a dashboard card and opens the corresponding dashboard.Event handler: Link to Destination

 Suggested app route: Dashboard

 Destination **sysid**: `@payload.routeSysid`

</td></tr></tbody>
</table>\[Omitted image "dashboard-overview-card-event-config.png"\] Alt text: Link Destination event handler with /dashboard app route and destination Sysid field value @payload.routeSysid

