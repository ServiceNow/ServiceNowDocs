---
title: Using CSS Grid layouts to build a page
description: Create a CSS Grid layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.Create a CSS Grid layout in UI Builder to build powerful pages in a low-code environment.Create a CSS Grid layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Organize components in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Using CSS Grid layouts to build a page

Create a CSS Grid layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.

CSS Grid is the most powerful layout system in CSS. CSS Grid is built on top of a two-dimensional grid. CSS Grid gives you control over how you create your pages. Use UI Builder to implement a CSS Grid layout using low-code layout configuration properties. For advanced layouts, you can view and edit CSS code to customize your layouts. Visit [Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/grid) to learn more about CSS Grid.

For example, you can have a grid with three columns and three rows to make a grid nine cells. You can place components inside these cells or make the component span multiple cells.

![CSS Grid layout](../image/UIB-layout-css-grid.png "CSS Grid layout")

Customizing the layout of your page lets you take full advantage of CSS Grid so that you can achieve your overall page design. For more information, see [Organize components in UI Builder pages](work-layouts.md).

To find out more about CSS layouts within your UI Builder instance, you can find them in the \[sys\_uib\_template\] table.

**Parent Topic:**[Organize components in UI Builder pages](work-layouts.md)

## Create a CSS Grid layout with the new layout system

Create a CSS Grid layout in UI Builder to build powerful pages in a low-code environment.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md).

4.  Select the **+ Add content** button in the UI Builder stage.

5.  Select **Grid** in the layouts tab.

    ![Arrow pointing to the Grid option in the layouts tab of the toolbox.](../image/grid-select-toolbox.png)

6.  Select the **Styles** tab in the configuration panel.

7.  In the **Layout** section, you should see **Grid** highlighted.

    ![Arrow pointing to the Grid option in the configuration panel styles tab.](../image/grid-highlighted.png)

8.  In the **Layout** section of the styles tab, you can change the following:

    -   **Columns**

        Defines the number, order, and width of grid columns.

    -   **Rows**

        Defines the number, order, and width of grid rows.

    -   **Direction**

        Sets whether newly added components are stacked horizontally or vertically.

    -   **Gap**

        Sets the size of the gap between rows and columns.

        **Note:** Select **Show advanced layout options** to see the next four options.

    -   **Align items**

        Defines how components within the container align as a group.

    -   **Justify items**

        Defines how the browser distributes space between and around content items along the inline axis of a grid container.

    -   **Align content**

        Sets the distribution of space between and around content items along a grid's block axis.

    -   **Justify content**

        Defines how to pack or space apart the components within the container.

    Visit [Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) to learn more about CSS Grid layout configurations.

9.  You can edit the CSS code by selecting **Show advanced configuration options** at the bottom of the **Styles** tab, and then selecting the **View and edit CSS** option.

10. Select **Save**.

    Your page refreshes and displays the changes made to the layout.

11. Add components to your page.

    See [Add and configure components](../task/add-components.md#) for more information.

12. View and test your page by selecting ![Preview button that opens the page variant.](../image/preview-button.png).


## Create a CSS Grid layout with the old layout system

Create a CSS Grid layout in UI Builder to build powerful pages so that you can customize with cascading style sheets \(CSS\) and can improve your performance.

### Before you begin

Role required: admin

### About this task

In the following procedure, you learn how to use CSS Grid to modify your CSS to customize the layout of your page.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md) or open a page.

4.  Click the **Layout** tab and choose the two-row by two-column layout.

    ![Standard two row, two-column layout.](../image/UIB-layouts-custom-four-standard.png "Standard two-row, two-column layout")

5.  Click **Edit layout code**.

    ![Edit layout code option.](../image/UIB-layouts-context-menu.png "Edit the layout code")

6.  Expand the code editor so that you can easily view the CSS code.

    ![Arrow pointing to the expand the code editor button.](../image/UIB-layouts-expand-edit-layout.png "Expand the code editor")

7.  Add another slot to the layout by copying the CSS code for an existing slot.

    Copying the CSS code is easier than typing it into the layout.

    ![Arrow pointing to copying the CSS code for a slot.](../image/UIB-layouts-copy-css-block.png "Copy the CSS code for a slot")

8.  Paste the CSS code below the code that you copied and change the **slotName** and **grid-area** to a unique value.

    ![Pasting the CSS code.](../image/UIB-layouts-paste-css-block.png "Paste the CSS code")

9.  Modify the layout rules to include the new column and template area, as follows:

    1.  Delete the `"Grid-template-columns": "1fr 1fr",` line.

    2.  Add a second `cell1` after `cell1`, and then add `cell5` after `cell4`.

    ![Modifying the layout rules.](../image/UIB-layouts-modifyCSS.png "Modify the layout rules")

    You can set many different configurations. In this example, there are the two resulting grids from two different grid template areas. The **"grid-template-areas"** property being modified is setting the CSS property of the same name. For more information, see [MDN grid-templates-areas](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-areas).

    ![Grid template areas.](../image/UIB-layouts-grid-template-areas.png "Grid template areas")

10. Collapse the expanded view, and then click **Apply**.

    ![Applying a layout change.](../image/UIB-layouts-click-apply.png "Apply a layout change")


### Result

The new CSS Grid layout shows that the new slot was added to the original two-row, two-column layout.

![New custom layout.](../image/UIB-layouts-custom-finalview.png "New custom layout")

Click **Reset to original** to reset the layout changes back to the original at any time.

![Arrow pointing to reset to original option.](../image/UIB-layouts-reset-to-original.png "Reset a layout")

**Related topics**  


[Create a Flexbox layout with the old layout system](flexbox-uib.md#)

