---
title: Message component setup
description: The Message component provides a framework for building messages, including text, images, and actions, from standard interactions, patterns, behaviors and applied styles.​Configure the alignment of your Message component with these properties.The Message component doesn't have configurable events \(actions\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/message-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Message component setup

The Message component provides a framework for building messages, including text, images, and actions, from standard interactions, patterns, behaviors and applied styles.​

## Before you begin

Typical use cases for the Message component include a message for empty state, feedback, and confirmation. For example, use messages to:

-   Explain an empty state situation and offer actions for next steps.​
-   Get feedback from the user.
-   Confirm a user-initiated action.

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Message component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "message-content-tree.png"\] Alt text: Message component with label displayed in the content tree

2.  Select the Message component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the message label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Message component properties

Configure the alignment of your Message component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_vfs_lbr_vnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alignment

</td><td>

alignment

</td><td>

Sets the alignment of the message to one of the following options:-   Adaptive
-   Horizontal
-   Vertical
-   Vertical centered

</td></tr></tbody>
</table>## Message component events

The Message component doesn't have configurable events \(actions\).

