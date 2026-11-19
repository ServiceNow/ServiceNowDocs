---
title: Avatar component setup
description: The Avatar component provide a graphic representation of an identity, displayed as an image, text, or anonymous icon. You can associate an avatar to an identity. For example, you can add a user's avatar to a card to associate that card with the user it is assigned to.The Avatar component can be associated with an identity and represents a user by their initials, a profile image, or an anonymous icon. This component has been added to the UIB component drawer so it can be dragged onto the stage when you're building a page.The Avatar component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/avatar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Avatar component setup

The Avatar component provide a graphic representation of an identity, displayed as an image, text, or anonymous icon. You can associate an avatar to an identity. For example, you can add a user's avatar to a card to associate that card with the user it is assigned to.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Avatar that differentiates it from other components in the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "avatar-content-tree.png"\] Alt text: Avatar UI component content tree

2.  Select the Avatar component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Avatar label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Avatar component properties

The Avatar component can be associated with an identity and represents a user by their initials, a profile image, or an anonymous icon. This component has been added to the UIB component drawer so it can be dragged onto the stage when you're building a page.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_tsr_g5y_znb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

​Size of the avatar: extra small, small, medium, large, or extra large

</td></tr><tr><td>

User name​\[userName\]

</td><td>

Name of user. If no **imageSrc** is provided, initials of first two names in string appear in avatar. Name is also read aloud to screen reader users. If no name is provided, screen reader announces avatar user as "unknown user.”

</td></tr><tr><td>

Presence\[presence\]

</td><td>

​Presence icon to show the online status of a user that always appears in the lower right of the avatar

</td></tr><tr><td>

Show presence pattern\[showPresencePattern\]

​

</td><td>

Enables a visual pattern enabled on presence icon for accessibility.

</td></tr><tr><td>

Image source\[imageSrc\]

​

</td><td>

Location of user image to display in the avatar.

</td></tr><tr><td>

Interaction\[interaction\]

</td><td>

Defines the interaction behavior of the avatar.Available options include:

-   `None`
-   `Button`
-   `Link`

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**.

</td></tr><tr><td>

Tooltip text\[tooltipContent\]

</td><td>

Content to display in a tooltip for the avatar. This text appears when hovering on the avatar.

</td></tr><tr><td>

Hide tooltip​\[hideTooltip\]

</td><td>

Suppresses tooltip when hovering on user name.

</td></tr></tbody>
</table>## Avatar component events

The Avatar component doesn't have configurable events.

