---
title: Image component setup
description: The Image component displays a static image.Properties in the Image component have available preset configuration values. You can accept these values or override them manually.The Image component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/image-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Image component setup

The Image component displays a static image.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Image that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "image-content-tree.png"\] Alt text: Shows the unique component name for image in the content tree

2.  Select the Image component, using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "image-preset-selection.png"\] Alt text: Shows the list of presets for the image component and the option to select none

3.  Select either **None** to configure the component properties manually or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "image-preset-config.png"\] Alt text: Shows the configuration panel for connecting the preset to the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md)


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Image component properties

Properties in the Image component have available preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record header image__**

    This preset places an image in the center of the container with its original proportions. The ALT text description of the image that the screen reader can announce is defined. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Image source
    -   Fit
    -   Position
    -   Alt text

### Properties

<table id="table_k3f_2kr_wtb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Image source \[src\]

</td><td>

URL to the image you want to display in your component.

</td></tr><tr><td>

Sources\[sources\]

</td><td>

An array of source objects to use in responsive images. Each source object contains:-   **Srcset** \(required\)
-   **Type**
-   **Media**
-   **Sizes**

```
[
  {
    "name": "srcset",
    "label": "Srcset",
    "fieldType": "string",
    "mandatory": true
  },
  {
    "name": "type",
    "label": "Type",
    "fieldType": "string",
    "mandatory": false
  },
  {
    "name": "media",
    "label": "Media",
    "fieldType": "string",
    "mandatory": false
  },
  {
    "name": "sizes",
    "label": "Sizes",
    "fieldType": "string",
    "mandatory": false
  }
]
```

</td></tr><tr><td>

Fit \[fit\]

</td><td>

Defines how the image fits in its container. The choices are: -   **Fill**: Fills the container with the image on all sides. The proportions of the image are changed to force it to fit in the container.
-   **Contain**: Expands or shrinks the image to fill the height of the container. This setting retains the proportions of the image.
-   **Cover**: Fills the container but retains the proportions of the image. Unless the height of the container is defined, the container expands to accommodate the proportions of the image. If the height of the container is defined, part of the image fills the container. This is the default setting in the preset.
-   **Scale down**: Reduces the size of the image proportionally so it fits in the container.
-   **None**: No change to the image with regard to the container

</td></tr><tr><td>

Position \[position\]

</td><td>

Anchors the image to a position inside if it's larger than the container. You can center the image or place it in any of the four corners. The default setting in the preset centers the image.

</td></tr><tr><td>

Alt text \[alt\]

</td><td>

Description of the image that a screen reader can announce.

</td></tr><tr><td>

Height \[height\]

</td><td>

Static height for the container. If no height is defined \(default\), the container takes the height of the image.

</td></tr></tbody>
</table>### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Image component events

The Image component doesn't have configurable events.

