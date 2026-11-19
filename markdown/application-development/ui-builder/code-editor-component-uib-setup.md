---
title: Now Code Editor component setup
description: The Now Code Editor component enables users to edit snippets of code and markup languages. Now Code Editor supports JavaScript, JSON, CSS, XML, and HTML languages.Configure the code editing and debugging capabilities of the Now Code Editor component.Select event handlers to configure the actions \(events\) provided with the Now Code Editor component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/code-editor-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Now Code Editor component setup

The Now Code Editor component enables users to edit snippets of code and markup languages. Now Code Editor supports JavaScript, JSON, CSS, XML, and HTML languages.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Now Code Editor that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "nce-content-panel.png"\] Alt text: Code editor content tree

2.  Select the Now Code Editor component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Now Code Editor label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Now Code Editor component properties

Configure the code editing and debugging capabilities of the Now Code Editor component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Language|language|Scripting language or markup language of the snippet displayed in the editor.|
|Script type|isClientScript|Server side JavaScript or client side JavaScript. This field applies only when the language is JavaScript.|
|Scope|scope|Application scope of the script. This field applies only when the language is JavaScript.|
|Initial content|content|Initial text loaded in the editor.|
|Disable editing|readOnly|Option to disable editing in the editor.|
|Disable word wrap|disableWordWrap|Option to disable word-wrapping in the editor.|
|Disable full screen|disableFullScreen|Option to disable full screen view of the editor.|
|Hide toolbar|hideToolbar|Option to hide the toolbar in the editor.|
|Hide gutter|hideGutter|Option to hide the gutter section in the editor.|
|Hide minimap|disableMinimap|Option to hide the minimap in the editor.|
|Disable debugging|disableDebugging|Option to disable debugging in the editor.|
|Record type|recordType|Name of the table associated with the script.|
|Script field|scriptField|Script field of the table associated with the script.|
|Sys id|sysId|Sys ID of the record.|
|Autocomplete suggestions|autocompleteSuggestions|Option to show auto-complete suggestions for the script languages in the editor.|
|Editor mode|editorMode|Mode of the editor. The available options are normal and diff \(side by side\).|
|Compare with|originalContent|Content to compare with the initial content in the diff mode.|
|Disable switching between modes|disableToggleDiffView|Option to toggle between the normal and diff mode in the editor.|
|Custom gutter icons|customIcons|Option to enable custom icons in the gutter area of the editor. This field applies only when the language is JSON.|

## Now Code Editor component events

Select event handlers to configure the actions \(events\) provided with the Now Code Editor component.

The Events tab shows the events used by the Now Code Editor component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Now Code Editor events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Editor content changed|Action dispatched when the user changes the content in the editor.|
|Editor focus changed|Action dispatched when the user changes focus in the editor.|
|Editor full screen toggled|Action dispatched when the user toggles to full screen.|
|Editor mode changed|Action dispatched when the user changes the editor mode.|

