---
title: Learn how to view and test your UI Builder experience
description: Preview your experience in UI Builder to see how it looks and functions while building an experience. Previewing helps ensure that your experience works as expected, that the data resources are available, and that the layouts are set up correctly.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Learn how to view and test your UI Builder experience

Preview your experience in UI Builder to see how it looks and functions while building an experience. Previewing helps ensure that your experience works as expected, that the data resources are available, and that the layouts are set up correctly.

## Test your page

You can test your page as the developer or see it as it would appear to an end user. Previewing doesn't require saving first.

**Note:** Previewing inactive variants and page collections \(sub pages\) isn't currently supported.

You can test various aspects of your page.

-   Test the variant that you're currently working on, including modals, viewports, and dynamic data by selecting the **Preview** button, which opens an overlay.

-   Test with different data by changing the test values and selecting **Apply**. For more information, see [Test values in a page](test-value.md).

-   See what the variant looks like at different screen widths by selecting a form factor icon. For example, view the variant at tablet or mobile size. For more information about creating pages for different form factors, see [Responsive authoring](responsive-authoring.md).

    ![Preview pane with black arrow pointing to form factor icons.](../image/responsive-author-preview-icons.png)


**Note:** If you edit the test values or the form factor when previewing, the new test values or form factor are retained when you view the page variant in the editor. For example, if you changed the form factor to mobile while previewing, the page variant is displayed in the editor at the mobile form factor. You can always change to another size by selecting a form factor icon.

When you have finished testing, select the **X** in the upper right to close the overlay.

## Test your page as an end user

Test which variant users see by opening the URL path. Select the arrow next to the **Preview** button and in the drop-down list select **Open URL path**. UI Builder checks the audience, conditions, and condition order, and then opens the appropriate variant in a new browser tab. When you have finished testing, close the tab.

**Parent Topic:**[Manage UI Builder pages and page variants](work-pages.md)

