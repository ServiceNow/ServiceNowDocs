---
title: Animated icon component setup
description: The Animated icon component is a numeric indicator that displays a count of unread messages, notifications, and so on.Configure the size and ARIA properties for your Animated icon component.The Animated icon component has no events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/animated-icon-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Animated icon component setup

The Animated icon component is a numeric indicator that displays a count of unread messages, notifications, and so on.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Animated icon that differentiates it from other components in the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Animated icon component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Animated icon label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Animated icon component properties

Configure the size and ARIA properties for your Animated icon component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_tsr_g5y_znb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Icon\[icon\]

</td><td>

There is no need to set this property, as the default is **Ai-sparkle-fill**. There are no other animated icons available.

</td></tr><tr><td>

Size\[size\]

</td><td>

​Size of the animated icon.Default: **medium**

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the dropdown. The value of each key is an object that contains an ARIA property and corresponding value. These ARIA properties are set on the specified element.

</td></tr></tbody>
</table>## Animated icon component events

The Animated icon component has no events.

