---
title: Configure a card action using Mobile Card Builder
description: Use Mobile Card Builder to add card actions to a mobile card.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Card actions, Mobile Card Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Configure a card action using Mobile Card Builder

Use Mobile Card Builder to add card actions to a mobile card.

## Before you begin

Role required: admin or delegated developer

For more information about the delegated developer role, see [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

## About this task

When creating mobile cards, you may want to add buttons to enable your users to perform various actions. Usually the process of configuring card actions occurs when creating a card template within the Mobile Card Builder. This topic details the process of configuring card actions as a standalone procedure.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Card Builder**.

2.  In the Mobile Card Builder menu, select **Templates**.

3.  Select the card template where you want to add a card action and select **Open**, or create a new card template using the **Create blank template** button.

4.  Select a plus icon ![Plus icon.](../image/mcb-plus-icon.png) to select a new component to add to your mobile card.

    ![Adding a component in card builder.](../image/mcb-new-component-2.png)

5.  Select **Button** from the displayed components.

    The Component configuration menu displays options related to button configuration.

6.  Select the display options to define the appearance of your buttons.

    Button configuration options include:

    -   The height and width of a button
    -   The addition of a border and rounded edges
    -   The size of margins to provide padding between other components
7.  Select the format and label properties of the button.

    The available options are:

    -   Label - A button with text only, for example an OK button. Enter the text required for the button.
    -   Icon - A button with an icon only, for example a trash icon \(![Trash icon for card action.](../image/trash-mcb.png)\) to denote a delete button. Select an icon from the menu.
    -   Label and Icon - A button with text and an icon, for example an edit button \(![Edit icon with text and image.](../image/edit-mcb.png)\). Enter the desired text and select the image from the fields.
8.  Select if you want the button to contain a single action or multiple actions.

    The actions listed in the functions menu come from the Function \[sys\_sg\_button\] table.

    -   Single - Search in the function menu to allocate a single action to a button.
    -   Multi - Creates a single button which, when tapped, reveals additional card actions in a menu at the bottom of the screen. Select **Add Menu Item** and from the displayed menu add as many card actions as required. Select **Finish** after you configure each card action.

        Drag the order icon \(![Order icon.](../image/order-mcb.png)\) to change the order of the card actions. You can also edit and delete the card actions at any point.

    ![Multiple action menu for card actions.](../image/multi-menu-mcb.png)

9.  Define the appearance of buttons, in terms of its background color, text color, and border color.

    You can define the color by either:

    -   Manually entering the hexadecimal color value.
    -   Selecting an appearance palette and then select either the Swatches or List tab at the top of the menu.
    ![Color picker for button appearance in card action.](../image/button-appearance-mcb.png)

    **Note:** For icons, black is the only color available for the base record. Select a text color input to change the icon color from black to the selected color.

10. Select **Save**.


