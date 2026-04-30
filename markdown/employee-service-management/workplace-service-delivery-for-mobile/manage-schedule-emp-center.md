---
title: Create a reservation for a day in Workplace
description: Reserve your preferred workspace in Workplace using the Workplace Service Delivery for Mobile app.
locale: en-US
release: yokohama
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-20"
reading_time_minutes: 12
keywords: [Workplace service delivery for mobile, workplace schedule, desk suggestions, preferred location]
breadcrumb: [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Create a reservation for a day in Workplace

Reserve your preferred workspace in Workplace using the Workplace Service Delivery for Mobile app.

## Before you begin

View your workday presence schedule, office as well as remote days in the schedule calendar.

Employees can plan their hybrid workplace schedule and modify workplace presence preferences \(in-office, Remote, and visiting another office\) in Workplace Service Delivery for Mobile. Employees can view their preferred in-office days and get insights on their preferred collaborators. They can reserve a space by selecting their preferred workspace and collaborators.

Get insights on workplace collaborators who plan to be in office on the days when you are in office. Change your workplace preferences and workplace presence information as and when required to maximize workplace productivity and collaboration. If no collaborators are available in your in-office days, update your in-office presence days to match it along with that of your preferred collaborators.

Make sure that you have the following applications:

-   Workplace Service Delivery for Mobile
-   Workplace Core
-   Workplace Reservation Management
-   Workplace Concierge
-   Indoor Mapping
-   Workplace Central
-   Workplace Space Management
-   Workplace Space Mapping

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Log in to the Now Mobile® app.

2.  Access your Workplace Service Delivery for Mobile instance.

3.  Tap and select the **Workplace** location pin icon \(![workplace location pin launch icon.](../images/wsd-mobile-location-pin-without-color.png)\) from the mobile home page.

    The location pin changes to a blue pin icon \( ![Blue pin location icon.](../images/wsd-mobile-location-pin-icon.png)\). The workplace screen appears for you to coordinate your workdays and collaborate with your preferred collaborators.

4.  Tap and select a date labeled as **In-office** day on the calendar to make a reservation.

    The Schedule calendar view shows the current date as selected by default. The text label **Today** is displayed for the current date of a month. When you select a future date,the label for **Today** is inactive. This label is not available for making bulk reservations.

5.  On the **Schedule** calendar view, make the following changes as required:

    If you have an existing reservation for a selected date, the date is shown with a dot on the calendar. By default, the current week, day, and month is selected on the calendar.

    ![Workplace showing options to make a single day reservation.](../images/wsd-mobile-workplace-single-day-rsv.jpeg)

    1.  View your in-office, remote workday schedule for a week on the calendar.

        The calendar view shows your hybrid workday schedule \(In-office, Remote\). Use the chevron buttons on the calendar to toggle between different calendar views \(Day, Week, and Month\). Adjust your calendar view as required.

        -   Use the chevron next button \(![Use the chevron next button to scroll to the next month or future months in a calendar.](../images/wsd-mobile-chevron-forward.png)\) to view the next or future week when you are in a week view on the calendar. To view the next month in a calendar, expand the calendar and tap the next button. By default, the calendar view is collapsed to show only a week view.
        -   Use the chevron previous button \(![Use the chevron previous or backward button to go back to the previous month or past months.](../images/wsd-mobile-chevron-backward.png)\) to go back to the previous week or weeks.
        -   Use the chevron expand button \(![chevron button to collapse the calendar view.](../images/wsd-mobile-chevron-down.png)\) to expand the calendar view for a month if it is in a collapsed state \(shows only a week view for a selected month when collapsed\).
    2.  Change your workplace presence information from **In-office**, **Remote**, or **Visiting another office**.

        The application fetches presence information from the Employee presence configuration. For information, see [Set Employee Presence](../../workplace-concierge/concept/use-workplace-concierge.md). This option is not available for creating bulk reservations.

        **Note:** If you try to select a date which is labeled as **Remote**, the Remote day is changed to an **In-office** presence day and this record is updated in the Employee Presence Exceptions table \(**All** &gt; **Workplace Concierge** &gt; **Employee Presence** &gt; **Exceptions**\). The **Location** column in this table is updated with the building name that you using to reserve a space for your **In-office** day. For more information, see [Components installed with Workplace Concierge](../../workplace-concierge/reference/components-installed-with-workplace-concierge.md).

        -   **In-office**: Option to indicate your in-office presence or days when you are working from office. For example, if you change your In-office presence day to Remote, the changed location message is displayed.

            ![Workplace showing cancel exception message for you to revert back your presence information using the presence drop-down list.](../images/wsd-mobile-workplace-cancel-exceptions.png)

            Select **Cancel exception** to revert back the changes that you made to your workday presence schedule. Revert back to **In-office** from **Remote**. A message is displayed "Exception canceled".

        -   **Remote**: Option to indicate that you are working remotely or from home. When you select a remote day on the calendar, application shows the message "You are working from home this day".

            For example, if you change your preference from Remote to In office, application shows the message 'Location changed."

        -   **Visiting another office**: Option to indicate that you are in office but visiting another office.

            When you try to change a remote or in-office day to Visiting another office, the change location dialog box opens. You can search and select a new location. Select **Change Location** to update a new location.

            ![Option to select the default preferred location while visiting another office. You can search and select a new location.](../images/wsd-preference-visiting-another-location-change.jpeg)

6.  Tap and select **Change preferences** to change your workplace preferences.

    The In-office preferences page opens for you to update your in-office days. Change or modify your location, collaborators, and workplace services as required. For more information, see [Manage your in-office presence preferences](workplace-preferences-emp-center.md).

7.  In **Space suggestions**, review the suggested building, floor, and a space.

    By default, the **Space suggestions** card displays your preferred desk or space. If you want to reserve a different location or space than what is suggested to you, application fetches other locations from the search results shown on the reservation portal.

    If the user has reservations on a selected day, following information is shown in the suggested workspace card;

    -   Reservation time based on building time zone and location.
    -   Reservation status \(Confirmed, Completed, Awaiting confirmation, and so on.\)
    -   Space Name
    -   Campus, Building, and Floor name.
    -   Time. The reservation time depends on the reservation system property for start time \(sn\_wsd\_rsv.day\_start\) and end time \(sn\_wsd\_rsv.day\_end\). The reservation time depends on the building time zone.
    -   Reservable module name: Desks.
    -   Capacity: Meeting room capacity.
    -   Standard services and Location purposes
    -   Workspace Image \(if the workspace has an image associated with it\)
    ![Space Suggestions card showing](../images/wsd-mobile-workplace-space-suggestions-card.png)

    ![Space card showing the Show on map to find your space on the map.](../images/wsd-workplace-mobile-space-suggestion-get-directions.jpeg)

    Application provides workspace suggestions based on your past and future reservation data, frequently used desk or spaces, preferred locations, favorite spaces, preferred workplace services, and preferred collaborators. The Suggestion tags you have added to the Space Suggestion configuration table is displayed on the Desk suggestions card. For example, **Reserved frequently**, **Your favorite**, and so on. When an employee is visiting another office, the suggestions are provided from the office that an employee is visiting and is not based on the users in-office preferences. For more information, see [Space suggestion Configuration](../../workplace-concierge/task/space-suggestion-configuration.md) and [Properties installed with Workplace Concierge](../../workplace-concierge/reference/properties-installed-with-workplace-concierge.md)

8.  To update or change a suggested workspace from Space Suggestions, select the **Suggest another** refresh button icon \(![Select the refresh button to suggest another workspace.](../images/wsd-mobile-refresh-icon-workplace-suggestion.png)\).

    Application shows the available spaces in a building. At a time, the application shows 10 maximum suggestions when an employee taps and selects the refresh button repeatedly. After the tenth attempt, the application shows a message, " Still looking for a space that fits your requirements? Click here to review suggestions again." Selecting **Click here to review suggestions again** displays a list of workspace suggestions.

    **Note:** If there are no available spaces based on employee preferences, the **Suggest another** option can also show a single space or few spaces \(and not 10 preferred available spaces always\) when an employee selects the refresh button.

    ![Space Suggestions showing the review suggestions again and the Search all spaces option.](../images/wsd-mobile-workplace-search-all-spaces-new.png)

    To review previous suggestions, tap and select "Click here to review suggestions again".

    Select **Search all spaces** if you are don't find the workspace that you are looking for. Selecting **Search all spaces** opens the Make a reservation screen on the mobile app. For more information, see [Make a reservation using the Now Mobile app](make-a-reservation-on-mobile.md).

9.  Select **Reserve** to reserve a space for a selected date and time on the Make a reservation page.

    **Note:** If the sn\_wsd\_concierge.allow\_overlapping\_reservations property is set to **false** by your administrator, you are not allowed to create an overlapping or parallel reservations for a day. You can make only a single reservation for a day.

    ![Make a reservation screen on the WSD mobile application to create a reservation.](../images/wsd-mobile-adv-reservation-portal.jpeg)

    If the user has no reservations for a selected day, a message appears 'You have no reservations for the this day".

    When there's no reservations for a selected workday, the application shows "You have no desk reservations for today." If you don't make a reservation, application shows "You have not made a reservation for this week's in-office day for \(&lt;date and month name&gt;\)''. If you select a remote day, application shows "You are working from home this day."

    Reservation timings are based on the **All day**Reservable module configuration set by your administrator. If **All day** is enabled and **All day meaning** is set to **Full day**, you can make a reservation for full day \(one day or entire day based on your building timezone\). For Example, reservation timings is shown from 9.00 am to 5.00 pm based on your office work day start time and end time reservation properties. settings. For more information, see [Properties installed with Workplace Reservation Management](../../wsd-reservation-management/reference/properties-installed-with-wsd-reservation-mgmt.md).

10. Tap the **Reservations** tab to view your reservations in an Agenda view.

    The Agenda view shows all your existing reservations. It shows reservations that you have made using the Advanced Reservation portal and reservations created using the mobile app. It also shows the labels for different type of reservations you have made like Group, All day, recurring \(multi-day\), multi-building, neighborhood, and so on.

11. Tap a reservation on the Agenda view and select the more information icon \(![More information icon.](../images/wsd-mobile-three-dots-icon.png)\) to open the Actions menu.

    ![Agenda view showing your reservations and types of reservations available for you.](../images/wsd-mobile-workplace-agenda-view.jpeg)

    It also shows the labels for different type of reservations you have made like **Group**, **All day**, **recurring \(multi-day\)**, **multi-building**, **neighborhood**, and so on. **All day** reservations are shown on the top and then other types of reservations are shown in the Agenda view.

    ![Agenda view showing reserved spaces for group reservations and all day.](../images/wsd-mobile-workplace-group-rsv-desks-use.png)

12. Select the Actions menu items to complete the following:

    1.  Select the Actions menu icon \(![Actions menu icon.](../images/wsd-mobile-three-dots-icon.png)\)adjacent to a reservation in the Agenda view to open the Actions menu.

    2.  The Actions menu shows the following options:

        -   Check in or Check out
        -   Cancel Reservation
        -   Edit Reservation
        -   View reservation information
        -   Show on map
        ![Selected reserved space card showing the Actions menu items.](../images/wsd-mobile-workplace-space-card-actions-items.png)

    3.  Check-in or Check-out: Select **Check-in** to check in a reservation.

        After a reservation is checked in, you see the **Check out** option to check out your reservation.

    4.  Select **Edit Reservation** to edit location, date and time for your reservations.

        Update your reservations to remove or edit workplace services using the Update reservation details page. For more information, see [Review and edit your reservations in Workplace](mobile-workplace-edit-rsv.md).

        ![Edit reservation dialog box.](../images/wsd-mobile-workplace-edit-dialog-box.png)

    5.  Select **Cancel Reservation** to cancel a reservation.

        Employees can directly cancel a reservation if the reservation doesn't require cancel notes. The option to add a cancel note is set by your administrator in the Reservable Module Widget Configuration. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

        ![Cancel Reservation dialog box.](../images/wsd-mobile-workplace-cancel-rsv-use.jpeg)

        Select **I want to add/edit/remove items instead** to update workplace items in a reservation.

    6.  Select **View reservation Information** to view Reservation summary for a reserved space.

        ![Reservation Summary page showing the Actions menu item.](../images/wsd-mobile-workplace-action-button-agendaview.png)

13. Tap and select the **Insights** tab to view your collaborators and get insight on their in-office days.

    Match your In-office days with that of your collaborators to maximize productivity and collaboration. The application fetches your preferred collaborators information from the Employee presence configuration. For information, see [Set Employee Presence](../../workplace-concierge/concept/use-workplace-concierge.md).

    Application shows the following information for your preferred collaborators:

    -   The number of collaborators who plan to be in office while you are visiting office
    -   View details of collaborators who are visiting another office in your in-office day.
    -   Collaborators who are working remotely on your in-office day
    If there are no collaborators for a selected in office day, application shows "None of your collaborators plan to be in office on this day."

    ![Your in-office days insights and collaborators information.](../images/wsd-mobile-collaborators-insights.jpeg)

    ![Select View to view your preferred collaborators workday schedule.](../images/wsd-mobile-view-collaborators.jpeg)

14. Review your in office days insights for a selected date.

    If all your preferred collaborators are planning to be in office on your in-office day, application shows "100% of your collaborators plan to come to the office". For days when you are working from home or remotely, application shows "No insights present for this date."


**Parent Topic:**[Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../concept/workplace-preference-schedule.md)

**Related topics**  


[Manage your in-office presence preferences](workplace-preferences-emp-center.md)

[Create bulk reservations in Workplace](mobile-workplace-bulk-reservations.md)

[Review and edit your reservations in Workplace](mobile-workplace-edit-rsv.md)

