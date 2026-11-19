---
title: MFA validate component setup
description: The MFA validate component enables a user to log into their instance with credentials and a generated passcode supplied by an multifactor authentication \(MFA\) authentication app, like Okta Verify or Google Authenticator.Configure the heading for the MFA validate component.Select event handlers to configure the actions \(events\) provided with the MFA validate component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/mfa-validate-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# MFA validate component setup

The MFA validate component enables a user to log into their instance with credentials and a generated passcode supplied by an multifactor authentication \(MFA\) authentication app, like Okta Verify or Google Authenticator.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for MFA validate that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "mfa-setup-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the MFA validate component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the MFA validate label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## MFA validate component properties

Configure the heading for the MFA validate component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Heading|heading|Text to introduce the component.|

## MFA validate component events

Select event handlers to configure the actions \(events\) provided with the MFA validate component.

The Events tab shows the events used by the MFA validate component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the MFA validate events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Device paired successfully|The device has been properly configured to accept an MFA passcode before logging into the instance.|
|Validation failed|The MFA authenticator app did not accept the verification code sent to pair the device.|
|Device unpaired|The device has not been properly configured to accept an MFA passcode before logging into the instance.|
|MFA disabled|The instance does not have multifactor authentication enabled.|
|Forget all browsers|Set your instance to prompt MFA when a user logs in from a new device or browser.|

