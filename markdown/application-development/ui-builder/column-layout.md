---
title: Column layouts
description: Column layouts are used to design and organize UI Builder pages.Add a column layout in UI Builder to build structure and organize components on an experience page.Configure column layouts in UI Builder to add the appropriate number of columns and the look you want on an experience page.In UI Builder, if a column contains multiple components, set the gap between the components.Set advanced column layout options in UI Builder including stack width and column layout height.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Organize components in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Column layouts

Column layouts are used to design and organize UI Builder pages.

This video shows you how to perform the following procedure.This video shows you how to add a column layout to a UI Builder page.

Column layouts enable you to create useful and visually appealing pages in an experience. A column layout is a type of flexible container that can hold components. Column layouts are simple layouts that are preconfigured, enabling you to design an efficient and attractive page quickly. It's useful to define and set the structure of the page with column layouts before adding components.

Column layouts can have columns of equal or different widths.

![Examples of column layouts available in UI Builder.](../image/column-layout-examples.png)

You can configure the column layout as a whole and the individual columns within the layout. For example, set a different border width and color for a column layout and for the individual columns within the layout.

![UI Builder page with a single column layout containing a heading and then a three column layout underneath.](../image/column-layout-sample-two-layouts.png)

**Note:** Currently, hiding/showing columns in a column layout based on conditions isn't supported.

**Parent Topic:**[Organize components in UI Builder pages](work-layouts.md)

## Add a column layout

Add a column layout in UI Builder to build structure and organize components on an experience page.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md) or open a page.

4.  Select **+ Add content** in the content tree.

5.  Select one of the **Basic** options on the **Layouts** tab.

    ![Floating component menu in UI Builder with layouts tab displayed listing the basic column layout options.](../image/nav-toolbox-layouts.png)

    The column layout appears on the stage so you can add components to the columns. See [Add and configure components](../task/add-components.md#) for more information.![Column layout with three empty columns.](../image/column-layout-on-stage.png)

6.  Add additional column layouts above or below.

    -   In the content tree, select and hold \(or right-click\) on a column layout name or select the Menu icon for a column layout. Then, select **Add before** or **Add after** from the list and select a layout.

        ![Content tree with column layout menu icon selected showing the options to add before or after the selected column layout.](../image/column-layout-add-from-content-tree.png)

    -   On the stage, select a column layout, and then select the plus sign at the top or bottom.

        ![Existing two column layout with plus sign icons to add additional column layouts.](../image/column-layout-add-above-below.png)


## Configure column layouts

Configure column layouts in UI Builder to add the appropriate number of columns and the look you want on an experience page.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md) or open a page.

4.  If the page doesn't already contain a column layout, [Add a column layout](column-layout.md#).

5.  Add \(up to a maximum of six\) columns using the content tree, the stage, or the configuration panel.

    -   In the content tree, select and hold \(or right-click\) on a column name or select the Menu icon for a column and then select **Add column before** or **Add column after** from the list.

        ![Content tree with column menu icon selected showing the options to add a column before or after the selected column.](../image/column-add-from-content-tree.png)

    -   On the stage, select a single column, select the Menu icon next to the column name, and then select **Add column before** or **Add column after** from the list.

        ![Stage shown with column menu icon selected showing the options to add a column before or after the selected column.](../image/column-add-from-stage.png)

    -   On the stage, select and hold \(or right-click\) on a column and then select **Add column before** or **Add column after** from the list.

        ![Stage shown with column menu open and black arrows pointing to the options to add a column before or after the selected column.](../image/column-add-from-stage2.png)

    -   In the content tree, select a column layout and then on the stage select the + plus icon to add columns to the right side of the column layout.

        ![Stage shown with a column layout selected and a black arrow pointing to the plus icon for adding additional columns.](../image/column-add-from-stage3.png)

    -   In the content tree, select a column layout and then in the configuration panel use the + plus icon next to **Columns** to add columns to the right side of the column layout.

        ![Column layout configuration panel with black arrow pointing to the layout columns option.](../image/column-add-from-config-panel.png)

    **Note:** Columns can be nested inside one another, but this level of complexity isn't often required on pages.

6.  Rename a column by editing the column label from the content tree, the stage, or the configuration panel.

    -   In the content tree, select and hold \(or right-click\) on a column name or select the Menu icon for a column, select **Rename**.
    -   On the stage, select the Menu icon next to a column name, select **Rename**.
    -   In the configuration panel, select the information icon next to the column name.

        ![Arrow pointing to configuration panel column name information icon and pop-up window expanded showing column label field.](../image/column-rename.png)

    Renaming columns can help you distinguish between different columns on the stage and in the content tree. If you have a complex page with many column layouts and columns, it is useful to rename columns.

7.  To change the width of a column in a layout, select the column layout \(in the content tree or on the stage\), then drag a column divider on the stage left or right to make the column narrower or wider.

    ![Animation showing how to resize a column by dragging the column divider.](../image/uib-resize-columns-video.gif)

    The width percentages at the top of the columns change automatically as you drag the column divider. The percentages add up to 100%. When resizing a column, be aware of how much space the component or components within the column need. For example, list and form components usually don't display well in narrow columns.

8.  Distribute columns in a layout evenly across the horizontal using the content tree, the stage, or the configuration panel.

    -   In the content tree, select and hold \(or right-click\) on a column layout name or select the Menu icon for a column layout, and then select **Distribute columns evenly** from the list.
    -   On the stage, select a column layout, select the Menu icon next to the column layout name, and then select **Distribute columns evenly** from the list.
    -   Select a column layout \(in the content tree or on the stage\) and in the configuration panel select **Distribute columns evenly**.
9.  Reorder columns \(including their contents\) within a column layout using the content tree or the stage.

    -   In the content tree, select the column and drag it to a different position \(a blue horizontal line shows where the column can be dropped\).

        ![Arrow pointing from column in content tree to new location in the tree denoted with a blue, horizontal line.](../image/column-rearrange-content-tree.png)

    -   On the stage, select a column header, drag the column to a different position, and drop the column into the drop zone defined by a vertical magenta line.

        ![Arrow pointing from column header on stage to a drop zone denoted by a vertical magenta bar.](../image/column-rearrange.png)

    If you reorder the column in the content tree the stage updates, and if you reorder on the stage the content tree updates.

10. Specify the amount of space between columns from the content tree, the stage, or the configuration panel.

    -   In the content tree, select and hold \(or right-click\) on a column layout name or select the Menu icon for a column layout, select **Layout** from the list, and select a size option in **Column gap**.
    -   On the stage, select a column layout, select the Menu icon next to the column layout name, select **Layout** from the list, and select a size option in **Column gap**.
    -   Select a column layout \(in the content tree or on the stage\) and in the configuration panel select a size option in **Column gap**.

        ![Component panel with column gap field expanded to show options.](../image/column-layout-column-gap.png)

11. Select the Tree icon to navigate to a different layer of content, for example, from a column to the parent column layout or a child component.

    ![Arrow pointing to tree icon for navigating column layouts, columns, and components on the stage.](../image/stage-tree-icon-navigate.png)

12. Delete columns from the content tree or the stage.

    -   In the content tree, select and hold \(or right-click\) on a column name or select the Menu icon for a column, and then select **Delete column** from the list.
    -   On the stage, select a single column, select the Menu icon next to the column name, and then select **Delete column** from the list.
    -   In the content tree, select a column layout and then in the configuration panel use the - minus icon next to **Columns** to remove columns from the right side of the column layout.
    For information about editing column spacing, see [Set the gap between components in columns](column-layout.md#).


## Set the gap between components in columns

In UI Builder, if a column contains multiple components, set the gap between the components.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md) or open a page.

4.  If the page doesn't already contain a column layout, [Add a column layout](column-layout.md#).

5.  Within a single column, add two components

    1.  In the content tree, identify a column and select **+ Add content** under the column name.

    2.  In the toolbox window, select a component, for example, **Avatar**.

    3.  In the content tree, move your mouse over the name of the component you just added, select the open menu \(three vertical dots\) icon, and select **Add after**.

        ![In the content tree, an arrow pointing to the open menu icon for the avatar component and a second arrow pointing to the add after option in the floating menu.](../image/column-gap-add-component.png)

    4.  In the toolbox window, select another component, for example, **Button**.

6.  Select **Save**.

7.  In the content tree, select the column to which you added the two components.

8.  In the configuration panel, select a size option in **Gap**.

    ![In the configuration panel, an arrow pointing to the gap field and a second arrow pointing to the gap drop down menu with various sizes listed.](../image/column-gap-choose-size.png)

9.  To specify an exact gap size in pixels, move your mouse over the **Gap** field, select the **Use custom value** \(pencil\) icon, and type in a number, for example, `300px`.

    ![In the configuration panel, a black arrow pointing to the gap field and a second black arrow pointing to the use custom value icon.](../image/column-gap-custom-size.png)

10. To change between stacking the components and placing them next to each other in the column, select the **Row** or **Column** icon in **Direction**.

    ![In the configuration panel, a black arrow pointing to the direction field and a second black arrow pointing to the row and column icons.](../image/column-gap-direction.png)

    To reverse the order and placement of the components in the column, select the **Advanced** \(three horizontal dots\) icon in **Direction**, and then select the **Reverse** option.

    ![In the configuration panel, a black arrow pointing to the direction field and a second black arrow pointing to the advanced direction icon.](../image/column-gap-direction-advanced.png)


## Set advanced column layout options

Set advanced column layout options in UI Builder including stack width and column layout height.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](../task/create-page.md) or open a page.

4.  If the page doesn't already contain a column layout, [Add a column layout](column-layout.md#).

5.  Select a column layout containing two or more columns in the content tree.

    ![Content tree with column layout one selected.](../image/column-layout-selected-in-tree.png)

6.  To set a stack width, go to **Configuration panel &gt; Layout** and select **Show advanced layout options**.

    **Note:** Setting a stack width enables you to control how a page with column layouts looks in a narrow browser window, tablet, or mobile device.

    ![Configuration panel with black arrow pointing to show advanced layout options link.](../image/column-layout-show-advanced-options.png)

7.  Type a width in **Stack columns below**.

8.  Select **Save**.

9.  To test the updated stack width, select the arrow next to **Preview** and select **Open URL path**.

10. Reduce the browser window width to less than the stack width that you specified to check that the columns on the right move below the first column.

11. Close the browser tab that opened with the URL path.

12. To control column layout height, select a column layout with two or more columns in the content tree, go to **Configuration panel &gt; Layout**, and select **Show advanced layout options**.

    **Note:** Setting height is useful if your column layout contains a component that can be tall, like the List component.

13. Under **Sizing**, type numbers into one or more of the options \(**Height**, **Min. H**, and **Max. H**\), and set the sizing unit \(for example, **px**, **%**, or **em**\).

    ![Configuration panel with black arrow pointing to advanced sizing option.](../image/column-layout-advanced-sizing.png)

14. Select **Save**.

15. To test the updated sizing, select the arrow next to **Preview** and select **Open URL path**.

16. Reduce and expand the browser window height to test the specified values.

17. Close the browser tab that opened with the URL path.


