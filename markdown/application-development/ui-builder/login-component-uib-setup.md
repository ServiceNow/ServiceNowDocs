---
title: Login component setup
description: The Login component authenticates users for your application.You can configure the Login component by adding text, a destination URL, and a logo.Select event handlers to configure the actions \(events\) provided with the Login component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/login-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Login component setup

The Login component authenticates users for your application.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: ui\_builder\_admin

## Procedure

1.  Define a label for your Login component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "login-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Login component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Login component label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Login component properties

You can configure the Login component by adding text, a destination URL, and a logo.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Logo|logoUrl|Reference to the company logo image. You can enter a URL or you can enter the name of the image \[db\_image\] record in your instance.|
|Heading|heading|Text that appears at the top of the login component.|
|Label for SSO|ssoLabel|A label to specify an SSO login.|
|Destination url|destinationUrl|For multi-SSO, this the target page users are taken to after they log into the instance.|

## Login component events

Select event handlers to configure the actions \(events\) provided with the Login component.

The Events tab shows the events used by the Recommended Actions component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Login events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|User Triggered Action|User triggers an action. For example, the event dispatches when the user clicks **Forgot password**.|
|Login Successful|User enters valid login credentials.|
|Login Failed|User enters invalid login credentials.|

