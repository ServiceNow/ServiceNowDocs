---
title: Email Quick Messages component setup
description: The Email Quick Messages component enables customer service agents to use canned responses in emails to customers. The component is associated with a record to include emails as part of the record.Configure the tables and properties for your Email Quick Messages component.Select event handlers to configure the actions \(events\) provided with the Email Quick Messages component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/email-quick-msgs-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Email Quick Messages component setup

The Email Quick Messages component enables customer service agents to use canned responses in emails to customers. The component is associated with a record to include emails as part of the record.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Email Quick Messages that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-styling-to-component.md).

    \[Omitted image "email-quick-messages-content-tree.png"\] Alt text: Email Quick Messages content tree.

2.  Select the Email Quick Messages component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Email Quick Messages label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Email Quick Messages component properties

Configure the tables and properties for your Email Quick Messages component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Quick messages|activeItems|Quick messages for the target record.|

## Email Quick Messages component events

Select event handlers to configure the actions \(events\) provided with the Email Quick Messages component.

The Events tab shows the events used by the Email Quick Messages component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Email Quick Messages actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Quick message insert|Action to insert a quick message.|

