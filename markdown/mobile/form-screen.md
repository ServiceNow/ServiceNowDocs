---
title: Record screen
description: Record screens display content for a specific single record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Record screen

Record screens display content for a specific single record.

Use record screens to display the content of a single record. You can configure functions on record screens to allow users to make edits and take actions. Record screens support top menu functions, footer functions, and smart buttons.

When a record screen is created, a details screen is configured by default. Add any of the five additional screen segment types listed below as needed.

Within a record screen, you can control the embedded screen segments. There are five types of embedded screen segments available for use when configuring a record screen through Mobile App Builder.

## Record screen configuration

Use the record configuration screen in Mobile App Builder to control the content and appearance of your record screen.

![Mobile App Builder Record Screen.](../image/mab-config-for-record-screens.png "The configuration screen for record screens in Mobile App Builder")

## Record screen fields

The record screen configuration form in Mobile App Builder contains the following fields.

-   **Name**

    The screen name for the record header. This name is visible to the end users.

-   **Description**

    Description of the record screen. This name is not visible to end users.

-   **Settings**
    -   **Fetch Type**: Controls when the data is loaded onto the screen. Change your fetch type to optimize load time performance.
    -   **Dynamic Pre-Fetch Count**: Defines when you select a fetch type of **Dynamic**.
    -   **Hide Screen Name**: Hides or shows the screen name in the Record screen.
-   **View Using \(Legacy Card / Card\)**

    A card used for the header section of the record screen. Use Mobile Card Builder to change the appearance of your mobile card or the fields displayed on the card. For more information about using Mobile Card Builder, see [Customize a screen using Mobile Card Builder](../task/mcb-customize-item-view.md).

-   **Icon**

    Icon that appears in the header of the launcher screen.

-   **Alert**

    You can configure a mobile alert overlay for a record screen to inform users of an important message and to redirect them to a specific screen. For more information about configuring an alert, see [Configure a mobile alert for a record screen](../task/form-screen-alerts.md).

-   **Data item**

    The data item defines what table you want data from and what conditions must be met for the data to be displayed. You can select an existing data item or create a new one.

    Data items are not required when a record screen is used as an embedded screen on a list item config.

-   **Record screen segments**
    -   **Record screen segment**: Within a record screen, you can control the embedded screen segments. There are five types of embedded record screen segments you can use when configuring a record screen. These record screen segments are listed in the following section.
    -   **Dynamic record screen segment**: Dynamic segments in a record screen enable users to see a subset of relevant records rather than a whole list of records. Use dynamic segments to create a link between selected elements near the top of the screen and the content displayed below.
-   **__Top menu function__**

    For each function you create for an application, you must associate it with a specific location. For more information, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).

-   **__UI parameters__**

    Parameters are a way of creating a variable or a placeholder for input from an end user or from the database. The variable then queries the database or the user for more information. You can add parameters to a data item or an action item.

-   **Dynamic screen name**

    Dynamically inherit a name from a field in a previous record.

-   **Role access**

    Limit user access to the record screen.


## Record screen segments

<table id="table_glc_lgw_dlb"><tbody><tr><td>

Activity stream screen segment

 Use an activity stream screen to display work notes, comments, and/or attachments for the record. Your users can configure whether all three of these are visible, or only a select few are visible.

 To configure an activity stream screen segment, see [Configure an activity stream screen for a record screen](../task/configure-activity-stream.md).

</td><td>

![Activity stream segment on a form screen.](../image/form-activity-segment.png)

</td></tr><tr><td>

Details screen segment

 Use a details screen to display specific screen fields from the record. On a record screen, you can see the same item view/pattern that was configured for the list item. Embed a details screen in your record screen when you want to display more info about the record.

 For more information on detail screens, see [Configure a details screen for a record screen](../task/configure-form-details-screen.md).

</td><td>

![Details segment on a form screen.](../image/form-details-segment.png)

</td></tr><tr><td>

Embedded browser screen segment

 Use an embedded browser screen to display content from a URL within a browser section. An embedded browser can display information such as related knowledge articles within your forms.

 For more information on embedded browser screens see [Configure an embedded browser screen for a record screen](../task/configure-form-browser-screen.md).

</td><td>

![Embedded browser segment on a form screen.](../image/form-embedded-browser.png)

</td></tr><tr><td>

Embedded list screen segment

 Use an embedded list screen to display a related list as an embedded tab within a record screen. An embedded list can provide a user immediate access to a single related list without the extra tap when using the related list screen.

 To configure an embedded list screen segment, see [Embedded lists for a record screen](sg-embedded-list.md).

</td><td>

![Embedded list segment on a form screen.](../image/form-embedded-list-segment.png)

</td></tr><tr><td>

Related list screen segment

 Use a related list screen to display related lists for the record. Each related list you configure appears in this related list screen. Your users can see the name of the list and tap to see the records within that list.

 To configure a related list screen segment, see [Configure a related list screen for a record screen](sg-mobile-related-lists.md).

</td><td>

![Related list segment on a form screen.](../image/form-related-list-segment.png)

</td></tr><tr><td>

Sections screen segment

 Enrich your record screen with the addition of item UI sections displayed in a card format. This capability presents content and users can trigger actions without the need to navigate to an additional list screen.

 To configure a sections screen segment, see [Configure a record UI section for a record screen](../task/item-section-form-screen.md).

</td><td>

 

</td></tr></tbody>
</table>