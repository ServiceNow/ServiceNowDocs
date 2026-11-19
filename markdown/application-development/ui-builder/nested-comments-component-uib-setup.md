---
title: Nested Comments component setup
description: The Nested Comments component enables users to leave feedback on a piece of content.Configure the comments, actions, and display for the Nested Comments component.Select event handlers to configure the actions \(events\) provided with the Nested Comments component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/nested-comments-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Nested Comments component setup

The Nested Comments component enables users to leave feedback on a piece of content.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Nested Comments that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "nested-comments-config-content-tree.png"\] Alt text: Nested Comments component in the content tree

2.  Select the Nested Comments component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Nested Comments label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Nested Comments component properties

Configure the comments, actions, and display for the Nested Comments component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Comments|comments|Array of comments to display.|
|Actions|actions|Array of supported comment actions.|
|Reaction label|reactionLabel|Label of reaction to be used. This field is automatically set to **like**.|
|Reaction icon|reactionIcon|Icon of reaction to be used. This field is automatically set to **Thumbs Up Outline**.|
|Initial display count|initialDisplayCount|Number of comments to display on first load. This field is automatically set to 3.|
|Indentation limit|indentationLimit|Limit on indentation for nested comments. The maximum value is 7. This field is automatically set to 3.|

## Nested Comments component events

Select event handlers to configure the actions \(events\) provided with the Nested Comments component.

The Events tab shows the events used by the Recommended Actions component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Recommended Actions events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event description

|Event|Description|
|-----|-----------|
|Comment submitted|User submits a comment.|
|Action submitted|User submits a comment action.|
|Reaction toggled|User toggles a reaction.|

