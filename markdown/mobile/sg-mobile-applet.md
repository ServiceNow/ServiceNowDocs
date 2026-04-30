---
title: Mobile screen types
description: Learn how to use screens in ServiceNow mobile. Use screens to make your mobile app functionality available to your end users.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile screen types

Learn how to use screens in ServiceNow mobile. Use screens to make your mobile app functionality available to your end users.

## Screen types

Screens are made up of one or more embedded screens, which are screens embedded with a record screen. Each screen has configurable components, conditional formatting, sorting order, and filters.

You can choose one of the available screen types within Mobile App Builder. Each screen type provides a unique experience or work flow, typically one per navigation tab, which your users can access on their mobile app The screen types may include other optional screens for your users to access for additional information. All screens display information that is based on records in a data item.

![Menu of screen types](../image/mab-screen-select.png)

<table id="table_ugs_vkb_nlb"><tbody><tr><td>

Launcher screen

 Launcher screens serve as landing pages or home pages. Using a launcher screen, you can access screens in various formats, as well as search, do quick actions, and find user information.

 For more information, see [Launcher screens](sg-mobile-applet-launcher.md).

</td><td>

![Launcher screen.](../image/launcher-screen-mobile.png)

</td></tr><tr><td>

List screen

 Use list screens to display a list of records queried from a data item. List screens can be configured together with a record screen. When both screens are configured together, your users can tap a record on the list screen to display the record screen for that record.

 For more information, see [List screen](list-screen.md).

</td><td>

![List screen.](../image/mobile-list.png)

</td></tr><tr><td>

Grouped list screen

 Use a grouped list screen to display a list of records that are grouped by a specific field. A group list screen uses a special group by data item.

 For more information, see [Grouped list screen](grouped-list-screen.md).

</td><td>

![Grouped list screen.](../image/GroupedListApplet.png)

</td></tr><tr><td>

Record screen

 User record screens to display information from one specific record. On a record screen, you can configure up to 4 different types of embedded screens as segments. These 4 different types of embedded screens include details, activity, related lists, and embedded lists.

 For more information, see [Record screen](form-screen.md).

</td><td>

![Record screen.](../image/form_applet.png)

</td></tr><tr><td>

Map screen

 Use a map screen to display a dynamic map that lets your users see the locations that are associated to the records in a data item. Below the map, your users can see data cards that show information about these records. Users can tap a card to see details for the record.

 -   The record screen shows additional information that you define when a user taps a record.
-   \(Optional\) The activity stream screen shows the activity stream details for a selected record.
-   \(Optional\) The related lists screen shows the related lists for a selected record.

 For more information, see [Map screen](map-screen.md).

</td><td>

![Map screen.](../image/SGMapScreen.png)

</td></tr><tr><td>

Calendar screen

 Use a calendar screen to display records associated with date fields. Users can tap a date on the calendar portion of the screen to see records associated with a specific date, in the event stream displayed in the lower portion of the screen. The record screen shows additional information that you define when a user taps a record.

 For more information, see [Calendar screen](calendar-screen.md).

</td><td>

![Calendar screen.](../image/CalendarScreen.png)

</td></tr><tr><td>

Mobile web screen

 Use a mobile web screen to open a URL from within a ServiceNow app. You can configure relative URLs to open pages within the ServiceNow platform, or an external link. For example, a user can see a knowledge article on the instance via the Service Portal.

 Relative URLs that direct your users to open pages within your instance are opened inside the mobile app. URLs that open external links will open the link in the default browser of the user's mobile device.

 For more information, see [Mobile web screen](url-screen.md).

</td><td>

![Mobile web screen.](../image/url_screen.png)

</td></tr><tr><td>

Chart screen

 Chart screens display an interactive view of a report or performance analytics chart. Users can tap on a chart to display a list of relevant records.

 -   The chart screen can display time series and single score reports that are used in the web-based UI.
-   The chart screen can display score type reporting charts that are configured to use the **Latest score** visualization.

 For more information, see [Chart screen](chart-screen.md).

</td><td>

![Chart screen.](../image/chart-applet.png)

</td></tr><tr><td>

Input form screen

 Input form screens display inputs to allow your users to quickly enter information into mobile apps. Use input form screens to create or edit records, complete surveys, or any other situation where your users need to enter information.

 Input form screens are screens that you use to execute an action or a function. They are not the first screen a user interacts with in a workflow.

 For more information, see [Input form screen](parameter-input-screen.md).

</td><td>

![Input form screen.](../image/input-form-screen.png)

</td></tr></tbody>
</table>