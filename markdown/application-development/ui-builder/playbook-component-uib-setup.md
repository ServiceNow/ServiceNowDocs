---
title: Playbook component setup
description: The Playbook component provides fulfillers a way to visualize and interact with business process workflows in real time, via a simple, task-oriented view.Configure the Playbook with these properties.Select event handlers to configure the actions \(events\) provided with the Playbook component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/playbook-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Playbook component setup

The Playbook component provides fulfillers a way to visualize and interact with business process workflows in real time, via a simple, task-oriented view.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

Make sure you are in the application scope containing a playbook.

## Procedure

1.  Define a label for your Playbook that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "playbook-content-tree.png"\] Alt text: Playbook content tree

2.  Select the Playbook component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Playbook label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Playbook component properties

Configure the Playbook with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Parent table|parentTable|Parent table containing a playbook.|
|Parent Sys ID|parentSysId|Sys ID of the parent record containing the playbook.|
|Playbook Experience|playbookExperienceId|Playbook Experience that the playbook should use. This will default to the Global Playbook Experience.|
|User ID|workspaceUserId|Current user ID to use with filtering and assignment.|
|Compact Mode|condensedMode|Option to display the playbook compact mode.|

## Playbook component events

Select event handlers to configure the actions \(events\) provided with the Playbook component.

The Events tab shows the events used by the Playbook component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Playbook actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Preview Record|Action dispatched to preview a record.|
|Add Notifications|Action dispatched once the field declarative action execution has completed. This action is only dispatched when the record contains fields with field decorators.|

