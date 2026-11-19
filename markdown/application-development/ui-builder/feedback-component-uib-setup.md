---
title: Feedback component setup
description: Feedback captures granular feedback when a user selects the thumbs-up or thumbs-down icon. For example, in a case summary, chat summary, Now Assist panel, and Now Assist popover. The options are configurable to be radio buttons or checklists to enable users to select one or multiple options in their feedback.Configure the text such as heading, options, and text boxes in the positive and negative popovers in the Feedback component with these properties.Select event handlers to configure the action \(event\) provided with the Feedback component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/feedback-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Feedback component setup

Feedback captures granular feedback when a user selects the thumbs-up or thumbs-down icon. For example, in a case summary, chat summary, Now Assist panel, and Now Assist popover. The options are configurable to be radio buttons or checklists to enable users to select one or multiple options in their feedback.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Feedback that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "feedback-uib-select.png"\] Alt text: Shows the Feedback component in the UI Builder content tree

2.  Select the Feedback component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "feedback-uib-props.png"\] Alt text: Shows a portion of the configurable properties for the Feedback component in the config tab


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Feedback component properties

Configure the text such as heading, options, and text boxes in the positive and negative popovers in the Feedback component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Load state\[loadState\]

</td><td>

Select the feedback icon to present as pre-selected when the component loads.

 Available options are:

-   **None**
-   **Thumbs up**
-   **Thumbs down**

 Default: **None**

</td></tr><tr><td>

Positive feedback\[positiveFeedback\]

</td><td>

The heading text and options to display in the positive feedback popover.

 By default, this property is configured as an array of objects. Edit this array based on your requirement, such as selecting option type as radio buttons instead of checklist or adding more options.

 Available options are:

-   `heading`: Heading text for the feedback popover
-   `items`: Array containing the configuration of the options and the text area's character limit. Options and text area configurations are separate "items". The following list describes the objects in this array:
    -   `type`: Configuration of the option type and the text area. Supported option types are: `checklist` or `radio`. To configure character limit in the text area, set this property as `textarea` and then specify the value of `maxlength`.
    -   `value`: Applicable to option configuration. Array with the configuration of the options to display. The following list describes the objects in this array:
        -   `id`: Unique string identifier for the option
        -   `label`: Option text
        -   `checked`: To pre-select the option when the component loads, set to **true**.
    -   `maxlength`: Applicable to text area configuration. Maximum characters allowed in the text area. Requires separate object notation in the array with `type` set as `textarea`, as shown in the default value.

 Default:

```json
{
    "heading": "Tell us why you liked the Now Assist response",
    "items": [
        {
            "type": "checklist",
            "value": [
                {
                    "id": "one",
                    "label": "It was clear and concise",
                    "checked": false
                },
                {
                    "id": "two",
                    "label": "It was accurate and reliable",
                    "checked": false
                }
            ]
        },
        {
            "type": "textarea",
            "maxlength": 300
        }
    ]
}
```

</td></tr><tr><td>

Negative feedback\[negativeFeedback\]

</td><td>

The heading text and options to display in the negative feedback popover.

 By default, this property is configured as an array of objects. Edit this array based on your requirement, such as selecting option type as radio buttons instead of checklist or adding more options. For details about object properties, see the description in **Positive feedback**.

 Default:

```json
{

    "heading": "Tell us more to help Now Assist improve",
    "items": [
        {
            "type": "checklist",
            "value": [
                {
                    "id": "one",
                    "label": "Missed important details",
                    "checked": false
                },
                {
                    "id": "two",
                    "label": "Included irrelevant details",
                    "checked": false
                }
            ]
        },
        {
            "type": "textarea",
            "maxlength": 300
        }
    ]
}
```

</td></tr><tr><td>

Manage submit\[manageSubmit\]

</td><td>

Select to override the default functionality of the **Submit** button.

 Default: **false**

</td></tr><tr><td>

Error\[error\]

</td><td>

The handling of the popover when the **Submit** button is selected. By default, this property is configured to close the feedback popover when the **Submit** button is selected.

 Edit the default array of objects based on your requirement.

 **Note:** Ensure that **Manage submit** is selected.

 Default:

```json
{"isError":false,"timestamp":-1}
```

</td></tr></tbody>
</table>## Feedback component events

Select event handlers to configure the action \(event\) provided with the Feedback component.

The **Events** tab shows the events used by the Feedback component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Feedback actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "feedback-uib-events.png"\] Alt text: Shows the events available for the Feedback component

### Event descriptions

|Event|Description|
|-----|-----------|
|Feedback button clicked|Triggers when the thumbs-up or thumbs-down icon is selected.|
|Granular feedback submit clicked|Triggers when the **Submit** button is selected.|

