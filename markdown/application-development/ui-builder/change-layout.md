---
title: Change the layout of a page created in Quebec or Rome
description: Add and modify your layout design to change the way your page looks. Choose how components are displayed on a page through Cascading Style Sheets \(CSS\) web layout technologies, such as Flexbox and CSS Grid.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Organize components in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Change the layout of a page created in Quebec or Rome

Add and modify your layout design to change the way your page looks. Choose how components are displayed on a page through Cascading Style Sheets \(CSS\) web layout technologies, such as Flexbox and CSS Grid.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Layouts control what containers and components are available on a page, and where they are. CSS rules apply to them. You can change the layout as follows.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  [Create](create-page.md) or open a page.

4.  Select the **Layout** tab.

5.  Depending on the type of page, do one of the following to select a container to update.

<table id="choicetable_cc5_jsb_dqb"><thead><tr><th align="left" id="d254375e139">

Type of page

</th><th align="left" id="d254375e142">

Instruction

</th></tr></thead><tbody><tr><td id="d254375e148">

**Existing page**

</td><td>

Select the container on your page for which you want to change the layout.**Note:** Alternately, you can select the container in the content tree to the left of the main page area. When the page structure is in the structured tree, you can more easily find the container you want to change. If you have many components and containers in the content tree, use the search bar to find a specific container.

</td></tr><tr><td id="d254375e160">

**New page**

</td><td>

In the content tree to the left of the main page area, select the **Body** of your page. **Body** is the root element of the page.

 ![Arrow pointing to body element in the content tree structure.](../image/UIB-content-tree-body.png)

</td></tr></tbody>
</table>    If you are starting a new page, you can select the layout at the page level, and later at the container level. If you are not the owner of an existing page, be aware of the impact of changing the layout at the page level.

6.  Change the layout of your container.

    1.  In the Page configuration pane, select the **Layout** tab to select the layout that you want to use.

        You can change the current layout of an existing page into a new one. For example, in a three-column layout, you can click the four-column layout to change the layout.

        You can also set the layout for a container. The following image shows the layout options for the UI Builder.

        ![Layout options for UI Builder.](../image/UIB-layouts.png)

    2.  If you are creating a page, add components to the new areas in your layout.

    3.  Click **Save**.

    4.  View and test your page by selecting ![Preview button that opens your page in runtime, which is a preview of how the page looks on a web page.](../image/preview-button.png).

    For changing an existing page, the following video shows how you can change the container layout from three to four columns, and then add a new component to the fourth column.

    ![Changing the layout of an existing page.](../image/UIB-change-layout-video.gif)

    For setting the layout of a new page, the following video shows you how to set the layout that you want for the page. For example, you can set your page to have two slots or columns. Then, you can add containers to each slot and change the layout for each container. You can also set the layout at the container level after you add containers to your page.

    ![Changing the layout of a page](../image/UIB-change-layout-page.gif "Change the layout of a page")

7.  Add components to slots.

    You build your page with containers components. See [Customize UI Builder pages using components](../concept/work-components.md) for more information.

    You can add components by using any of the following ways.

<table id="choicetable_dzv_llh_wnb"><thead><tr><th align="left" id="d254375e310">

To add a component

</th><th align="left" id="d254375e313">

Do the following

</th></tr></thead><tbody><tr><td id="d254375e319">

**Directly from your page \(option 1\)**

</td><td>

Select the add content \(plus\) icon, select the **Components** tab, and then select a component.

</td></tr><tr><td id="d254375e336">

**Directly from your page \(option 2\)**

</td><td>

On a column layout or component, select the add before \(plus\) or add after \(plus\) icon, and then select a component.

</td></tr><tr><td id="d254375e348">

**From the content tree**

</td><td>

In the content tree, select **+ Add content** and then select a component.

 ![Black arrow pointing to + add content option in content tree next to the toolbox window with Components tab selected.](../image/component-add-from-content-tree.png)

</td></tr><tr><td id="d254375e370">

**From the floating menu above the page**

</td><td>

On a column layout or component, select the Menu icon, select **Add before** or **Add after**, and then select a component.

</td></tr></tbody>
</table>8.  Modify the layout styling options in any of the following ways.

<table id="choicetable_n3q_gmd_jjb"><thead><tr><th align="left" id="d254375e397">

Option

</th><th align="left" id="d254375e400">

Instruction

</th></tr></thead><tbody><tr><td id="d254375e406">

**Change the layout styling**

</td><td>

1.  Click a container for which you want to change the layout.

You can click the container in the content tree, or you can click the container on the page.

2.  From the floating menu above the page, click **Layout**.

![Location of change layout icon on the floating menu.](../image/UIB-layout-change.png)

3.  Choose to display your content as either Flex or Grid. For more information about flex or grid options, see [Using Flexbox layouts in UI Builder](../concept/flexbox-uib.md#) or [Using CSS Grid layouts to build a page](../concept/css-grid-uib.md#).


</td></tr><tr><td id="d254375e460">

**Choose Flex**

</td><td>

1.  From the Display list, select **Flex**.

![Flex or grid option in a drop-down.](../image/UIB-flex-or-grid-option.png)

2.  Select the following options based on how you want to display your container content on the page. The options can also be entered in the CSS styles box:

    -   Flex direction: Choose from **Row**, **Row-reverse**, **Column**, or **Column-reverse**.
    -   Justify content: Choose from any of the following:
        -   **Flex-start**: Items are at the start of the flex direction, similar to left-justified content. This is the default setting.
        -   **Flex-end**: Items are at the end of the flex direction, similar to right-justified content.
        -   **Space-between**: Items are distributed evenly.
        -   **Space-around**: Items are distributed evenly with equal space around them.
        -   **Space-evenly**: The spacing between items is equal.
    -   Align items: Defines how you want your flex content displayed along the cross axis. Choices are as follows:
        -   **Stretch**: Stretch your content to fill the container. This is the default setting.
        -   **Flex-start**: Place your content at the start of the cross axis.
        -   **Flex-end**: Place your content at the end of the cross axis.
        -   **Center**: Center your content in the cross axis.
        -   **Baseline**: Align your content the same as your baseline alignment.
    -   Height: Set the height automatically, or manually.
    -   Width: Set the height of your flexbox items automatically or manually.
    -   Margin: Set your minimal distance between flexbox items.
    -   Padding: Set the padding for each side of your flexbox items.
![Flex style options.](../image/UIB-flexbox-styling.png)

</td></tr><tr><td id="d254375e592">

**Select Grid**

</td><td>

1.  From the Display list, select **Grid**.

![Grid selected from the Display list.](../image/UIB-grid-select.png)

2.  Fill in the following information:
    -   Height: Set the height automatically, or manually.
    -   Width: Set the height of your grid items automatically or manually.
    -   Margin: Set your minimal distance between grid items.
    -   Padding: Set the padding for each side of your grid items.


</td></tr></tbody>
</table>
**Parent Topic:**[Organize components in UI Builder pages](../concept/work-layouts.md)

