---
title: Icon component setup
description: The Icon component is a symbol used to launch an action, add clarity, or provide additional context.Select the Icon and its size with these properties.The Icon component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/icon-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Icon component setup

The Icon component is a symbol used to launch an action, add clarity, or provide additional context.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Icon that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "icon-content-tree.png"\] Alt text: Icon component in content tree showing customized label

2.  Select the Icon component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Icon label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Icon component properties

Select the Icon and its size with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_s5c_rsy_znb"><thead><tr><th>

Label\[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Icon\[icon\]

</td><td>

Name of the icon in dash-case, including the **-fill** or **-outline** suffix to indicate whether the icon is filled or outlined. Users can define a custom name not already used by the NDS library. This custom name should include the asset's file extension. Custom icons can be of any standard image format but are rendered using the **.img** extension. The component doesn't store any references to the custom icon, and won't be able to cache it internally.

**Note:** See [https://developer.servicenow.com/dev.do\#!/reference/next-experience/utah/now-components/now-icon/gallery](https://developer.servicenow.com/dev.do#!/reference/next-experience/utah/now-components/now-icon/gallery)for more information.

</td></tr><tr><td>

Size\[size\]

</td><td>

Icon sizeChoices: Small, Medium, Large, Extra Large

 Default: Medium

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

Configures the ARIA properties. Possible properties are:-   aria-braillelabel
-   aria-brailleroledescription
-   aria-colindextext
-   aria-description
-   aria-label \(Required to be accessible using a screen reader\)
-   aria-placeholder
-   aria-roledescription
-   aria-rowindextext
-   aria-valuetext

</td></tr></tbody>
</table>## Icon component events

The Icon component doesn't have configurable events.

