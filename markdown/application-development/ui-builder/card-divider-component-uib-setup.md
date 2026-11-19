---
title: Card Base Divider component setup
description: This Card Base Divider subcomponent renders a horizontal line with configurable padding within the card content. The position of the line is the same as the component position in the Content tree.Configure the appearance of the Card Base Divider.The Card Base Divider component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/card-divider-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Card Base Divider component setup

This Card Base Divider subcomponent renders a horizontal line with configurable padding within the card content. The position of the line is the same as the component position in the Content tree.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Card Base Divider that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "card-divider-content-tree.png"\] Alt text: Content tree showing a Card Base Divider inside a Card Base Container.

2.  Select the Card Base Divider component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Card Base Divider label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Card Base Divider component properties

Configure the appearance of the Card Base Divider.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_e4k_qmd_2sb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Full width

</td><td>

fullWidth

</td><td>

When true, creates a full-width divider in the enclosing Card component.Default: false

</td></tr><tr><td>

Padding

</td><td>

blockSpacing

</td><td>

Choose the spacing between the blocks that the divider creates.Default: Large

</td></tr></tbody>
</table>## Card Base Divider component actions

The Card Base Divider component doesn't have configurable events.

