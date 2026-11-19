---
title: Now Assist context menu component setup
description: The Now Assist context menu \(NAcm\) component is a configurable UIB component used to implement Now Assist context menu in your application. Use NAcm with active skills, available NAcm configurations, or custom NAcm configurations to configure Now Assist actions.Configure the context menu type, actions, skills, trigger properties, recommendation dialog properties, target record table ID, record ID, granular feedback properties, and payload in the NAcm component with these properties.Select event handlers to configure the action \(event\) provided with the NAcm component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/nacm-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 9
keywords: [Now Assist context menu]
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Now Assist context menu component setup

The Now Assist context menu \(NAcm\) component is a configurable UIB component used to implement Now Assist context menu in your application. Use NAcm with active skills, available NAcm configurations, or custom NAcm configurations to configure Now Assist actions.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for NAcm that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the NAcm component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.\[Omitted image "nacm-props.png"\] Alt text: Shows a portion of the configurable properties for the NAcm component in the Config tab


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Now Assist context menu component properties

Configure the context menu type, actions, skills, trigger properties, recommendation dialog properties, target record table ID, record ID, granular feedback properties, and payload in the NAcm component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record table\[documentTableName\]

</td><td>

The table containing the target records on which to apply the Now Assist actions. For example, if using the NAcm component to summarize an incident, then configure this property with the sys\_id of the incident table.

</td></tr><tr><td>

Record ID\[documentSysId\]

</td><td>

The ID of the record to read from the record table. Use dynamic binding to configure this property. For example, if using the NAcm component to summarize an incident, then configure this property to link to the incident sys\_id column in the incident table.

</td></tr><tr><td>

Variant\[variant\]

</td><td>

The type of NAcm component. The NAcm component’s variant depends on the intended use case and the contextual information that the component must use to generate an output. Options: -   **Fixed**: Places the component as a fixed element \(summary card\) in the page. This variant is suitable when using data from multiple sources. For example, case summarization.
-   **Draggable**: Places the component as a traveling icon which opens a draggable recommendation dialog \(modeless dialog\) when triggered. This variant is suitable when using data from a single element. For example, email composition.

Default: Draggable

</td></tr><tr><td>

Component ID

\[componentKey\]

</td><td>

Unique identifier for the component. Use alphanumeric values without special characters.

</td></tr><tr><td>

Skill ID

 \[skillId\]

</td><td>

The skill ID to use in the NAcm configuration. Verify that you activate the skills in **Admin Center &gt; Now Assist Admin &gt; Now Assist Experiences &gt; Now Assist context menu &gt; Available** before using the skill ID in NAcm.

 For more information about skills, see [Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills.md).**Note:** **Skill ID**, **Configuration ID**, and **NAcm configuration** correspond to Now Assist actions. Configure only one of these properties

</td></tr><tr><td>

Configuration ID

 \[nacmConfig\]

</td><td>

List of available NAcm configurations. These configurations are made available based on the plugins you use.**Note:** **Skill ID**, **Configuration ID**, and **NAcm configuration** correspond to Now Assist actions. Configure only one of these properties

</td></tr><tr><td>

NAcm configuration

 \[adminConfig\]

</td><td>

Configuration of the NAcm actions as a JSON object. Use this property to define a different NAcm configuration than those available in existing NAcm configurations or skills.

 **Note:** **Skill ID**, **Configuration ID**, and **NAcm configuration** correspond to Now Assist actions. Configure only one of these properties

 Default: `{}`

</td></tr><tr><td>

AMB channel \[ambChannelName\]

</td><td>

Name of the Asynchronous Message Bus \(AMB\) channel for the component to use. Don’t add any special characters such as `'@' ',' '/'` in the channel name.

</td></tr><tr><td>

Caller type

 \[caller\]

</td><td>

Specifies whether the component is being configured for mobile-based applications, UI16, or a workspace. The configuration here doesn’t affect how the component functions but is used for tracking analytics and other logics.Options:

-   **Mobile**
-   **UI16**
-   **Workspace**

Default: Workspace

</td></tr><tr><td>

Trigger properties

 \[buttonProps\]

</td><td>

Configuration of the preset menu trigger button’s properties as a JSON object.The following list describes the button object’s properties:

-   `size`: The size of the button to use. Available configurations are: `sm` \(small\), `md` \(medium\), and `lg` \(large\).
-   `variant`: The type of the button to use. Available configurations are: `primary`, `secondary`, and `tertiary`.
-   `label`: The label for the button.
-   `icon`: The icon to show in the button.
-   `tooltipContent`: The tooltip content to show for the button.
-   `isCaretForDropdown`: To show the Now Assist icon, set to true.
-   `strictlyUseDefaultPresetAction`: To use the preset trigger as a button regardless of `selectedText` configuration, set to true. To use the preset trigger as a drop-down, set to false. This property requires the `defaultPresetAction` property.
-   `hideButtonOnDialog`: To hide the button when the dialog appears, set to true.
-   `isFullWidthButton`: To let the button occupy the full width of the container, set to true.
-   `hasShadow`: To remove the shadow around the button in the fixed variant, set to true.

Default:

```json
{
    "size": "sm",
    "variant": "secondary",
    "label": "",
    "icon": "ai-sparkle-outline",
    "tooltipContent": "Test Tooltip",
    "isCaretForDropdown": false,
    "strictlyUseDefaultPresetAction": false,
    "hideButtonOnDialog": true,
}

```

</td></tr><tr><td>

Recommendation dialog properties\[recommendationDialogProps\]

</td><td>

Configuration of the recommendation dialog’s properties as a JSON object.The following list describes the recommendation dialog properties:

-   `footerLabel`: Footer label for the recommendation dialog.
-   `offsetLeft`: The left offset for the dialog in the initial render as a percentage.
-   `offsetTop`: The top offset for the dialog in the initial render as a percentage.
-   `height`: The height of the dialog in pixels. Height should be at least 160. If configured less than 160, the component uses a height of 160.
-   `width`: The width of the dialog in pixels. Width should be at least 320. If configured less than 320, the component uses a width of 320.
-   `insertButtonLabel`: The label for the insert button in the dialog.
-   `refineCount`: The maximum number of refinements allowed in a single flow.
    -   &gt; 0, the component allows only the configured number of refinements.
    -   &lt; 0, the component allows infinite refinements.
    -   0, the component shows a disabled **Refine** button with a warning in the footer.
    -   If configured as a non-numeric value, the component defaults to allowing infinite refinements.
-   `hideInsertButton`: To hide the insert button, set to true.
-   `isDialogHoisted`: To hoist the dialog, set to true.
-   `fixedVariantInitialLineCount`: The maximum number of lines shown in the component’s fixed variant when the component loads.
-   `fixedVariantShowMoreLineCount`: The maximum number of additional lines shown in the component’s fixed variant when the **Show more** button is selected.
-   `additionalInfoTip`: The tooltip text to render when the info icon is selected or hovered on.
-   `headerInitialLabel`: Recommendation dialog’s header label when the component loads.
-   `headerLoadingLabel`: Recommendation dialog’s header label when the component is loading.
-   `headerLoadedLabel`: Recommendation dialog’s header label when the component has loaded.

Default:

```json
{
            "footerLabel": "Check AI-generated content for accuracy.",
            "offsetLeft": 10,
            "offsetTop": 10,
            "height": 400,
            "width": 600,
            "insertButtonLabel": "Insert",
            "refineCount": "1",
            "hideInsertButton": false,
            "isDialogHoisted": true,
            "additionalInfoTooltip": "AI generates text by using relevant context. Be sure to check for accuracy."
        }

```

</td></tr><tr><td>

Granular feedback properties\[feedbackConfig\]

</td><td>

Configuration of the feedback properties as a JSON object.The following list shows the supported properties:

-   Positive feedback
    -   Heading
    -   Items
-   Negative feedback
    -   Heading
    -   Items

Default: `{}`

</td></tr><tr><td>

Selected text

 \[selectedText\]

</td><td>

Required when implementing text-based Now Assist actions like elaborate, shorten, and so on Configuration to identify when a user selects text for the Now Assist actions.

</td></tr><tr><td>

Timeout error message\[timeoutErrorMessage\]

</td><td>

Timeout error message text to show. The component uses a default error message if this isn’t configured.

</td></tr><tr><td>

Draft text\[draftedText\]

</td><td>

Required when implementing text-based Now Assist actions like elaborate or shorten. Configuration to identify the text block in which to perform the Now Assist actions. The common out of the box actions rely on selected text. So, if selected text is missing, NAcm uses drafted text.

</td></tr><tr><td>

Payload\[payload\]

</td><td>

JSON object with the configuration of a custom payload to pass to the component. This payload is also sent as a parameter in the Now Assist action when it’s invoked.

 Default: `{}`

</td></tr><tr><td>

Disable skeleton

 \[renderDisabledSkeleton\]

</td><td>

To render a disabled skeleton to avoid layout shift, set to true. Otherwise, the component renders when the configurations are ready.Default: false

</td></tr></tbody>
</table>## Now Assist context menu component events

Select event handlers to configure the action \(event\) provided with the NAcm component.

The Events tab shows the events used by the NAcm component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the NAcm actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "nacm-events.png"\] Alt text: NAcm default events tab showing available events

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Call to action selectedSN\_NACM\#CTA\_CLICKED

</td><td>

Dispatched when the user selects the call-to-action \(CTA\) button.

</td></tr><tr><td>

Component RenderedSN\_NACM\#COMPONENT\_DOM\_RENDERED

</td><td>

Dispatched when the component loads. This event signals the correct configuration of NAcm.

</td></tr><tr><td>

Feedback submittedSN\_NACM\#FEEDBACK\_SUBMITTED

</td><td>

Dispatched when the user selects the feedback button.

</td></tr><tr><td>

Insert button clickedSN\_NACM\#INSERT\_RECOMMENDATION\_CLICKED

</td><td>

Dispatched when the user selects the insert button.

</td></tr><tr><td>

Menu action selectedSN\_NACM\#MENU\_ACTION\_CLICKED

</td><td>

Dispatched when the user selects a menu item.

</td></tr><tr><td>

Modeless dialog closedSN\_NACM\#RECOMMENDATION\_DIALOG\_CLOSED

</td><td>

Dispatched when the user closes the recommendation modeless-dialog.

</td></tr><tr><td>

Received updates on Record WatcherSN\_NACM\#RW\_MESSAGE\_RECEIVED

</td><td>

Dispatched when the record ID changes.

</td></tr><tr><td>

Refine action selectedSN\_NACM\#REFINE\_ACTION\_CLICKED

</td><td>

Dispatched when the user selects the refine menu item.

</td></tr></tbody>
</table>