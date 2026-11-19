---
title: Display Only Form component setup
description: Display Only Form is a simplified version of the form component that is often embedded in other components, such as modals. The form layout is based on the configured workspace and view, which can be overridden.Configure your Display Only Form component with these properties.The Display Only Form component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/display-only-form-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Display Only Form component setup

Display Only Form is a simplified version of the form component that is often embedded in other components, such as modals. The form layout is based on the configured workspace and view, which can be overridden.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Display Only Form that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "display-only-form-content-tree.png"\] Alt text: Shows the display only form component in the content tree

2.  Select the Display Only Form component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Display Only Form component properties

Configure your Display Only Form component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Table|table|Table of the record to display.|
|Sys ID|sysId|Sys ID of the record to display.|
|View|view|View that is used to render the form. The default view is used if this field is left blank or contains an invalid value.|
|Forced view name|forcedViewName|Specific overriding view. Overrides any view specifications from View Rules. This property is primarily used by Playbook.|
|Query|query|Encoded query string to use to filter the fields displayed.|
|Workspace ID|workspaceConfigId|Sys ID of the record's workspace configuration.|

## Display Only Form component events

The Display Only Form component doesn't have configurable events.

