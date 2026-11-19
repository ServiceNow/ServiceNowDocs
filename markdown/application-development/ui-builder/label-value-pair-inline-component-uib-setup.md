---
title: Label Value component setup
description: Use the Label Value component to display a label and text string side by side with minimal formattingDefine the text and appearance of your Label Value component with these properties.The Label Value component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/label-value-pair-inline-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Label Value component setup

Use the Label Value component to display a label and text string side by side with minimal formatting

## Before you begin

This task assumes you have placed the Label Value component on the page and are ready to configure the component properties and events. For instructions on accessing and using the UI Builder toolbox, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md). For instructions on overriding styles using the Styles pane, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-styling-to-component.md).

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Label Value that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "label-value-pair-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Label Value component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Label Value label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Label Value component properties

Define the text and appearance of your Label Value component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Label|label|The text of the label|
|Value|value|The text of the value|
|Reversed|reversed|When enabled the order of the label and value is reversed, so the value appears before the label.|
|Truncated|truncated|When enabled the text of the label appears as a single line and limited to the width of the selected layout.|

## Label value component events

The Label Value component has no configurable actions \(events\).

