---
title: Copy and Paste in the Rich Content Editor
description: Copy and paste HTML and CSS source code for elements in the canvas.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsites, Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Copy and Paste in the Rich Content Editor

Copy and paste HTML and CSS source code for elements in the canvas.

Directly [edit the CSS](rce-editing-source-code.md) for an element to add styling, or copy-paste code to migrate content from other sources.

**Important:** For the May 2025 release, if any pasted content has a **background-color**, the right-hand panel will not display the color unless it is formatted with **background-image styling**. The background acts as layers to add **background-color**, **gradient**, and **image** to your content. The edit code feature can be used to adjust the pasted styling from **background-color** to the corresponding value for **background-image CSS**, if you want the color to be displayed on the right-hand panel.

**Tip:** Color opacity functionality is a new feature and isn't supported in any prior release.

## Limitations

-   Browsers might display different copy-paste behaviors due to browser functional differences.
-   Copying a component on canvas doesn’t duplicate as expected on ctrl+v, so you must access the **component toolbar**.


![Provides additional selections from the Component Toolbar](../images/rce-cp-limitation-toolbar.jpg "Component Toolbar")

**Note:** You can also add color opacity to the canvas. However, one of the limitations is that copy/paste won't transfer all styling when the colors are formatted in **rgba\(\)**instead of **rgb** or **hex**.

-   Pasting highlighted text isn’t supported within text components, so behaviors that work in Chrome might not work in Firefox or Safari.

-   We recommend adding colors of pasted content in **hex code** format \(**\#rrggbbaa** to add opacity, or you can use **\#rrggbb**\).

    -   The hash-tag \(\#\) is required.
    -   Hex codes start with a pound sign or hash-tag \(\#\) followed by 6 letters if there is no color opacity, or 8 letters if there is color opacity.
    -   The 8-character syntax only works if it is added to the element CSS through the edit-code feature. The color input field on the right-hand panel only accepts 6-character syntax.
-   You can also open the edit code modal to adjust the **rgba\(\)** colors of the component to hex code to reflect the styling.

If certain styling isn’t applied \(for example Font name\) or adjusting any of the settings for the pasted content doesn’t work, try to clear the styling first by selecting the “**x**" next to **Font name**.

![Allows you to adjust font settings](../images/rce-cp-limitation-fontname.jpg "Font name")

-   If your pasted content doesn’t display as expected or behaves incorrectly, try to copy a smaller chunk instead of a big section at once.
-   • If your pasted content is displayed differently before and after saving and reloading, it might be due to some script tags removed by the HTML sanitizer.

## Deselected Areas

-   If you select the **Pink** areas, it deselects any component that is selected on the canvas.

-   If you select the **Green** areas, it keeps the current component selected.


![Allows you to determine action based on color background selected](../images/rce-cp-limitation-canvascolor.jpg "Rich Content Editor Canvas")

**Note:** Cutting and pasting highlighted text isn’t supported within text components and experiences across browsers might behave differently. Behaviors that work in Chrome might not work in Firefox or Safari.

## Additional Rich Content Actions and Behaviors

**Note:** Content Managers and Admins have the option to apply background colors to selected canvas elements, including images. Available features include the use of solid and gradient colors, as well as adjustments for color opacity. These settings can be accessed in the right-hand panel under the Settings Styling tab when adding rich content to a canvas element.

The ability to add color opacity to the canvas is a useful function available to you. The only limitation is that the copy and paste function styling is different when the colors are formatted in rgba\(\) instead of rgb, or hex.

-   Add colors in hex code format \(`#rrggbbaa` to add opacity or just `#rrggbb`\).
-   Open the edit code modal to adjust the rgba\(\) colors of the component to hex code to reflect the styling.
-   Color Opacity shows the gradient and color layer options. Since background image layer is first, opacity isn’t relevant. Gradient is FFFFFF and OOOOOO by default.
-   Background color to canvas element shows the background options for gradient, color and image. Toggle on and then select background options.


**Note:** Content is pasted at the end of the canvas when no component is selected.

-   If a component is selected, content pastes underneath it.
-   If a component is being edited, the following paste behavior occurs:
    -   If the source is plain text, the content pastes into the current component, and matches the pasted text to the destination styling.
    -   If the source is formatted, it’s appended under the most current component.
    -   If the component enables nested components \(for example Tab, Accordion, or Row\), then content is appended within the parent container.
-   If components are deselected when selected out of the canvas, it enables paste with source formatting.

For more information on editing source code, see [Editing source code in the Rich Content Editor](rce-editing-source-code.md)

