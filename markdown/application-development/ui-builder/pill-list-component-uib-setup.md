---
title: Pill List component setup
description: The Pill List component display a list of pills to use for navigation or filtering.Configure which pills to display, the number of pills to display, and the Pill List title.Select event handlers to configure the actions \(events\) provided with the Pill List component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/pill-list-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Pill List component setup

The Pill List component display a list of pills to use for navigation or filtering.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your pill list that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "pill-list-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Pill List component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Pill List label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Pill List component properties

Configure which pills to display, the number of pills to display, and the Pill List title.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_wbl_qsn_mnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

title

</td><td>

Title to describe the list of pills. For example, to describe a list of tags that are related to the page content, you would enter `Related Tags`.

</td></tr><tr><td>

Pills

</td><td>

pills

</td><td>

Array of objects to display in pills. Each object should contain a `pillText` to define the text of the pill. It should also contain a `pillValue` object. You can use the `pillValue` from the payload data to trigger an action. For example, to configure a pill that navigates to Service Portal, you would enter the following:```
[ { "pillText": "Service Portal", "pillValue": { "url": "<instance-name>.service-now.com/sp"} } ] 
```

</td></tr><tr><td>

Pill limit

</td><td>

maxPillLimit

</td><td>

Maximum number of pills to display.

</td></tr></tbody>
</table>## Pill List component events

Select event handlers to configure the actions \(events\) provided with the Pill List component.

The Events tab shows the events used by the Pill List component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Pill List actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Action Pill Clicked|User clicks a pill from the list.|

