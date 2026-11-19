---
title: Star Rating component setup
description: Give users a way to rate the content by using the Star Rating component.Define the star size, rating display, number of stars, and the ARIA label of your Star Rating component with these properties.Select event handlers to configure the actions \(events\) provided with the Star Rating component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/star-rating-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Star Rating component setup

Give users a way to rate the content by using the Star Rating component.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Star Rating that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [UI Builder tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).\[Omitted image "star-rating-content-tree.png"\] Alt text: Image showing star rating content tree

2.  Select the Star Rating component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Star Rating label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Star Rating component properties

Define the star size, rating display, number of stars, and the ARIA label of your Star Rating component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_y14_btp_rnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Read only\[readOnly\]

</td><td>

Display mode of the rating

</td></tr><tr><td>

Rating\[rating\]

</td><td>

Displayed rating

</td></tr><tr><td>

Size\[size\]

</td><td>

Size of the stars

</td></tr><tr><td>

Number of stars\[stars\]

</td><td>

Number of stars to be displayed

</td></tr><tr><td>

ARIA label\[ariaLabel\]

</td><td>

ARIA label for the rating

</td></tr></tbody>
</table>## Star Rating component events

Select event handlers to configure the actions \(events\) provided with the Star Rating component.

The Events tab shows the events used by the Star Rating component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Star Rating actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Star rating submitted|The star rating submitted by the user.|

