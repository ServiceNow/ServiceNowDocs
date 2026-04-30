---
title: Calendar screen
description: Calendar screens display a calendar interface and records associated with the selected date.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Calendar screen

Calendar screens display a calendar interface and records associated with the selected date.

<table id="table_inx_q2b_y2c"><tbody><tr><td>

Users use a calendar screen to display records when the dates relating to those records are relevant. For example, displaying when tasks are due or when important events take place.

 The calendar screen displays a calendar interface. Each date on the screen displays an indicator below any date that has at least one record associated with it.

 Below the calendar, is the events list where your users can see a list of records associated with the date selected in the calendar. You can configure the calendar app to display these records in a record screen when the user taps them. For more information, see [Using the calendar screen](../reference/calendar-screen-using.md).

</td><td>

![Calendar screen example showing multi-day event.](../image/CalendarScreen.png "Calendar screen example showing a multi-day event")

</td></tr></tbody>
</table>## General guidelines for calendar screens

Consider these general guidelines when configuring your calendar screen.

**Note:** For configuration instructions, see [Configure a calendar screen](../task/configure-calendar-1.md). For design considerations and user experience general guidelines when configuring your calendar screen, refer to the [Calendar screen](https://horizon.servicenow.com/native-mobile/screens/calendar-screen) section in the Horizon design system website.

-   **Swipe functions**

    Consider configuring swipe functions in the list view area to access quick actions like deleting a record or changing its state. For more information, see [Configure a calendar screen](../task/configure-calendar-1.md) and [Quick actions](../task/sg-config-quick-actions.md).

-   **Top menu actions**

    Consider configuring a top menu actions in the calendar screen for more complex or global actions, such as creating an appointment. For more information, see [Use your navigation function as a top menu selection](../task/sg-launcher-navigation-example-3.md).

-   **Template calendar card**

    Calendar cards are based on mobile cards. If you use the base system template named Calendar, avoid using the full date of the event, as it's already shown in the day's title.

-   **Cards from multiple tables**

    Calendar screens can display records from multiple tables. For a consistent experience, use similar card views for each record type shown in a calendar.

-   **Remote tables**

    When working with remote tables, it’s important to consider the performance implications. Efficient query design, indexing, and caching mechanisms should be employed to optimize performance.

-   **Start day of the week**

    By default, the first day of the week is Sunday. Users can change this option in the Settings area of their mobile app.


