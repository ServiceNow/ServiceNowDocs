---
title: Process Optimization - Map component setup
description: Map the different states that are part of your process and the transitions between those states. See which states the objects of the process are in and the speed with which they change state.Select the Process Mining project to map and the map details.\\The Process Optimization - Map component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/process-optimization-map-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Process Optimization - Map component setup

Map the different states that are part of your process and the transitions between those states. See which states the objects of the process are in and the speed with which they change state.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for the Process Mining Map that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Process Mining Map component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Process Optimization - Map component properties

Select the Process Mining project to map and the map details.\\

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Links the property to data from another component by using data resources. For details, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_icl_ym1_fxb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Show Header \[showHeader\]

</td><td>

When enabled, displays the visualization header, including title and icons.Default: true/on

</td></tr><tr><td>

Show header separator \[showHeaderSeparator\]

</td><td>

When enabled, displays a line separating the header from the rest of the component.Default: true/on

</td></tr><tr><td>

Chart title \[title\]

</td><td>

An alphanumeric human-readable string to identify the chart, visible to users

</td></tr><tr><td>

Description \[description\]

</td><td>

A short overview of the chart, visible to users. Use this field to explain to users in detail and in the least technical way possible what they are seeing and how to interpret it.

</td></tr><tr><td>

Show border \[showBorder\]

</td><td>

When enabled, the chart is surrounded by a border.Default: true/on

</td></tr></tbody>
</table><table id="table_dmt_dk1_fxb"><thead><tr><th>

Label/property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process optimization project \[projectId\]

</td><td>

A reference field for the Process Mining project to map

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td>

When enabled, the process map follows the filter set for the page. Toggle off to disable the filtering.Default: true/on

</td></tr><tr><td>

Connections \(%\) \[edgePercentage\]

</td><td>

The percentage of connections, or edges, to show by default. The most frequently followed connections between nodes are prioritized. For example, if you set the value to 20%, the 20% of connections with the most traffic are shown. Users can adjust this value in runtime.

</td></tr><tr><td>

Activities \(%\) \[nodePercentage\]

</td><td>

The percentage of activities/states/nodes to show by default. The most frequently engaged activities/occupied nodes are given priority. Users can adjust this value in runtime.

</td></tr><tr><td>

Case follow simulation \[enableCaseFollowSimulation\]

</td><td>

Enable to animate the connections between nodes by default. Animated connections show as moving dashed lines. The speed of the lines corresponds to the speed with which objects move between activities on the line. The thickness of the lines corresponds to the volume of traffic. Users can turn this animation on or off in runtime.

</td></tr></tbody>
</table>## Process Optimization Map component events

The Process Optimization - Map component doesn't have configurable events.

