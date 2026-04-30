---
title: Using Flexbox layouts in UI Builder
description: Create a Flexbox layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.Create a Flexbox layout in UI Builder to build powerful pages in a low-code environment.Create a Flexbox layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Organize components in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Using Flexbox layouts in UI Builder

Create a Flexbox layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.

You can easily build custom pages with Flexbox layouts in UI Builder. Customizing the layout of your page lets you take full advantage of Flexbox so that you can achieve your overall page design. For more information, see [Organize components in UI Builder pages](work-layouts.md).

Flexbox is a one-dimensional layout system in CSS. Flexbox is inherently flexible, which is useful for when you don’t know the size of your content. If you plan to build complex pages, you can customize the layout of your page in the configuration panel styles tab or with CSS. Visit [Mozilla](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) to learn more about Flexbox.

You can change the direction of your content in the layout in the following ways:

-   Row: Rows are organized left-to-right or right-to-left, depending on the direction of your browser's default language. Left/right is the case for an English browser.
-   Row-reverse: Rows are organized in the reverse direction of your browser's default language, such as right-to-left or left-to-right.
-   Column: Up/down or down/up
-   Column-reverse: Down/up

    ![Diagram showing Flexbox row and column directions.](../image/UIB-flexbox.png "Flexbox row and column directions")

-   Justify content: Defines the alignment along the main axis. Choices are as follows:
    -   Flex-start: Items are at the start of the flex direction, similar to left-justified content. This is the default setting.
    -   Flex-end: Items are at the end of the flex direction, similar to right-justified content.
    -   Space-between: Items are distributed evenly.
    -   Space-around: Items are distributed evenly with equal space around them.
    -   Space-evenly: The spacing between items is equal.
-   Align items: Defines how you want your flex content displayed along the cross axis. Choices are as follows:
    -   Stretch: Stretch your content to fill the container. This is the default setting
    -   Flex-start: Place your content at the start of the cross axis.
    -   Flex-end: Place your content at the end of the cross axis.
    -   Center: Center your content in the cross axis.
    -   Base system: Align your content the same as your baseline alignment.
-   Height: Set the height automatically or manually.
-   Width: Set the height of your flexbox items automatically or manually.
-   Margin: Set your minimal distance between flexbox items.
-   Padding: Set the padding for each side of your flexbox items.

**Parent Topic:**[Organize components in UI Builder pages](work-layouts.md)

## Create a Flexbox layout with the new layout system

Create a Flexbox layout in UI Builder to build powerful pages in a low-code environment.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md).

4.  Select the **+ Add content** button in the UI Builder stage.

5.  Select **Flexbox** in the layouts tab.

    ![Arrow pointing to the Flexbox option on the layouts tab of the toolbox.](../image/flexbox-select-toolbox.png)

6.  Select **Add**.

7.  Select the **Styles** tab in the configuration panel.

8.  In the **Layout** section, you should see **Flexbox** highlighted.

    ![Arrow pointing to the Flexbox option on the configuration panel styles tab.](../image/flexbox-highlighted.png)

9.  In the **Layout** section of the styles tab, you can change the following:

    -   **Direction**

        Define how you want components to stack, horizontally or vertically.

    -   **Align Items**

        Define how components within containers align as a group.

    -   **Justify content**

        Define how to pack or space apart the components within the container.

        **Note:** Select **Show advanced layout options** to see the next two options.

    -   **Gap**

        Set the size of the gap between rows and columns.

    -   **Wrap child elements to multiple lines**

        Set whether components are forced onto one line or overflow onto multiple lines.

    Visit [Mozilla](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) to learn more about Flexbox layout configurations.

10. You can edit the CSS code by selecting **Show advanced configuration options** at the bottom of the **Styles** tab, and then selecting the **View and edit CSS** option.

11. Select **Save**.

    Your page refreshes and displays the changes made to the layout.

12. Add components to your page.

    See [Add and configure components](../task/add-components.md#) for more information.

13. View and test your page by selecting ![Preview button that opens the page variant.](../image/preview-button.png).


## Create a Flexbox layout with the old layout system

Create a Flexbox layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.

### Before you begin

Role required: admin

### About this task

In the following procedure, you learn how to use Flexbox to change the CSS code to customize the layout of your page.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md) or open a page.

4.  Click the **Layout** tab and choose the two-column layout.

    ![Standard two-column-layout.](../image/UIB-layouts-flexbox-two-row.png "Standard two-column-layout")

5.  Click **Edit layout code**.

    ![Edit the layout code.](../image/UIB-layouts-context-menu.png "Edit the layout code")

6.  Expand the code editor so that you can easily view the CSS code.

    ![Arrow pointing to expand the code editor button.](../image/UIB-layouts-flexbox-expand.png "Expand the code editor")

7.  Add another slot to the layout by copying the CSS code for an existing slot.

    Copying the code is easier than typing it into the layout.

    ![Arrow pointing to copy the CSS code for a slot.](../image/UIB-layouts-flexbox-copy-css.png "Copy the CSS code for a slot")

8.  Below the code that you copied, place a comma and then paste the following CSS code:

    1.  Change the **"slotName"** property to `"Column 3",`.

    2.  Change the **"flex"** property to `"2"`.

    3.  Add `"margin-left": "1rem"`.

    ![Pasting the CSS code.](../image/UIB-layouts-flexbox-paste-css.png "Paste the CSS code")

    Changing the **"flex"** property increases the size of the column. By using **"margin-left"**, you add space between the previous columns.

9.  Collapse the expanded view, and then click **Apply**.

    ![Applying a layout change.](../image/UIB-layouts-flexbox-apply.png "Apply a layout change")


### Result

The new Flexbox layout that you created shows the new slot that you added to the original two-column layout.

![New, finished custom layout.](../image/UIB-layouts-flexbox-final-layout.png "New custom layout")

Click **Reset to original** to reset layout changes back to the original.

![Arrow pointing to reset to original option.](../image/UIB-layouts-reset-to-original.png "Reset a layout")

**Related topics**  


[Create a CSS Grid layout with the old layout system](css-grid-uib.md#)

