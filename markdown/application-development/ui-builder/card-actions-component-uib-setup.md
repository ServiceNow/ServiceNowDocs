---
title: Card Base Actions component setup
description: The Card Base Actions subcomponent displays one to three large action buttons on a card. Add as a subcomponent of a Card Base Container.Configure the Card Base Actions properties.Select event handlers to configure the actions \(events\) provided with the Card Base Actions component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/card-actions-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Card Base Actions component setup

The Card Base Actions subcomponent displays one to three large action buttons on a card. Add as a subcomponent of a Card Base Container.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Card Base Actions component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "card-actions-content-tree.png"\] Alt text: Card Base Actions in content tree, as a subcomponent of a Card Base Container in a Repeater.

2.  Select the Card Base Actions component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Card Base Actions label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Card Base Actions component properties

Configure the Card Base Actions properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_cz2_mnc_2sb"><thead><tr><th>

Label\[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Items\[items\]

</td><td>

An array of objects that define the buttons in the component. Configure up to three objects, one for each button. The keys for each object are properties for the Button component. For more information about these properties, see [Button](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/now-components/now-button/overview).-   `label: string` \(Required\) Label describing the action.
-   `icon: string` Icon displayed with the label.
-   `variant: string` Button style variant.
-   `disabled: boolean` Set to **true** to mute the button color and disable user click interactions.
-   `clickActionType: string = "NOW_CARD_ACTIONS#ACTION_CLICKED"` Configure to override the default action type dispatched when the user clicks the action.
-   `tooltipContent: string` Text to display in the optional tooltip associated with the button.

</td></tr></tbody>
</table>## Card Base Actions component events

Select event handlers to configure the actions \(events\) provided with the Card Base Actions component.

The Events tab shows the events used by the Card Base Actions component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Card Base Actions actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

<table id="table_gmb_5bd_2sb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card actions action clicked

</td><td>

Dispatched when the user clicks a button. The payload includes a reference to the clicked item and action. To override the action type, configure `item.clickActionType`.Payload type: `{action: Object}`

</td></tr></tbody>
</table>