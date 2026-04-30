---
title: Create a reservation in Microsoft Outlook add-in
description: Employees can create a workplace reservation in Microsoft Outlook. They can use the Workplace Reservation Management manifest add-in file for Microsoft Outlook add-in.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 10
breadcrumb: [Using Workplace Reservations for Microsoft Outlook Add-in, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a reservation in Microsoft Outlook add-in

Employees can create a workplace reservation in Microsoft Outlook. They can use the Workplace Reservation Management manifest add-in file for Microsoft Outlook add-in.

## Before you begin

Install and configure the following:

-   Workplace Reservation Management
-   Workplace Calendar Synchronization
-   Workplace Core
-   Workplace Case Management
-   Workplace Concierge
-   Indoor Mapping

Verify that you have completed the following Microsoft Outlook add-in manifest file configuration:

-   Add a manifest file for Microsoft Outlook add-in
-   Upload the manifest file in Microsoft Outlook Add-in. Depending on your usage, complete the following:

    -   Upload the manifest file for a single user
    -   Upload the manifest in Microsoft Outlook
    For more information, see [Activate the add-in for Microsoft Outlook](add-outlook-addin.md).


Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Open your mailbox in Microsoft Outlook to make a reservation.

2.  Perform any one of the following actions depending on the type of reservation that you want to make:

    -   To set up a meeting in Microsoft Outlook, open the calendar and select "New Event" or "New Meeting.”
    -   Complete the New Event form details in Outlook Calendar:
        -   New Event: Option to provide the meeting title or subject.
        -   Add Attendees: Add meeting attendees.Use **Optional** field to enter any optional meeting attendees.
        -   Date: Option to select a Date for your reservation.
        -   From: Option to select the start time of your reservation.
        -   To: Option to select the end time of your reservation.
        -   All day: Option to enable **All day** reservation. For more information, see [Configure Reservable Module for Microsoft Outlook](config-rsv-module-outlook.md).
        -   Add a location: Option to display the meeting location. The locations you select on the Make a reservation form on the Outlook side bar in Step 3 is added in this field option. You can also opt to end the location manually using this option.
        -   Use the **Scheduling Assistant** in Microsoft Outlook calendar to find a time that works for everyone and add a location or online meeting details.
3.  Select the **See more items** icon \(![See more items in outlook to select the Outlook add-in file.](../image/see-more-items-icon.png) from the Microsoft Outlook ribbon, and, select the reservation add-in manifest file.

    For example: **Workplace\_Outlook\_add\_in\_manifest\_example.xml**

    **Note:** When you open the add-in manifest file for the first time, the MOA OAuth login screen appears. Provide your instance login access credentials. When the manifest add-in file is opened for the first time, it takes some time to load and display the Make a Reservation form.

    ![WSD RSV MOA OAuth Registry](../image/outlook-moa-login-screen.png)

4.  Select **Allow**.

5.  The add-in opens in a sidebar and displays the Make a reservation form.

    Employees can search for a space and add locations for a given date and time. You can create multi-building reservations, neighborhood reservations, or make a reservation near your colleague. Employees can add workplace services to a reservation. They can edit a reservation or workplace services added to a reservation.

    ![The Make a reservation form page shown on the Calendar invite for employees to make a workplace reservation.](../image/outlook-make-rsv-first.png)

    Fill in the field information:

<table id="table_elj_w1w_fhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Option to select a Reservable Module type.For example: Meeting rooms

**Note:** Employees can only select a Reservable Module assigned to them by their administrator. For more information, see [Configure Reservable Module for Microsoft Outlook](config-rsv-module-outlook.md).

</td></tr><tr><td>

Where

</td><td>

Option to select a reservable path.-   **Browse all**
-   **Browse by area**
-   **Browse by neighborhood**
-   **Browse near a person**

For more information, see [Create a reservation](create-reservation-request-1.md).

**Note:** **Browse by Shift** Reservable path is available for Microsoft Outlook Add-in reservations.

</td></tr><tr><td>

Building

</td><td>

Select a building where you want to make the reservation.

</td></tr><tr><td>

Floor

</td><td>

Select a Floor.**Note:** If the Reservable Module Configuration option **Enable floor-based search** option isn’t configured by your administrator, this option to search by floors is displayed on the form. For more information, see [Configure Reservable Module for Microsoft Outlook](config-rsv-module-outlook.md).

</td></tr><tr><td>

Add another building

</td><td>

Select this option to add another building to your reservation. You can create multi-building reservations using this option.

</td></tr></tbody>
</table>6.  Select **Search** to search for a space.

    If the Auto-search option is enabled by your administrator, the Search button is not displayed and the spaces are fetched automatically for reservation.

    **Note:** Administrators can enable the auto-search by setting the **sn\_wsd\_rsv.enable\_auto\_search** system property to true. For more information, see [Properties installed with Workplace Reservation Management](../reference/properties-installed-with-wsd-reservation-mgmt.md).

    **Note:** If a selected room for a meeting invite or event has an email address configured to it, the search results shows only the room that is configured with the email configuration. For example, eureka@sncplatform.onmicrosoft.com. Microsoft Outlook doesn't show any other locations while you’re searching for spaces while making a reservation. For more information, see [Add a room using Workplace Space Management](../../workplace-space-management/task/add-a-room.md).

    ![Workplace Room showing mail configuration for the selected location.](../image/outlook-room-email-id.png)

7.  Select the **Filter** drop-down list to set filter criteria to search with the following criteria.

    -   Minimum capacity: Option to increase or decrease the space capacity.
    -   Services: Option to add services
    -   Purposes: Option to add location purposes.
    -   Floors: Option to include floor-based search in a selected building.
    Select **Clear all** to clear the filters.

    Select **Apply** to apply the filters.

8.  The search results are displayed on the **Card** view and **Map** view.

    Employees can select the Card or Map view to reserve a space.

9.  Select Card or Map view to view a space on the Card or Map view.

    **Note:** The Workplace Reservation Management by default assigns the following two views to a reservable module:

    -   **Card**
    -   **Schedule**
    **Map** view is only available when Indoor Mapping is active.

    1.  Card view: Select the **Card** tab. View and select a location or locations using the Card View.
    2.  Map view: Select the **Map** tab. View and select location or locations on the map.
        -   Floor: Select a **Floor**.
        -   Select a space on the map. The space details card is displayed. Select Add to add the space to your reservation.
        -   Legend: Select the toggle radio button to turn on or turn off the **Accessibility patterns**.

            ![Map legend showing the toggle button to activate accessibility on map.](../image/outlook-map-view.png)

10. Select the favorite icon \(![Favorite icon to favorite a space.](../image/favorite-icon.png)\) to favorite a space.

11. Select **Next**.

    A message is displayed if you try to reserve a space on your remote office day. The application gives you an option to update your remote day to in office presence day using the Presence dashboard.

    ![Employees trying to book a space on their remote presence days are shown a message "It looks like you are reserving a space on your remote work day."](../image/outlook-presence-message-remote-day.png)

    -   Select the URL link shown in the message to navigate to the Presence Dashboard and update your remote day to in office day. For more information, see [Set in-office days](../../workplace-concierge/task/set-in-office-days.md).![Presence dashboard showing calendar dates of your presence information. Change your remote days to in office to reserve a space in office.](../image/presence-dashboard-remote-days.png)

        Select the **Remote** drop-down list and select **In-office** or **Visit another office** as required.

        ![Presence Dashboard in Workplace Concierge showing option to convert your Remote days to In office or Visit another office.](../image/presence-dashboard-remote-to-office.png)

    -   On the Presence Dashboard, select the **Remote** day for a date that you were making reservation and change it to **In office** or **Visiting another office**.
    -   Select the **Make Reservation** tab.
    -   You’re redirected to the MOA Reservation Auth login page.
    -   Select **Allow** to access the Microsoft Outlook web portal.
    -   Make your reservation.
12. Add invites to your reservation.

    **Note:** You can invite your colleagues in Microsoft Outlook Outlook by using the invite list \(Invite attendees" or "Add required people"\). If you want to add guests, you need to include the guests to your invite in Microsoft Outlook and register them in Microsoft Outlook Add-in.

    ![Select invitees that you want to add to your workplace reservation.](../image/outlook-add-invitees.png)

13. Add external visitors to your reservation.

    ![Option to add external visitors to your reservation.](../image/outlook-add-invite-external-visitor-llink.png)

    On the form, select one of the following options to add a visitor:

    -   Previous visitor: Option to select a prior visitor.
    -   Add a new visitor: Option to add a new visitor.
    ![Select a visitor to add to your reservation.](../image/invite-external-visitor-add.png)

14. Select **Add extra services** drop-down list to add workplace services available for a location.

    Edit or remove workplace services as required. For example: Catering, space arrangement, projector, and so on.

    ![Catering services details form.](../image/outlook-add-services-catering.png)

    ![Add a space arrangement for a location. Select Chair layout from the list option for space arrangement.](../image/outlook-add-services-seat-arrangement-chair-layout.png)

    ![For chair arrangement services, select the Banquet style layout.](../image/outlook-chair-layout-details-banquet-stye.png)

15. Select **Submit Reservation**.

    ![Select Submit Reservation to make a reservation.](../image/outlook-submit-resv.png)

16. The Reservation Summary page is displayed.

    ![After submitting a reservation, the Reservation Summary page displays the reservation in Draft state.](../image/draft-state-of-reservation-rsv-summary-page.png)

17. Select **Actions** tab and select **Change Reservation details** from the drop-down list to edit or update your reservation.

    ![Draft reservation showing the Actions tab to update reservation, if required.](../image/outlook-update-rsv-details-message.png)

18. Edit Workplace Services or remove workplaces as required.

    While editing and updating a reservation to a new location, date, or time, the application shows the missing services message for services that are missing in your new updated location.

    ![While updating a reservation, if some services are missing from the updated location, date, or time, the application shows missing services message for few service items added to a reservation.](../image/missing-retain-extra-services-message.png)

19. Review the services that you want to retain before updating the reservation and select the **Retain Services** tab.

    The services are retained from the changed location to the updated location.

    ![Retain extra services tab to retain services from the changed location to the updated one.](../image/outlook-retain-extra-services-tab.png)

20. Select the **Update reservation details** tab or **Change location** to update changes to your location, date, and time.

    ![After modifying or updating your reservation, select the Update reservation details tab to update the changes.](../image/outlook-update-reservation-details-tab.png)

    "The service creation or update is currently in progress. Reservation details can’t be edited until the process is complete" message is displayed.

21. The updated reservation details are updated in the Reservation Summary page.

22. Select **Send** to send the meeting invite to invitees.

    **Note:** A Meeting invite when created in the Microsoft Outlook is in a **Draft** state. After it is sent to Microsoft Exchange Online, It takes some time for a meeting or reservation request sent from a client server to be synchronized with the Microsoft Exchange Online server. After it is synchronized, the reservation state changes to **Confirmation**.

23. Navigate to **All** &gt; **Workplace Reservation Management** &gt; **All Reservations**.

    Select your reservation to review the details on Workplace Reservation Management.

    If you have delegated access to a team member to create a reservation on your behalf, the All Reservations page shows the reservation details along with updated **Requested for** and **Opened by** column values.

    ![Workplace Reservations page showing meeting delegate and meeting organizer.](../image/delegate-fields-all-reservations-page.png). For more information, see [Delegate reservations in Microsoft Outlook add-in](outlook-delegate-rsv.md).


**Parent Topic:**[Using Workplace Reservations for Microsoft Outlook Add-in](../concept/using-outlook-addin.md)

**Previous topic:**[Using Workplace Reservations for Microsoft Outlook Add-in](../concept/using-outlook-addin.md)

**Next topic:**[Edit reservation details in Microsoft Outlook](outlook-edit-rsv.md)

