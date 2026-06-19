---
title: Change the default appearance of components
description: Set the styles for components and wrappers to change the default appearance.Set CSS styles for a component to change its default appearance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/add-styling-to-component.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Change the default appearance of components

Set the styles for components and wrappers to change the default appearance.

This video shows you how to perform the following procedure.

## Before you begin

Role required: ui\_builder\_admin

## About this task

This task describes how to add styles to components and the wrappers \(such as Body, column layouts, or a column\) containing components. Customize component styling by selecting the component in the Content tree or apply styles to multiple components by placing components inside a wrapper.

For information about adding styling to your entire experience, see [Manage the visual style of UI Builder experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/manage-the-visual-style-of-ui-builder-experiences.md).

This task applies to the new layout system introduced in Australia. If your page is using the old layout system, see [Add styling to a component using the old layout system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-styling-to-component.md) for more information.

**Note:** As you add and configure components on the page, the stage shows your work. If you make changes and the updates do not load on the stage, select the **Open menu** icon and then select **Developer &gt; Reload Stage**. Reloading the stage shows your changes, but does not save them. To save your work, select **Save** at the top right.

\[Omitted image "force-stage-reload.png"\] Alt text: Experience view with Open menu selected showing the Developer and Reload Stage options.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

4.  In the Content panel, select a component or wrapper \(for example, Body, a column layout, or a column\) for which you want to add styling.

5.  For Body or a component, select the **Styles** tab in the configuration panel.

    \[Omitted image "styles-tab.png"\] Alt text: Configuration panel Styles tab.

6.  Use the visual representations on the **Styles** tab to decide what is best for the look and feel of your page.

    -   **Accessibility \(Column layout and Column\)**

        Specifies accessibility settings such as ARIA Region Name, ARIA Region Heading Level, ARIA Role, and inclusion of ARIA Heading. For detailed information, see the ARIA documentation on [developer.servicenow.com](https://developer.servicenow.com/dev.do#!/reference/next-experience/utah/ui-framework/advanced/accessibility).

    -   **Alignment \(Column and Component\)**

        For a column, defines how components align within the column as a group. For a component, defines how the component aligns within the parent layout element, such as a column or column layout.

    -   **Background \(Body, Column layout, Column, and Component\)**

        Sets the background color behind the layout element. Select a color from the color picker **My Colors** tab where you can view available colors in a grid or a list. Alternatively, use the **Custom** tab to specify any color in HEX, RGB, or HSL.

        \[Omitted image "styles-tab-background.png"\] Alt text: Background color options on the List tab.

    -   **Border \(Column layout, Column, and Component\)**

        Adds a border around the content. The border is placed on the immediate inside of the margin and the immediate outside of the padding. Specify the border thickness, type, color, and corner shape. For components, you have the option to use custom CSS for the border.

        \[Omitted image "styles-tab-border.png"\] Alt text: Border option expanded showing Thickness, Type, Color, and Corner shape options.

    -   **Layout \(Body, Column layout, Column, and Component\)**

        For body and column, specifies direction, alignment, and content justification. For column layout, specifies the number of columns and the column gap \(space between columns\). For some components, such as Card Base Container, select **Edit CSS** to apply specific CSS styles to the container layer and to the internal layer controlling components within the container.

        \[Omitted image "css-styles-edit.png"\] Alt text: Edit CSS styles modal with style options for containers and layout styles for components inside container.

    -   **Shadow \(Column layout, Column, and Component\)**

        Adds shadow effects around the content. You have the option to use custom CSS.

    -   **Sizing \(Component\)**

        For applicable components, sets the default, minimum, and maximum height and width for the component \(in px, %, em, rem, or a custom value\). This value is relevant for when the browser window is resized.

        \[Omitted image "styles-tab-sizing.png"\] Alt text: Sizing option expanded showing width and height options.

    -   **Spacing \(Body, Column layout, and Component\)**

        Margin sets the size of the space on the immediate inside of the body, column layout, or component. Padding sets the size of the space on the immediate outside of the body, column layout, or component. Select Margin or Padding to set the same size for all four sides.

        \[Omitted image "styles-tab-spacing.png"\] Alt text: Margin and padding spacing options.

        You can set the size for each margin or padding side by selecting the current setting and then selecting an option.

        \[Omitted image "spacing-margin-padding-video.gif"\] Alt text: Spacing option with margin and padding settings for all four sides of body, column layout, or component.

7.  For Body and components, you can edit the CSS code by selecting the **View and edit CSS** link at the bottom of the **Styles** tab.

    The **Styles tab** displays a **CSS styles** code editor. The following CSS properties are the most commonly used:

    -   `background-color`
    -   `background-image`
    -   `border-style`
    -   `border-width`
    -   `border-color`
    -   `border-radius`
    -   `box-shadow`
    -   `height`
    -   `min-height`
    -   `max-height`
    -   `margin`
    -   `overflow`
    -   `padding`
    -   `width`
    -   `min-width`
    -   `max-width`
    -   `z-index`
    \[Omitted image "uib-css-code-editor.png"\] Alt text: CSS styles code editor.

    **Important:** Some components contain built-in styling configurations that you can't override with CSS in UI Builder. For information about overriding these style configurations, see [Manage the visual style of UI Builder experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/manage-the-visual-style-of-ui-builder-experiences.md).

8.  In the main header, select **Save** to save your changes.


**Parent Topic:**[Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-components.md)

## Add styling to a component using the old layout system

Set CSS styles for a component to change its default appearance.

### Before you begin

Role required: ui\_builder\_admin

### About this task

This task describes how to add styles to the wrapper containing your component, which is generally recommended instead of applying styles to the component directly. Make sure that the component whose styles that you want to define is placed within a container component to put the component in a wrapper. Your component's wrapper is one level higher than the component in the Content hierarchy and is labeled by default as `Main`.

To add styling to an entire page, you can use standards-based CSS in the wrapper for the page. For information about adding styling to your entire experience, see [Manage the visual style of UI Builder experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/manage-the-visual-style-of-ui-builder-experiences.md).

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

    **Note:** A component must be placed in a container before adding styles to the component.

4.  Select the container holding the component you want to add styling to.

    The container is typically one level higher than the component in the content tree.

    The Styles tab appears in the configuration panel.

5.  In the CSS Styles window, enter standards-based CSS properties and values.

    The following CSS properties are the most commonly used to apply styles for components within containers:

    -   `background-color`
    -   `background-image`
    -   `border-style`
    -   `border-width`
    -   `border-color`
    -   `border-radius`
    -   `box-shadow`
    -   `height`
    -   `min-height`
    -   `max-height`
    -   `margin`
    -   `overflow`
    -   `padding`
    -   `width`
    -   `min-width`
    -   `max-width`
    -   `z-index`
    **Important:** Some components contain built-in styling configurations that you cannot override with CSS in UI Builder. For information about overriding these style configurations, see [Manage the visual style of UI Builder experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/manage-the-visual-style-of-ui-builder-experiences.md).

6.  In the main header, select **Save** to save your changes.

    \[Omitted image "add-styling-to-component-demo.gif"\] Alt text: Styles tab CSS styles option that can be used to add styling to the body or a component using standards-based CSS.


