---
title: Responsive authoring
description: Use responsive authoring to create UI Builder pages that adjust smoothly to different form factors \(sizes\), such as desktop, tablet, and mobile.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Responsive authoring

Use responsive authoring to create UI Builder pages that adjust smoothly to different form factors \(sizes\), such as desktop, tablet, and mobile.

## Responsive authoring in UI Builder

Responsive authoring enables you to create pages that look good and function properly at any form factor, making it easier for people to interact with the content. For example, a page containing three columns when viewed on a laptop, can adjust to a single column for smaller screens.

UI Builder currently offers three default form factors:

-   Desktop \(1281 pixels to infinity\)
-   Tablet \(1280 pixels and smaller\)
-   Mobile \(500 pixels to zero\)

In addition to these form factors, you can create up to three additional custom breakpoints \(widths\). For more information, see [Create a breakpoint for responsive authoring](../task/responsive-authoring-create-breakpoint.md).

There are different techniques for editing pages so they're usable at different form factors. Use any of the following options:

-   [Show or hide components](../task/responsive-authoring-component-visibility.md)
-   [Change component configuration](../task/responsive-authoring-component-configuration.md)
-   [Edit styles](../task/responsive-authoring-adjust-styles.md)
-   [Rearrange the layout](../task/responsive-authoring-adjust-layout.md)

## Responsive authoring and reflow

As of Xanadu Store Release 1, responsive authoring is only available when creating UI Builder pages from scratch. Responsive authoring isn't available for existing pages or pages created with a template. These types of pages continue to use the existing, default reflow model to adjust pages for different screen widths.

Reflow transforms page layouts into a vertical, stacked view automatically without loss of content or functionality when users increase browser zoom to 400%. This adjustment helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations.

All existing pages that were created with templates or from scratch use reflow automatically. Now, when creating pages from scratch in UI Builder, an extra step shows you that responsive authoring is selected by default. You can choose to use reflow instead by selecting **Build without responsive**, however, using the responsive authoring option gives you more control over how pages work and look at different form factors. For more information about creating pages in UI Builder, see [Create a page in UI Builder](../task/create-page.md).

![New step showing responsive authoring and reflow options when creating a page from scratch.](../image/responsive-author-create-page.png)

For more information about reflow, see [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

For a list of UI Builder components that support reflow, see the **Support for reflow** section of the [Next Experience Components release notes](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/component-rn.html).

## Application and cascading of changes

All changes made to a form factor are applied to all smaller form factors automatically. For example, any changes made to tablet apply to both tablet and mobile. However, if you then make changes to the mobile form factor, it overrides the cascaded settings from the tablet form factor. This cascading functionality enables you to make specific changes for each smaller form factor so the page looks and functions well.

**Note:** Changes don't cascade up to larger sizes. For example, changes made to tablet aren't applied to the desktop.

## Responsive authoring and controllers

If you add a controller to a page, the controller properties are global and cannot be set per form factor. For more information about controllers, see [Bind data to UI Builder pages using controllers \(advanced feature\)](controllers.md#).

## Using responsive authoring as you create pages

As you build pages, create tailored designs to control the look and feel for different form factors.

By default on the stage, you build pages for the desktop \(1281 pixels to infinity\). At any time, select another icon to see the page on the stage at a different form factor, such as tablet or mobile. As needed, edit the page so it displays appropriately at the new form factor.

![Black arrow pointing to the form factor icons for desktop, tablet, and mobile at the top of a UI Builder page in editor view.](../image/responsive-author-icons.png)

Here's what a sample page looks like at the desktop form factor.

![Sample page displayed at 1304 pixels wide to represent a desktop or laptop screen.](../image/responsive-author-desktop-size.png)

Here's the same page customized for the tablet form factor.

![Sample page displayed at 900 pixels wide to represent a tablet.](../image/responsive-author-tablet-size.png)

For tablet, the heading and image components have been reduced in size. The simple list component configuration was edited to show four columns instead of six and the maximum number of rows was set to 5. When editing a component for a form factor, the fields that have changed are marked with a cascading icon for that form factor \(in this case, tablet\). The icon enables you to determine the differences between the form factors for a given page easily.

![Simple list component configuration panel with black arrows pointing to the tablet cascading responsive authoring icon next to two fields.](../image/responsive-author-config-pane-icon.png)

Here's the same page customized for the mobile form factor.

![Sample page displayed at 320 pixels wide to represent a mobile device.](../image/responsive-author-mobile-size.png)

The number of words in the heading was reduced and the image component was hidden. The simple list component configuration was edited to show two columns instead of four and the option to hide the "view all" footer option was selected. The two fields customized specifically for mobile have a mobile cascading icon next to them. The **Maximum rows** field still retains the tablet cascading icon because that field is inheriting the tablet setting and wasn't customized for mobile.

![Simple list component configuration panel with black arrows pointing to the two mobile and one tablet cascading icons next to fields.](../image/responsive-author-config-pane-icon2.png)

In addition to the default form factors in the editor view, at any time you can manually enter a number in the pixel field. The stage adjusts to the nearest form factor based on range. For example, entering 850 pixels adjusts the stage to the tablet form factor because its range is defined as 1280 to 501 pixels.

![Black arrows pointing to the tablet form factor icon and the pixel field.](../image/responsive-author-test-custom-breakpoint.png)

**Note:** Form factors and the ability to enter a pixel width are also available when previewing a page. For more information, see [Learn how to view and test your UI Builder experience](preview-page-ui-builder.md).

-   **[Adjusting component visibility in responsive authoring](../task/responsive-authoring-component-visibility.md)**  
When creating pages with responsive authoring for different form factors, learn how to show or hide components by completing steps to hide an image at mobile size.
-   **[Configuring components for responsive authoring](../task/responsive-authoring-component-configuration.md)**  
When creating pages with responsive authoring for different form factors, learn how adjusting some component configuration options can make pages look and work better at smaller sizes.
-   **[Adjust styles for responsive authoring](../task/responsive-authoring-adjust-styles.md)**  
When creating pages with responsive authoring for different form factors, learn how to change style options to increase the usability of the page at smaller sizes.
-   **[Adjust layout for responsive authoring](../task/responsive-authoring-adjust-layout.md)**  
When creating pages with responsive authoring for different form factors, learn how to adjust the layout to improve the look and feel of the page at smaller sizes.
-   **[Create a breakpoint for responsive authoring](../task/responsive-authoring-create-breakpoint.md)**  
Learn how to create custom breakpoints for responsive authoring to control the look and feel of a page at different form factors.

**Parent Topic:**[Manage UI Builder pages and page variants](work-pages.md)

