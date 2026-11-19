---
title: Loader component setup
description: The Loader components indicate a loading state with an animated spinner.Define the loader size, text, and labelled action button of your Loader component with these properties.Select event handlers to configure the actions \(events\) provided with the Loader component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/loader-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Loader component setup

The Loader components indicate a loading state with an animated spinner.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Loader that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "loader-content-tree.png"\] Alt text: Image showing loader component content tree

2.  Select the Loader component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Loader label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Loader component properties

Define the loader size, text, and labelled action button of your Loader component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_tm2_lqm_qnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size

</td><td>

size

</td><td>

Size of the loader spinner

</td></tr><tr><td>

Label

</td><td>

label

</td><td>

Descriptive text of the loader**Note:** If the label is not specified, the property can be left empty and won't be displayed.

</td></tr><tr><td>

Action label

</td><td>

action

</td><td>

Labelled action button**Note:** If the action label is not specified, the property can be left empty and won't be displayed.

</td></tr></tbody>
</table>## Loader component events

Select event handlers to configure the actions \(events\) provided with the Loader component.

The Events tab shows the events used by the Loader component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Loader actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Button clicked|Button clicked by the user|

