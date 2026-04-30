---
title: Associate a function with a location in the app
description: For each function you create for an app, you must associate it with a specific location. You can associate most functions with a top menu, a swipe, or a specific field.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Associate a function with a location in the app

For each function you create for an app, you must associate it with a specific location. You can associate most functions with a top menu, a swipe, or a specific field.

## Launcher screen header functions

<table id="table_sgr_glt_1nb"><tbody><tr><td>

Launcher screen header functions allow your users to navigate to a specific parametrized record screen. Some common examples include navigating to a users profile, or navigating to a cart.

 For details on creating parametrized record screens, see [Configure a parameterized record screen](../task/configure-param-form-applet.md).

 For details on how to use these record screens in a launcher screen header, see [Configure a launcher screen header](../task/create-alp-header.md).

</td><td>

![Launcher screen.](../image/applet-launcher-1.png "Launcher screen header function")

</td></tr></tbody>
</table>## Chart header functions

<table id="table_kxn_4jt_1nb"><tbody><tr><td>

Chart header functions enable your users to navigate to a specific set of records from a chart screen. When a user is viewing a chart, they can click on the chart header function \(![chart function icon](../image/chart-function-icon.png)\) on the top-right corner of the screen, to view a list of all the records that are within the chart. .

</td><td>

![Chart screen with header functions.](../image/chart-function.png "Chart header function")

</td></tr></tbody>
</table>## Field functions

<table id="table_n1w_ptw_wlb"><tbody><tr><td>

Field functions enable your end users to change the value of a field. Field functions only apply to items on the details screen in a displayed area.

 1.  In Mobile App Builder, open a details screen that you want to add a field function to. Make sure that there are screen fields in your details screen that you can add field functions to, and a Table selected.
2.  For each screen field on your details screen, you can add a field function under **Field function instances** field. You can't reuse previous function instance records.
3.  In the **Display label** field of the new Function instance record, add the name of the function to display.
4.  Select **Save**.

 For more information on how to create field functions, see [Configure a details screen for a record screen](../task/configure-form-details-screen.md).

</td><td>

![Incident with the caller field highlighted.](../image/FieldFunction.png "Field function")

</td></tr></tbody>
</table>## Footer functions

<table id="table_vgx_qtw_wlb"><tbody><tr><td>

Footer functions enable your end users to add an action on the bottom of a record screen.

 Supported screens for the footer function are: record details screen, record embedded section screen, dynamic segments in a record screen, map screen, and list screens.

 1.  In Mobile App Builder open a screen that you want to add a footer function to.
2.  In the Footer function instance section, select **New** to create a function instance. You cannot reuse previous function instance records.
3.  In the **Display label** field of the new Function instance record, add the name of the function to display.
4.  Complete all the other required inputs for the record, then select **Save**.

 For more details on how to create a footer function, see [Use your navigation function as a footer function](../task/sg-launcher-navigation-example-4.md).

</td><td>

![Screen with three footer functions.](../image/footer-functions.png)

</td></tr></tbody>
</table>## On tap functions

<table id="table_cx1_g3t_1nb"><tbody><tr><td>

Use the on tap function instance to trigger a function when a user taps on a record in a list. This function location can, for example, navigate a user to another screen when they tap a record. On tap functions are configured on list item config records, which are used in any screen that needs to display a list of records. 1.  In Mobile App Builder open a list screen that you want to add an on tap function.
2.  Select the List item config record field. For example, this field is found in a stream record within a screen segment record.
3.  In the list item config record, locate the **On tap** field and select **Use a function instance**.
4.  Populate the list item config record with the navigation function that you want to use.
5.  Select **Save**.

</td><td>

![Navigation function used to direct users from one list to another.](../image/list-to-list-example-2.png)

</td></tr></tbody>
</table>## Top menu functions

<table id="table_dlr_dsw_wlb"><tbody><tr><td>

Use top menu function location for less frequently used actions, and on record screens where you have more actions than fit conveniently in the footer.

 1.  In Mobile App Builder open a screen that you want to add a top menu function to.
2.  In the Top menu function instances section, select **New** to create a new function instance. You can't reuse previous function instance records.
3.  In the new Function instance record, populate the **Display** label with the words you want displayed on your function. In the Function placement section, the fields are auto-populated based on your screen record’s details.
4.  Select **Save** after filling in all other required inputs on each record.

 For more details on how to create a top menu function, see [Use your navigation function as a top menu selection](../task/sg-launcher-navigation-example-3.md).

</td><td>

![Top menu for an incident which includes the following functions: Reassign, Resolve, Add comments, and Edit.](../image/top-menu.png "Top menu functions")

</td></tr></tbody>
</table>## Quick action functions

<table id="table_irj_qsw_wlb"><tbody><tr><td>

Use the quick action item location to provide your users with a shortcut to an item or action in your launcher screens. Users access quick actions by tapping the quick action icon.

-   For Android users quick actions appear under a plus icon \(![Android quick action icon](../image/quick-action-icon.png)\) at the bottom-right corner of the launcher screen.
-   For iOS quick actions appear under the ellipsis icon \(![iOS quick action icon](../image/quick-action-icon-ios.png)\).

 For details on configuring quick actions, see [Quick actions](../task/sg-config-quick-actions.md).

</td><td>

![Quick actions.](../image/launcher-quick-action.png)

</td></tr></tbody>
</table>## Swipe functions

<table id="table_ckp_ltw_wlb"><tbody><tr><td>

The swipe function location applies to screens that display a list, including a map screen. Swipe functions can be initiated from two directions, swiping to the right initiates leading swipe function and swiping to the left initiates trailing swipe functions. You can display three functions per direction.

1.  Navigate to a screen that you want to add a swipe function to. Navigate to that list screen’s List item config record. For example, this field is found in a stream record within a screen segment record.
2.  Select which direct to initiate the swipe functionality:
    -   Select **Leading swipe function instances** for users to initiate swipe functions dragging to the right from the edge of a card.
    -   Select T**railing swipe function instances** for users to initiate swipe functions dragging to the right from the edge of a card.
3.  In the new function instance record, populate the **Display label** with the words to display on your function. In the **Function placement** section, the fields are auto-populated based on your screen record’s details.
4.  In the Function section, select the function record you would like to use, or select **New**. This function determines the behavior that the system performs when a user taps the footer function.
5.  Select **Save** after filling in all other required inputs on each record.

 For more details on how to create a standard function, see [Configure a navigation to a screen](../task/sg-config-navigation-function.md).

</td><td>

![Swipe function from the list view with options to Resolve or Reassign an incident.](../image/SwipeFunction.png "Swipe functions")

</td></tr></tbody>
</table>## Top icon functions

<table id="table_whq_122_t1c"><tbody><tr><td>

The top icon function is a button location on the record screen top app bar. Use the top icon action to provide your users with an additional shortcut to an item or to actions in your record screen.

 Only one top icon function can be added to each record screen.

</td><td>

![Image of top icon function mobile screen](../image/top-icon-function-button-instance.png "Top icon function")

</td></tr></tbody>
</table>## Custom map bottom drawer functions

<table id="table_ljf_q22_t1c"><tbody><tr><td>

The custom map bottom drawer functions apply to the custom map screen for Indoor Wayfinding experiences. Use the custom map bottom drawer functions to provide your users with a shortcut to actions from Indoor Wayfinding experiences. One or more custom map bottom drawer functions can be added to a custom map screen.

 If only one custom map bottom drawer function is configured, users see the action button for the function with the configured icon and labels. If more than one function is configured, all the functions appear under the more menu icon \(![more menu icon](../image/button-more-ios.png)\).

</td><td>

![Custom map bottom drawer function button.](../image/cust-map-bot-drawr-func-butn-instns.png "Custom map bottom drawer function")

</td></tr></tbody>
</table>