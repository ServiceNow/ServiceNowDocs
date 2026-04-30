---
title: Create bulk reservations in Workplace
description: Create bulk reservations in Workplace using the Workplace Service Delivery for Mobile. Employee can manage multiple planned reservations from the Workplace page.
locale: en-US
release: yokohama
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-23"
reading_time_minutes: 10
breadcrumb: [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Create bulk reservations in Workplace

Create bulk reservations in Workplace using the Workplace Service Delivery for Mobile. Employee can manage multiple planned reservations from the Workplace page.

## Before you begin

Create bulk reservations using the Workplace page. Select multiple days in the Schedule calendar view and reserve all selected days simultaneously. Check in or check out reservations, edit reservations, view reservation summary details, or cancel a reservation using Workplace. Manage your reservations and presence information using your mobile app. Change your **Remote** working days to **In-office** or **Visiting another office** presence days. Select your preferred space or desk. Add or edit workplace services to your reservations.

**Note:** The **sn\_wsd\_concierge.workplace\_day\_selection\_limit** property is configured by your administration for enabling multiple days selection on the Workplace page. This property when set to an integer value \(for example, 3, 5, and so on\) enables employees to select multiple dates or days on the calendar to make bulk reservations. For example, if this property is set to 5, employees can make bulk reservations and select only five dates or days on the calendar to make bulk reservations. For more information, see [Properties installed with Workplace Concierge](../../workplace-concierge/reference/properties-installed-with-workplace-concierge.md).

If the Reservable Module Configuration property **Max days in future** is set to 5 days by your administrator, and the **sn\_wsd\_concierge.workplace\_day\_selection\_limit** property is set to 6 by your Workplace administrator, employees can select only five dates or days on the calendar for making bulk reservations. The least minimal value is selected for default bulk days selection the calendar by the application.

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

    The location pin changes to a blue pin icon \( ![Blue pin location icon.](../images/wsd-mobile-location-pin-icon.png)\). The Workplace page opens for you to reserve your preferred workspaces, coordinate your workdays and collaborate with your preferred collaborators.

4.  Tap the **Select Multiple days** toggle button.

    Make bulk reservations or select multiple days on the calendar to make multiple reservations at once. When this toggle button is selected, users can select multiple days on the calendar for making reservations. When you turn on the toggle **Select multiple days** the calendar is expanded by default and shows a month view.

    **Note:** If the employee selects or manually enters past timings on the reservation page, it resets to the n-1 slot. For example, if the current time of building is 2:00 PM \(n\), the available time slots are from 1:30 PM \(n-1\) onwards. When you manually enter 1:00 PM in the Start time, the time is reset to 1:30 PM \(n-1\).

    Past dates are disabled on the calendar view and are not visible to workplace employees when the **Select multiple days** toggle button is selected. Only the current date and future dates are available for selection on the calendar.

    If the Workplace Concierge property \(**sn\_wsd\_concierge.allow\_overlapping\_reservations**\) is set to **Yes**, the dates on which you are already having an existing reservation are not disabled and displayed with a dot on the calendar. If this property is set to **No**, the reserved dates on the calendar are disabled and employees cannot select those dates. If overlapping reservations are allowed, the **In office** days are selected. This also includes exceptions when the employee plans to be in the office \(changing the Remote day to In-office day\) and when the employee is visiting another office. If overlapping reservations are not allowed, only allowed days indicated as **In office** are selected. This also includes exceptions where the employee is visiting another office.

    **Note:** If the sn\_wsd\_concierge.allow\_overlapping\_reservations property is set to **false** by your workplace administrator, you cannot create an overlapping or parallel reservations for a day. You can make only a single reservation for a day.

    **Note:** If you try to select a date which is labeled as **Remote**, the Remote day is changed to an **In-office** presence day and this record is updated in the Employee Presence Exceptions table \(**All** &gt; **Workplace Concierge** &gt; **Employee Presence** &gt; **Exceptions**\). The **Location** column in this table is updated with the building name that you using to reserve a space for your **In-office** day. For more information, see [Components installed with Workplace Concierge](../../workplace-concierge/reference/components-installed-with-workplace-concierge.md).

5.  Tap and remove dates from calendar that are selected by default and select few days of your choice.

    **Note:** You can only those number of dates on the calendar that is set by your administrator in the **sn\_wsd\_concierge.workplace\_day\_selection\_limit** property.

    If the user has no reservations for a selected day, a message appears 'You have no reservations for the this day".

    When there's no reservations for a selected workday, the application shows "You have no desk reservations for today." If you don't make a reservation, application shows "You have not made a reservation for this week's in-office day for \(&lt;date and month name&gt;\)''. If you select a remote day, application shows "You are working from home this day."

6.  In **Space suggestions** list view, review the suggested workspaces before making bulk reservations.

    ![Select multiple days toggle button is selected for employees to make bulk reservations.](../images/wsd-mobile-workplace-multiday-toggle-on.png)

    Application provides workspace suggestions based on the following employee preferences and usage:

    -   Past and future reservation data
    -   Frequently used desk or workspace
    -   Preferred locations
    -   Favorite spaces
    -   Preferred workplace services
    -   Preferred collaborators
    ![Space card showing the Show on map to find your space on the map.](../images/wsd-workplace-mobile-space-suggestion-get-directions.jpeg)

    The tags displayed on a suggested space is fetched from the Space Suggestion configuration table. These tags are displayed on the Space Suggestions card. For example, **Reserved frequently**, **Near your location**, **Your favorite**, and so on. When an employee is visiting another office, the suggestions are provided from the office that an employee is visiting and is not based on the employees in-office preferences set in the Presence dashboard. For more information, see [Space suggestion Configuration](../../workplace-concierge/task/space-suggestion-configuration.md) and [Properties installed with Workplace Concierge](../../workplace-concierge/reference/properties-installed-with-workplace-concierge.md).

7.  To update or change a suggested workspace from Space Suggestions, select the **Suggest another** refresh button icon \(![Select the refresh button to suggest another workspace.](../images/wsd-mobile-refresh-icon-workplace-suggestion.png)\).

    ![Option to review your space suggestions again or select the Search all spaces option from the Make a reservation page.](../images/wsd-mobile-workplace-search-all-spaces-new.png)Application shows the available spaces in a building. At a time, the application shows 10 maximum suggestions when an employee taps and selects the refresh button repeatedly. After the tenth attempt, the application shows a message, " Still looking for a space that fits your requirements? Click here to review suggestions again." Selecting **Click here to review suggestions again** displays a list of new workspace suggestions.

    **Note:** If there are no available spaces based on employee preferences, the **Suggest another** refresh option can also show a single space or few spaces \(and not the 10 preferred available spaces always\).

    To review previous suggestions, tap and select "Click here to review suggestions again".

8.  Select **Search all spaces** if you don't find the workspace that you are looking for.

    Selecting **Search all spaces** opens the Make a reservation page on your mobile app. If you want to reserve a space than what is suggested in the Space Suggestions card, use the Make a reservation page to reserve a space.

9.  Select **Reserve Selected days** to reserve multiple spaces shown in the Space Suggestions card.

10. Tap and select **Clear selected days** to remove a selected date or dates from the calendar before making bulk reservations.

    You can also clear selected dates by tapping the selected dates on the calendar. When you tap a date, the date is removed from your selection and space suggestions are not shown for the unselected dates.

11. Tap the **Reservations** tab to view all your reserved spaces in an Agenda view.

    The Agenda view shows all your existing reservations. It shows all reservations that you have made using the Advanced Reservation portal and reservations created using the mobile app.

12. Tap a reservation on the Agenda view and select the more information icon \(![More information icon.](../images/wsd-mobile-three-dots-icon.png)\) to open the Actions menu.

    ![Agenda view showing your reservations and types of reservations available for you.](../images/wsd-mobile-workplace-agenda-view.jpeg)

    Reservation timings are based on the **All day**Reservable module configuration set by your administrator. When **All day** is enabled and **All day meaning** is set to **Full day**, you can make a reservation for full day \(one day or entire day based on your building timezone\). For Example, reservation timings is shown from 10.25 to 23.59 based on your office full day time zone settings. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

13. Review the different types of reservations that you have made in the Agenda view.

    The reservations from both Reservation portal and mobile application is shown in the Agenda view. It also shows the labels for different type of reservations. For example, **Group**, **All day**, **recurring \(multi-day\)**, **multi-building**, **neighborhood**, and so on. **All day** reservations are shown on the top and then other types of reservations are shown in the Agenda view.

    ![Agenda view showing reserved spaces for group reservations and all day.](../images/wsd-mobile-workplace-group-rsv-desks-use.png)

14. Select the Actions menu items to complete the following:

    1.  Select the Actions menu icon \(![Actions menu icon.](../images/wsd-mobile-three-dots-icon.png)\)adjacent to a reservation in the Agenda view to open the Actions menu.

    2.  The Actions menu shows the following options:

        -   Check in or Check out
        -   Cancel Reservation
        -   Edit Reservation
        -   View reservation information
        -   Show on map
        ![Selected reserved space card showing the Actions menu items.](../images/wsd-mobile-workplace-space-card-actions-items.png)

    3.  Select **Check-in** to check in a reservation.

        After a reservation is checked in, you see the **Check out** option to check out your reservation.

    4.  Select **Edit Reservation** to edit a location, date and time for your reservations.

        ![Edit reservation dialog box.](../images/wsd-mobile-workplace-edit-dialog-box.png)

        Update your reservations to remove or edit workplace services using the Update reservation details page. For more information, see [Review and edit your reservations in Workplace](mobile-workplace-edit-rsv.md).

    5.  Select **Cancel Reservation** to cancel a reservation.

        Employees can directly cancel a reservation if the reservation doesn't require cancel notes. The option to add a cancel note is set by your administrator in the Reservable Module Widget Configuration. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

        ![Cancel Reservation dialog box.](../images/wsd-mobile-workplace-cancel-rsv-use.jpeg)

        Select **I want to add/edit/remove items instead** to update workplace items in a reservation.

        The option to add a cancel note is set by your administrator in the Reservable Module Widget Configuration. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

    6.  Select **View reservation Information** to review the Reservation summary for a selected space.

        ![Reservation Summary page showing the Actions menu item.](../images/wsd-mobile-workplace-action-button-agendaview.png)

    7.  Select **Show on map** to open the location directory page and reserve a space using a floor map.


**Parent Topic:**[Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../concept/workplace-preference-schedule.md)

**Related topics**  


[Manage your in-office presence preferences](workplace-preferences-emp-center.md)

[Create a reservation for a day in Workplace](manage-schedule-emp-center.md)

[Review and edit your reservations in Workplace](mobile-workplace-edit-rsv.md)

