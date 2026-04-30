---
title: Configure font type icons
description: Configure font type icons that can be used in a variety of places in mobile apps. For example, you can use font type icons in screens, cards, functions for quick actions, and navigation bars and tabs.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile icons, Mobile styles, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure font type icons

Configure font type icons that can be used in a variety of places in mobile apps. For example, you can use font type icons in screens, cards, functions for quick actions, and navigation bars and tabs.

## Before you begin

Role required: admin

## About this task

You can configure an icon within the work flow of configuring a screen or you can configure an icon by selecting the **Cards &amp; icons** category from the Mobile App Builder menu. This procedure uses the **Cards &amp; icons** category.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Cards &amp; icons** category, and then select **New**.

4.  In the Create a card or icon dialog box, select **Icon**, and then select **Continue**.

5.  In the Icon form, enter a **Name** for the icon.

    Make sure you choose a name that makes it easy to identify the icon.

6.  From the Type drop-down list, select **Font**.

7.  In the Set appearance section, enter the following information in the **Style** and **Value** fields to configure the font icon.

    Select the plus icon to add a row.

<table id="table_vkm_zn3_vwb"><thead><tr><th>

Style

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Enter `FontName`

</td><td>

Enter one of the following font families:

 -   `now-mobile-icons`

These icons are designed to be used in screens. Use them for lists and section destinations that go to list screens and browser screens. Use these icons to represent a work flow or a screen that you want users to navigate to.

-   `now-mobile-icons-cards`

Use these icons in the body of cards.

-   `now-mobile-icons-buttons`

These icons are designed to be used for functions. They can be used on buttons that are located on cards or for quick actions.

-   `now-mobile-icons-ALPnavbar`

These icons appear in the upper right corner of your mobile screen and are used as navigation to another screen.

</td></tr><tr><td>

Enter `Value`

</td><td>

Enter the code that identifies the icon in the font family you want to use. For example, `e903` is the code for the solid cart icon in the **now-mobile-icons-buttons** font family.

 For lists of font family icon codes, see the topic for the type of icon you want to use in the [Mobile icon reference](../concept/mobile-icon-reference.md).

</td></tr><tr><td>

Enter `FontColor` to specify a hex code for the color of your icon.

 This configuration is optional. If you do not specify a color, the default icon color is black.

</td><td>

Enter the hex code for the color you want to use. For example, to specify a red icon, enter `#FF494D`.

</td></tr><tr><td>

Enter `Name`

</td><td>

Enter the name listed for the icon in the font family. For example, if you wanted to use the shopping cart icon in the **now-mobile-icons** font family, you should enter `Cart`.

 For lists of font family icon names, see the [Mobile icon reference](../concept/mobile-icon-reference.md).

</td></tr></tbody>
</table>8.  Select **Save**.


## What to do next

After you create the font family icon, you must use Mobile App Builder to configure a mobile app to use the icon. For more information, see [Add a font icon in a mobile app](config-using-font-icon-in-mobile-app.md).

