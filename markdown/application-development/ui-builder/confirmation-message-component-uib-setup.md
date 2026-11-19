---
title: Confirmation Message component setup
description: A Confirmation Message informs a user whether an operation was completed successfully or not and provides options for next steps.Configure the text and icon that appears in your Confirmation Message.Select event handlers to configure the actions \(events\) provided with the Confirmation Message component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/confirmation-message-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Confirmation Message component setup

A Confirmation Message informs a user whether an operation was completed successfully or not and provides options for next steps.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your confirmation message that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "confirmation-message-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Confirmation Messagecomponent, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Confirmation Message label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Confirmation Message component properties

Configure the text and icon that appears in your Confirmation Message.

<table id="table_vwn_5vg_mnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Icon

</td><td>

icon

</td><td>

Icon to display in the confirmation message.

</td></tr><tr><td>

Icon Status

</td><td>

iconStatus

</td><td>

Icon color to indicate priority.

</td></tr><tr><td>

Header message

</td><td>

header

</td><td>

Main message to display to the user.

</td></tr><tr><td>

Header level

</td><td>

headerLevel

</td><td>

Size of the header message. To use a large header, select a lower number like 1 or 2.

</td></tr><tr><td>

Caption

</td><td>

caption

</td><td>

Text that appears after the heading.

</td></tr><tr><td>

More information

</td><td>

moreInfo

</td><td>

Text that appears after the caption. You may choose to enter information to set expectations for the user. For example, to let the user know that an agent will follow-up on their request, you would enter `An agent will reach out shortly`.

</td></tr><tr><td>

Resolution

</td><td>

resolution

</td><td>

Text that appears after the **More information** text. You can manually enter this content in a code editor, or you can populate the content dynamically by binding to a data resource. -   To manually enter the content, click **Edit**. In the code editor, enter a label-value pair. For example, to create content that reads `Estimated resolution in: 2 hours`, you would enter the following:

    ```
{
"label": "Estimated resolution in",
"value": "2 hours"
}
    ```

-   To dynamically populate the content, click the data icon \(\[Omitted image "data-icon.png"\] Alt text: Data icon\) and select a data resource.

</td></tr><tr><td>

Primary action label

</td><td>

primaryActionLabel

</td><td>

Label for the primary button.

</td></tr><tr><td>

Secondary action label

</td><td>

secondaryActionLabel

</td><td>

Label for the secondary button.

</td></tr></tbody>
</table>## Confirmation Message component events

Select event handlers to configure the actions \(events\) provided with the Confirmation Message component.

The Events tab shows the events used by the Confirmation Message component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Confirmation Message actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|NOW CONFIRMATION MESSAGE PRIMARY CLICKED|User clicks the primary action button.|
|NOW CONFIRMATION MESSAGE SECONDARY CLICKED|User clicks the secondary action button.|

