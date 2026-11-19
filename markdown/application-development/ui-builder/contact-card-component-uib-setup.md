---
title: Contact card component setup
description: The Contact card component provides information about customers who have contacted the contact center for help​.Configure the content of your Contact card with these properties.Select an event handler to configure the action \(event\) provided with the Contact card component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/contact-card-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Contact card component setup

The Contact card component provides information about customers who have contacted the contact center for help​.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Contact card that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "contact-card-content-tree.png"\] Alt text: Contact card component with label displayed in the content tree.

2.  Select the Contact card component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Contact card label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Contact card component properties

Configure the content of your Contact card with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_pyg_mhf_b4b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Avatar URL\[avatarSrc\]

</td><td>

Location of the user image to display in the avatar. Leaving this empty displays the initials of the customer.​

</td></tr><tr><td>

Heading name\[headingName\]

</td><td>

The display name of the contact.

</td></tr><tr><td>

Heading level​\[headingLevel\]

</td><td>

Maximum number of lines to display the heading name and badges. This is useful when the card width needs to be narrow.​ This HTML heading element number can be one of \[1, 2, 3, 4, 5, 6\].

</td></tr><tr><td>

Heading badges​\[headingBadges\]

</td><td>

Critical information about the customer that is displayed with different background colors. ​

</td></tr><tr><td>

Subheading titles​\[subHeadingTitles\]

</td><td>

Titles to show for the contact. Supports multiple titles.

</td></tr><tr><td>

Subheading badges​\[subHeadingBadges\]

</td><td>

Critical information about the customer that needs to be displayed with different background colors alongside the sub-header.​ Supports multiple badges.

</td></tr><tr><td>

Contact fields\[content\]

</td><td>

List of fields for all information about the customer that would be useful to the agent to reference to get to know the customer associated to the case or interaction.

</td></tr><tr><td>

Hide border​\[hideBorder\]

</td><td>

Boolean value indicating whether to show or hide the border around the card.​

</td></tr><tr><td>

ARIA label\[ariaLabel\]

</td><td>

Forces screen readers to read this label before beginning to read the text inside the card.

</td></tr></tbody>
</table>## Contact card component events

Select an event handler to configure the action \(event\) provided with the Contact card component.

The Events tab shows the events used by the Contact card component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Contact card actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Item clicked|Dispatched when the user clicks a clickable item on the card.|

