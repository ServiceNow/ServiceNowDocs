---
title: Editing source code in the Rich Content Editor
description: Modify the HTML and CSS source code for all the elements in the canvas or for a specific element.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsites, Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Editing source code in the Rich Content Editor

Modify the HTML and CSS source code for all the elements in the canvas or for a specific element.

Build the layout using HTML elements, directly edit the CSS for an element to add styling that isn't otherwise available in the canvas interface, or copy-paste code to migrate content from other sources.![Add a border around a row and customize the header font](../images/rce-code-editor.png)

## Features and capabilities

-   **Ensure portal security**

    When you click **Apply** in the Edit code window, the code editor removes HTML tags that could be used to compromise your instance. For more information, see HTML sanitizer.

-   **Identify important code**

    The editing window highlights CSS fragments in red if they should not be deleted. This indicates either a setting that is part of the portal theme or that multiple elements use that code.

    Additionally, if you delete a CSS rule that is referenced by one of the following HTML elements, the code editor reinstates the CSS rule:

    -   Row
    -   Cell
    -   Canvas
    -   Divider
    -   Button
    -   Link block
    -   Tabs
-   **Remove unnecessary code**

    When you save your changes, the code editor removes any unused CSS rules.

    Conversely, if the code editor reinstates a CSS rule that you are trying to remove, highlight that block of CSS code and click the **Remove CSS** button to override the code editor.

    In the following video, the user tries to delete a CSS rule using the delete key, but the system reinstates the code. Next the user highlights the code and clicks **Remove CSS**, which successfully removes the code.

    ![User unsuccessfully tries to delete a CSS rule using the delete key, so they use the Remove CSS button, which removes the highlighted code](../images/rce-remove-css.gif "Example of using the Remove CSS button")


**Note:** This feature is not available by default. An Admin must enable the **Edit code** property. See [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md)

## Important considerations

-   Adding custom HTML and CSS can break your design. Proceed with caution when using this feature. The Rich Content Editor does not track changes in the code editor, so the **Undo** button will not reliably revert the code changes.
-   We do not recommend using HTML elements \(such as div or p\) to define CSS rules, as that can have unintended consequences.

    In the following example, the user defines a CSS rule for the p element in a cell. However, in the page preview, the style rules apply to the p elements in all the text boxes, as well as in the footer.

    ![User defines a CSS rule using the HTML p element for a cell but the rule is applied throughout the page](../images/rce-dont-do-this.gif "Example of an unexpected outcome when using HTML element to define CSS rule")

-   Different browsers may exhibit varying copy/paste behaviours. If pressing Ctrl+V does not duplicate the content as expected, click the duplicate icon in the component toolbar.
-   If copy-pasted content does not retain its styling \(such as font\), and adjusting the settings does not help, clear the styling by clicking the “x" next to the styling field, then set the styling.![Remove the custom styling by clicking the "x" next to the styling field](../images/rce-fix-styling.png)
-   If pasted content appears differently saving, it likely due to some script tags being removed by the HTML sanitizer.

