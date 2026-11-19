---
title: Checklist component setup
description: The Checklist component shows items with a check box to mark them as completed or pending.Configure the Checklist component with these properties.Select event handlers to configure the actions \(events\) provided with the Checklist component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/checklist-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Checklist component setup

The Checklist component shows items with a check box to mark them as completed or pending.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Checklist that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "checklist-label.png"\] Alt text: Checklist component in tree.

2.  Select the Checklist component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Checklist label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

    \[Omitted image "checklist-config-panel.png"\] Alt text: Shows the config panel for Checklist properties


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Checklist component properties

Configure the Checklist component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_yjl_ydz_5wb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Size of the checklist.Options are:

-   **Small**: Sets the size at 20 px
-   **Medium**: Sets the size at 24 px

Default: **Medium**

</td></tr><tr><td>

Prefixes\[prefixType\]

</td><td>

Determines if checkboxes will be ordered, and provides options for numeric or alphabetic prefixes.Options are:

-   **None**
-   **Numeric**
-   **Alphabetic**

Default: **None**

</td></tr><tr><td>

Checkbox items\[checklistData\]

</td><td>

JSON object with the configuration of the items to show in the checklist.Object properties:

-   `itemId`: Unique identifier for the checklist item
-   `checked`: To mark the checklist item as selected when the list loads, set to **true**
-   `required`: To mark the checklist item as required, set to **true**. Enabling this property adds a \* next to the item.
-   `disabled`: To disable the checklist item, set to **true**. Disabled items are not selectable.
-   `readonly`: To mark the checklist item as read-only, set to **true**. Read-only items are not selectable.
-   `invalid`: To mark the checklist item as invalid, set to **true**.
-   `order`: The order of the item in the checklist.
-   `label`: Label to display for the checklist item.
-   `hasLink`: To identify that the checklist item has a link, set to **true**. Requires `link` configuration.
-   `errorMsgForLabel`: Error message to display when unable to display the checklist item's label.
-   `link`: Configuration of link properties.
    -   `url`: Link URL.
    -   `text`: Link text.
    -   `errorMsgForLink`: Error message to display when the link URL has issues.

Default:

```json
[
    {
        "itemId": "checkbox_0",
        "checked": false,
        "required": true,
        "order": 0,
        "label": "this is item 0",
        "hasLink": true,
        "link": {
            "url": "javascript:void(0)",
            "text": "sample link 0"
        }
    },
    {
        "itemId": "checkbox_1",
        "checked": false,
        "order": 1,
        "label": "this is item 1",
        "hasLink": true,
        "link": {
            "url": "javascript:void(0)",
            "text": "sample link 1"
        }
    },
    {
        "itemId": "checkbox_2",
        "checked": false,
        "order": 2,
        "label": "this is item 2",
        "hasLink": true,
        "link": {
            "url": "javascript:void(0)",
            "text": "sample link 2"
        }
    },
    {
        "itemId": "checkbox_3",
        "checked": false,
        "order": 3,
        "label": "this is item 3",
        "hasLink": true,
        "link": {
            "url": "javascript:void(0)",
            "text": "sample link 3"
        }
    }
]
```

</td></tr><tr><td>

Open links in a new window\[opensWindow\]

</td><td>

To open links in a new window or tab \(depending on user's browser configuration\), set to **true**.Default: **false**

</td></tr><tr><td>

Allow editing\[allowEditing\]

</td><td>

To enable the end user to edit the checklist, set to **true**. Users can add, edit, or delete checklist items and links. Users can also reorder items in the list by dragging and dropping them. Default: **false**

</td></tr><tr><td>

Show edit mode\[isEditMode\]

</td><td>

Available when **Allow editing** is set to **true**. To load the checklist directly in edit mode, set to **true**.Default: **false**

</td></tr><tr><td>

Disable add link\[disableAddLink\]

</td><td>

Available when **Allow editing** is set to **true**. To disable the **Add link** button, set to **true**.Default: **false**

</td></tr><tr><td>

Checklist Edit options\[checklistEditOptions\]

</td><td>

Available when **Allow editing** is set to **true**. JSON object containing field-interactivity options to show in the edit mode. Each configuration is a boolean property, enabling any adds its corresponding toggle under the checklist item.Default:

```json
{
    "required": false,
    "disabled": false,
    "invalid": false,
    "readonly": false
}
```

</td></tr></tbody>
</table><table id="table_cgd_zpz_5wb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Empty state title\[emptyStateTitle\]

</td><td>

Primary text to display in the empty state message.

</td></tr><tr><td>

Empty state message\[emptyStateMsg\]

</td><td>

Secondary text to display in the empty state message.

</td></tr><tr><td>

Show loading spinner\[showLoadingSpinner\]

</td><td>

Displays a loading spinner to an end user to indicate that the system is loading data or saving the users change's to the checklist.

</td></tr></tbody>
</table>## Checklist component events

Select event handlers to configure the actions \(events\) provided with the Checklist component.

The Events tab shows the events used by the Checklist component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Checklist actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

<table id="table_orv_4cc_wrb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Item link clicked

</td><td>

Link text is clicked for any checklist item. The event payload contains the following:-   itemId \(string\)
-   link
    -   text \(string\)
    -   url \(string\)

</td></tr><tr><td>

Item clicked

</td><td>

A checklist item is checked or unchecked. The event payload contains the following:-   checked \(true/false\)
-   itemID \(string\)

</td></tr><tr><td>

Edit clicked

</td><td>

User selects the **Edit** action to put the checklist into edit mode

</td></tr><tr><td>

Edit cancelled

</td><td>

User selects the **Cancel** action to leave edit mode

</td></tr><tr><td>

Save clicked

</td><td>

User selects the **Save** action in edit mode to save changes to the checklist.Payload:

-   actionType
-   data

</td></tr></tbody>
</table>Checklist event handler script

The following script can serve as the event handler for both the **Item link clicked** and **Item clicked** events:

```
/**
 * @param {params} params
 * @param {api} params.api
 * @param {any} params.event
 * @param {any} params.imports
 * @param {ApiHelpers} params.helpers
 */
function handler({
    api,
    event,
    helpers,
    imports
}) {
    console.log(event.payload);
    // const {itemId, checked} = event.payload;
    api.setState('payload', JSON.stringify(event.payload));
}
```

