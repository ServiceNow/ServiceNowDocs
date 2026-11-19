---
title: Loader custom component setup
description: The Loader custom component enables users to create a context-specific loading experience by placing a custom Lottie animation with an optional progress bar and label.Configure Loader custom by setting these properties.Select event handlers to configure the events provided with the Loader custom component. Event handlers work with data resources to link the Loader custom actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/loader-custom-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Loader custom component setup

The Loader custom component enables users to create a context-specific loading experience by placing a custom Lottie animation with an optional progress bar and label.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Loader custom that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "loader-custom-content-tree.png"\] Alt text: Loader custom in the UI Builder content tree.

2.  Select the Loader custom component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "loader-custom-config.png"\] Alt text: Loader custom in the UI Builder configuration panel.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Loader custom component properties

Configure Loader custom by setting these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Animation properties\[configAnimation\]

</td><td>

A JSON object that holds all the information needed to render the animation. It contains the following properties:-   `src` \(string, sets the source of the animation file\)
-   `tokenID` \(string, identifies the token associated with the animation\)
-   `loop` \(boolean, determines whether the animation loops\)
-   `autoplay` \(boolean, determines whether the animation starts automatically\)

</td></tr></tbody>
</table><table id="table_j3k_cwv_x2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Optional label that displays with the animation.

</td></tr><tr><td>

Announce label\[announceLabel\]

</td><td>

Enable this property to announce the label when the component is rendered \(for screen reader users\).Default: **False**

</td></tr></tbody>
</table><table id="table_d1q_qwv_x2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Sets the size of the progress bar and label to accompany the animation. Options include **Small**, **Medium**, and **Large**.Default: **Medium**

</td></tr><tr><td>

Progress bar properties\[progressBarProps\]

</td><td>

An object that holds all the information needed to render the progress bar. It contains the following properties:-   `pathType` \(string\)

Choices are:

    -   **initial**
    -   **positive**
    -   **alert**
    -   **error**
    -   **inactive**
    -   **pink**
    -   **green**
    -   **orange**
    -   **gray**
-   `max` \(number\)

The maximum value for the progress bar, representing the full extent of the task.

-   `value` \(number\)

The current value of the progress bar, representing the progress of the task.


Default: No default value

</td></tr></tbody>
</table>## Loader custom component events

Select event handlers to configure the events provided with the Loader custom component. Event handlers work with data resources to link the Loader custom actions to the data you want to display to your users.

The Events tab shows the events used by the Loader custom component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Loader custom actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Loader custom animation visible\[NOW\_LOADER\_CUSTOM\#ANIMATION\_VISIBLE\]

</td><td>

Dispatched when the Lottie animation is rendered on the page.

</td></tr></tbody>
</table>