---
title: Carousel component setup
description: The Carousel component shows a horizontal ribbon of other components that users cycle through. Select the components for the Carousel and set how to display them.Configure how Carousel moves the components and the placement of the navigation controls with these properties. Also configure header title and links.Select event handlers to configure the actions \(events\) provided with the Carousel component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/carousel-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Carousel component setup

The Carousel component shows a horizontal ribbon of other components that users cycle through. Select the components for the Carousel and set how to display them.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Carousel that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Add one or more components to the content slot for the Carousel to display.

    You can put any component into the Carousel, but be aware of the styling when doing so. Each top level component is considered a single component. For example, if you add a container with multiple components, the Carousel treats the container as the main component.

    **Tip:** Consider using a Carousel inside a Repeater. In this case, do not enable any styling on the Repeater component. Accept its default settings. For more information, see [Add repeaters in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/repeaters.md).

    In this example, Carousel 4 has a container with a Heading and a Button.

    \[Omitted image "carousel-content-tree.png"\] Alt text: Content tree for 4 Carousel components.

    The Heading and the Button are shown together in a single component.

    \[Omitted image "carousel-container-heading-button.png"\] Alt text: Container with heading and button in Carousel, shown in runtime


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Carousel component properties

Configure how Carousel moves the components and the placement of the navigation controls with these properties. Also configure header title and links.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Title properties

Set the text to display in the Carousel title.

<table id="table_iq4_rcz_bsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide title\[hideTitle\]

</td><td>

When **true**, the title is hidden. If **hideTitle** and **hideLink**are **true**, the header is hidden.Default: **false**

</td></tr><tr><td>

Title\[carouselTitle\]

</td><td>

Text that displays in the header.Default: **Title**

</td></tr><tr><td>

Title level\[titleLevel\]

</td><td>

Defines which HTML heading level element `<h#>` renders the title.Default: **2**

</td></tr><tr><td>

Badge configuration\[badgeConfig\]

</td><td>

Customizable badge that appears as a background color to the badge **label**. Badge is located to the right of the **title**.Properties are:

-   **label**: A string that sets the text of the badge.
-   **color**: The badge color.

Choices are:

    -   critical
    -   high
    -   warning
    -   moderate
    -   positive
    -   info
    -   low
    -   magenta
    -   pink
    -   orange
    -   yellow
    -   brown
    -   green
    -   green-yellow
    -   blue
    -   gray
    -   teal
    -   purple
-   **variant**: A string that sets the style variant of the badge.

Choices are:

    -   primary
    -   secondary
    -   tertiary

Default: **label** is empty, **color** is **low**, and **variant** is **tertiary**

</td></tr><tr><td>

Title style variant\[titleVariant\]

</td><td>

Defines the styles used to render the title, based on the Heading component.Default: **header-tertiary**

</td></tr><tr><td>

Title location\[titlePosition\]

</td><td>

Sets the position of the title, which can be left-aligned or right-aligned.Default: **left**

</td></tr><tr><td>

Disable text wrapping\[disableTextWrapping\]

</td><td>

If set to **true**, disables title text from wrapping and truncates the title instead.Default: **false**

</td></tr></tbody>
</table>### View all link properties

Set the appearance of link on the top-right corner of the header. This link dispatches the **Link clicked** action.

<table id="table_jzl_x2z_bsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide view all link\[hideLinkhideLink\]

</td><td>

When **true**, the link is hidden. If **hideTitle** and **hideLink** are **true**, the header is hidden.Default: **false**

</td></tr><tr><td>

Link icon\[linkIcon\]

</td><td>

Defines the icon to use for the link text.Default: **Arrow Right Fill**

</td></tr><tr><td>

Link text\[linkText\]

</td><td>

Text describing the link.Default: **View all**

</td></tr></tbody>
</table>### Navigation and interaction properties

Define how Carousel moves the components and the placement of the navigation controls.

<table id="table_w4h_bfz_bsb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of items in view\[itemsInView\]

</td><td>

Select whether Carousel shows a horizontal ribbon of multiple items or only a single item at a time.Default: **Multiple content items**

</td></tr><tr><td>

Sliding type\[slidingType\]

</td><td>

Determines whether a user can move a set of items along the ribbon at once or only one at a time. Available only when `itemsInView` is set to multiple-content-items.Default: **Slide next set of items**

</td></tr><tr><td>

Auto scroll speed\[autoScrollSpeed\]

</td><td>

Carousel content auto scroll speed interval.

</td></tr><tr><td>

Pause auto scroll\[pauseAutoScroll\]

</td><td>

Pauses Carousel content auto scroll when enabled.

</td></tr><tr><td>

Disable looping\[disableLooping\]

</td><td>

When **true**, the left arrow on the first slide and the right arrow on the last slide don't appear. The user can't scroll backwards from the first component to the last components, or forwards from the last component to the first components.Default: **false**

</td></tr><tr><td>

Left and right navigation controls location\[navPosition\]

</td><td>

The location of the navigation controls on Carousel. Choices are:

-   center
-   bottom-left
-   bottom-right
-   bottom-split

Default: **center**

</td></tr><tr><td>

Navigation control gradient color\[gradientStyle\]

</td><td>

The color of the gradient surrounding the navigation controls.Choices are:

-   primary
-   secondary
-   tertiary
-   dark
-   none

 Default: **primary**

</td></tr><tr><td>

Navigation control style\[navStyle\]

</td><td>

Specifies whether your navigation icons are filled or outlined.Default: **fill**

</td></tr><tr><td>

Enable advanced navigation button configuration\[enableAdvancedNavConfig\]

</td><td>

Determines whether or not the navigation control configuration is shown and used. Determines whether the **navButton** is styled by the existing **navStyles** property or by the **navButtonConfig**, **leftNavButtonIcon**, and **rightNavButtonIcon** properties. When true, enables advanced configuration of the navigation control buttons.Default: **false**

</td></tr><tr><td>

Left navigation button icon\[leftNavButtonIcon\]

</td><td>

When the advanced navigation button property is enabled, you can set the icons for the left/right navigation buttons. This property defines the icon for the left Iconic button navigation control.Default: **circle-chevron-start**

</td></tr><tr><td>

Right navigation button icon\[rightNavButtonIcon\]

</td><td>

When the advanced navigation button property is enabled, you can set the icons for the left/right navigation buttons. This property defines the icon for the right Iconic button navigation control.Default: **circle-chevron-end**

</td></tr><tr><td>

Navigation control configuration\[navButtonConfig\]

</td><td>

Configurable JSON that determines the styling for the navigation buttons. This property only displays when the advanced navigation button property is enabled.Default: `"{"size": "lg", "hide-padding": "true", "bare": "true"}"`

</td></tr><tr><td>

Hide dot indicator\[hideDotIndicator\]

</td><td>

When **true**, the dot indicators under the Carousel ribbon are hidden. These dots indicate which set of components along the ribbon the user is viewing. The user can select a dot to move to that set of components.\[Omitted image "carousel-dot-indicators.png"\] Alt text: Carousel dot indicators.

 Default: **false**

</td></tr><tr><td>

View index\[startingIndex\]

</td><td>

Starts Carousel at the given index position along the components.Default: **0**

</td></tr></tbody>
</table>### Empty state properties

Define what to show when Carousel is empty.

<table id="table_emj_dfz_bsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Empty state heading\[emptyStateLabel\]

</td><td>

Heading displayed when Carousel is empty.Default: **No content to display**

</td></tr><tr><td>

Empty state message\[emptyStateContent\]

</td><td>

The message displayed when Carousel is empty.Default: **Please add components into the carousel**

</td></tr><tr><td>

Empty state illustration\[emptyStateIllustration\]

</td><td>

Illustration shown when Carousel is empty.Type: choice

 Default: **Completed-tasks**

</td></tr></tbody>
</table>## Carousel component events

Select event handlers to configure the actions \(events\) provided with the Carousel component.

The Events tab shows the events used by the Carousel component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Carousel actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Link clicked|The user clicks the View All link. This event doesn't have a set payload. Handler and payload depend on what you want to happen when View All is clicked, which in turn depends on the components in Carousel.|
|Index updated|The user performs a navigation action to change which components are in focus. The payload is the new `indicator` number. You don't need to configure an event handler for navigation to work. Add an event handler only if you want some action other than the default navigation action to occur.|

