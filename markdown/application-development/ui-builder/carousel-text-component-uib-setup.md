---
title: Carousel text component setup
description: The Carousel text component enables users to configure a series of rotating text messages that display with animated transitions. Configure the content and styling of Carousel text.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/carousel-text-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Carousel text component setup

The Carousel text component enables users to configure a series of rotating text messages that display with animated transitions.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Carousel text that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "carousel-text-content-tree.png"\] Alt text: Carousel text in the UI Builder content tree.

2.  Select the Carousel text component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "carousel-text-config.png"\] Alt text: Carousel text in the UI Builder configuration panel.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Carousel text component properties

Configure the content and styling of Carousel text.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Items\[items\]

</td><td>

List of labels that rotate in the order specified.

</td></tr><tr><td>

CSS\[css\]

</td><td>

Field for adding custom CSS to style the text. CSS entered here is wrapped in a &lt;style&gt; tag and applied to the HTML elements within the carousel text.

</td></tr><tr><td>

Announce label\[announceLabel\]

</td><td>

Determines which label is announced to screen readers. Options include:-   **First**: The first label is announced once.
-   **All**: Each label is announced as it is displayed.
-   **None**: No labels are announced.

Default: **First**

</td></tr></tbody>
</table>