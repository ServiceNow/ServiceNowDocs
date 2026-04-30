---
title: List screen
description: Use a list to display a list of records. Records in lists display in a card format, showing a limited selection of the information in the record.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# List screen

Use a list to display a list of records. Records in lists display in a card format, showing a limited selection of the information in the record.

<table id="table_w4s_g2w_dlb"><tbody><tr><td>

Use a list screen to see records in a list view. Within a list screen, each record has a card. This card is a visualization which contains a selected few fields that display as a preview for each record. You can configure the card in Mobile Card Builder \(MCB\). MCB can be accessed from Mobile App Builder \(MAB\) when creating a list screen.

 Use the optional features available with list screens to improve your user's experience.

-   **Record screen**

Configure your list screen to include a record screen. This configuration automatically displays a detailed view of a record when your users tap it in the list screen. Learn more about record screens in [Record screen](form-screen.md).

-   **List filters**

Mobile list filters enable your users to find what they need in the records on your instance. For more detail on filters, see [Mobile list screen filters](mobile-list-filters.md).

-   **Dynamic screen name**

Configure your list screen to inherit the name of a previous screen selection or form field and display it as the header on a subsequent screen. For more information, see [Configure a dynamic screen name for a list screen](../task/dynamic-screen-titles.md).

-   **Functions**

Functions determine which actions users can perform in your mobile apps. For more detail on functions, see [Mobile functions](sg-studio-mobile-button-types.md).


</td><td>

![List screen.](../image/mobile-list.png)

</td></tr></tbody>
</table>## Configure lists with forms

<table id="table_y4t_zv3_nlb"><tbody><tr><td>

Configure your list with a record screen so your users can tap list items to view details of the records on your list. For details on list configuration, see [List screen configuration](../task/sg-configure-list-screen.md).

</td><td>

![List and form screens.](../image/form-and-list.png)

</td></tr></tbody>
</table>## Parametrized list screens

<table id="table_plp_sw3_nlb"><tbody><tr><td>

Use parameters to pass information into your list screens. For example, when a user taps on a group in a group list screen, a list containing records in the group is displayed. The list of records in the group is a parametrized list, which accepts the value of the group your user selected as a parameter.

 To learn about parametrized list configuration, see [Parametrized list screens](list-applet-parameters.md).

</td><td>

![Opening a parametrized list of records from a group list.](../image/param-list.png)

</td></tr></tbody>
</table>## List screen functions

Add functions to your list screens to give your users the ability to take actions directly on a record screen. List screens support swipe, footer, and top menu functions. For more information on functions, see [Mobile functions](sg-studio-mobile-button-types.md).

<table id="table_o45_nbq_slb"><tbody><tr><td>

Swipe functions

 Use swipe functions to act on a specific record on the list. You can configure one or more actions to appear when a user swipes on a record. You can also configure a different set of actions depending on whether a user swipes to the left or to the right.

</td><td>

![Swipe function from the list view with options to Resolve or Reassign an incident.](../image/SwipeFunction.png)

</td></tr><tr><td>

Top menu functions

 Use top menu actions for less frequently used actions, or actions that apply to the list rather than individual records, such an **Approve all** action.

</td><td>

![Top menu for an incident which includes the following functions: Reassign, Resolve, Add comments, and Edit.](../image/top-menu.png)

</td></tr><tr><td>

Footer functions

 Footer functions enable your end users to take an action on a menu item located in a screen's footer region.

</td><td>

 

</td></tr></tbody>
</table>## List screen filters

By default, the instance automaticaaly creates filter and sorting functionality. This filter is based on the fields selected in your list pattern. No further configuration is needed. Users can filter and sort the list based on any of these fields.

If the default filters do not fit your requirements, you can create a custom filter. You can manually select the fields that are available to the list filter and enable keyword filtering. For more information about list screen filters, see [Mobile list screen filters](mobile-list-filters.md).

## Dynamic screen name

Use dynamic screen name functionality to let users to easily identify the screen or field which they are currently viewing. You can configure a screen to inherit a name from a previous screen selection. These dynamic names can be used with grouped lists, where the selected group name becomes the header on a subsequent screen. Alternatively, a field in a form can be used as a header in a different screen. For more information, see [Configure a dynamic screen name for a list screen](../task/dynamic-screen-titles.md).

<table id="table_rjt_nmr_ylb"><tbody><tr><td>

Display name from a redirection parameter

 Use a dynamic screen name to inherit a name from a previous screen selection. In the example, the screen name comes from a list which is grouped by category from a launcher screen.

</td><td>

![Display screen name from a redirection parameter.](../image/dynamic-name-redirection-parameter.png)

</td></tr><tr><td>

Display information from field previous record

 Use dynamic record screen names to display information from a specific record in a table. The record screen name can come from any field in a database record. In the example, the screen name comes from the incident field.

</td><td>

![Dynamic screen name displayed from field in previous record.](../image/dynamic-name-form-screen.png)

</td></tr></tbody>
</table>