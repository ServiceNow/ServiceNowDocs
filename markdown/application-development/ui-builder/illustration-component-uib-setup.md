---
title: Illustration component setup
description: Give users a way to create a custom set of illustrations in experiences by using the Illustration component.Define the attributes of the illustration used in the Illustration component with these properties.The Illustration component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/illustration-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Illustration component setup

Give users a way to create a custom set of illustrations in experiences by using the Illustration component.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Illustration that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "illustration-content-tree.png"\] Alt text: Image showing Illustration content tree

2.  Select the Illustration component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Illustration label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Illustration component properties

Define the attributes of the illustration used in the Illustration component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Illustration|illustration|Name of the illustration to use. Select an image from the dropdown that fits the use case, such as an error or a completed task.|
|Size|size|Size of the illustration asset to use. If you select **auto**, the component chooses the appropriate illustration based on the current size of the now-illustration component.|
|Alt text|alt|Alternative text to use on the `<img>` tag of the illustration. By default, there isn't any alternative text.|

## Illustration component events

The Illustration component has no configurable actions \(events\).

