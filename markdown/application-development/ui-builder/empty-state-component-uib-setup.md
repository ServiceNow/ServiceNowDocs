---
title: Empty State component setup
description: The Empty State component lets a user know that an area of the experience is not populated with data. This template component displays a message containing an illustration, header, description, and button.Configure the contents and appearance of your Empty State component with these properties.Select event handlers to configure the actions \(events\) provided with the Empty State component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/empty-state-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Empty State component setup

The Empty State component lets a user know that an area of the experience is not populated with data. This template component displays a message containing an illustration, header, description, and button.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Empty State that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "empty-state-content-tree.png"\] Alt text: Content tree showing custom name for an Empty State component.

2.  Select the Empty State component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Empty State label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Empty State component properties

Configure the contents and appearance of your Empty State component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_i5y_tcr_znb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Illustration

</td><td>

illustration

</td><td>

Name of the illustration to use.Default: no-search-results

</td></tr><tr><td>

Heading

</td><td>

heading

</td><td>

Primary text to display in the empty state messageType: `{label: string, level: ("1" | "2" | "3" | "4" | "5" | "6")}`

 Default: `{\"label\":\"No results found\",\"level\":\"3\"}`

</td></tr><tr><td>

Content

</td><td>

content

</td><td>

Secondary text to display in the empty state messageType: string

 Default: Please try your search again

</td></tr><tr><td>

Actions

</td><td>

actions

</td><td>

Array of button objects. The object keys are the same as the properties in the [Button component](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/now-components/now-button/api).Choices:

-   `label` \{string\}: Required. Label describing the action.
-   `icon` \{strring\}: Icon displayed with the label
-   `variant` \{string\}: Button style variant
-   `disabled` \{Boolean\}: When `true`, mutes the button color and disables user click interactions.
-   `tooltipContent` \{string\}: Text to display in the optional tooltip associated with the button
-   `configAria` \{object\}: ARIA attributes to set on the action button
-   `clickActionType` \{string\}: Overrides the default action type dispatched when the user clicks the action button. Default: "NOW\_TEMPLATE\_MESSAGE\_EMPTY\_STATE\#ACTION\_CLICKED"

</td></tr><tr><td>

Alignment

</td><td>

alignment

</td><td>

Sets the alignmentChoices: vertical-centered or horizontal

 Default: vertical-centered

</td></tr></tbody>
</table>## Empty State component events

Select event handlers to configure the actions \(events\) provided with the Empty State component.

The Events tab shows the events used by the Empty State component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Empty State actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_jxq_lvr_znb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template message empty state action clicked

</td><td>

Dispatched when the user clicks a button defined in the `actions` property. The payload includes a reference to the clicked action. You can override this action type by configuring the `clickActionType` property.Payload: `{action: Object}`

</td></tr></tbody>
</table>