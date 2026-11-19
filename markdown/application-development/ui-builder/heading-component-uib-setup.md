---
title: Heading component setup
description: The Heading component displays heading text in multiple styles and sizes.Properties in the Heading component have preset configuration values. You can accept these values or override them manually.The Heading component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/heading-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Heading component setup

The Heading component displays heading text in multiple styles and sizes.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Heading that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "heading-content-tree.png"\] Alt text: Shows the heading component in the UI Builder content tree

2.  Select the Heading component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "heading-presets.png"\] Alt text: Shows the list of presets available for the heading component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "heading-preset-config.png"\] Alt text: Shows details of the record title preset for the heading component

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Heading component properties

Properties in the Heading component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record title__**

    This preset sets a simple heading with a primary style at a heading 1 level that doesn't wrap. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Style
    -   Label
    -   Disable text wrap
    -   Hide bottom margin
    -   Level

### Properties

<table id="table_kan_kud_ai2"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Style\[variant\]

</td><td>

Text style.Default: **header-primary**

</td></tr><tr><td>

Label\[label\]

</td><td>

Text for the heading.

</td></tr><tr><td>

Disable text wrap\[wontWrap\]

</td><td>

Truncates the text with an ellipsis if it doesn't fit on one line.Default: **true**

</td></tr><tr><td>

Hide bottom margin\[hasNoMargin\]

</td><td>

Hides the extra space on the bottom of the text.Default: **true**

</td></tr><tr><td>

Level\[level\]

</td><td>

Defines the HTML heading element used to render the label. Options are numbers from 1 to 6.Default: **1**

</td></tr><tr><td>

Align\[align\]

</td><td>

Controls the alignment of the text. Options include:-   **Start**
-   **Center**
-   **End**
-   **Justify**

Default: **Start**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Heading component events

The Heading component doesn't have configurable events.

