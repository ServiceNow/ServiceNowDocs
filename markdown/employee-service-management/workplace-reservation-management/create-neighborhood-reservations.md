---
title: Create neighborhood reservations
description: Reserve neighborhood spaces using Advanced reservation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/create-neighborhood-reservations.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create neighborhood reservations

Reserve neighborhood spaces using Advanced reservation.

## Before you begin

The option to reserve neighborhood spaces is available only if your administrator has enabled the **Enable browse by neighborhood** option on the Reservable Module Configuration. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

The employee can see and select neighborhoods on the reservation portal only when:

-   The employee is assigned to the neighborhood, and the neighborhood is restricted.
-   The employee is assigned to the neighborhood, and the neighborhood is not restricted.
-   The neighborhood is not restricted and the employee is not assigned to it.

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Select any of the following context menu navigation options to make a neighborhood reservation.

<table id="choicetable_prt_yr3_smb"><thead><tr><th align="left" id="d753265e86">

Location

</th><th align="left" id="d753265e89">

Steps

</th></tr></thead><tbody><tr><td id="d753265e95">

**Application navigation filter**

</td><td>

Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

</td></tr><tr><td id="d753265e119">

**From Employee Center Portal**

</td><td>

-   Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
-   On the Employee Center portal, select **Workplace Services** &gt; **Browse Workplace Services**.
-   Select the **New general reservation** card.

Make a reservation portal page opens for you to make workplace reservations.

-   Another way to make reservation is to use chat icon. On the home page, select the chat icon \(\[Omitted image "chat-icon.png"\] Alt text: Chat icon.\). To make a reservation, enter your question or select **Show Me Everything** to select from the list of available options.

</td></tr></tbody>
</table>    The Make a Reservation page opens in a new tab.

2.  Select a Reservable Module configuration.

    For example, select any of the following Reservable Module configuraiton. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

    -   Desks
    -   Desks with an Area
    -   Meeting rooms require approval
    -   Meeting rooms
    -   Desks with a shift
3.  To search for reservable spaces in a neighborhood, select **Browse by Neighborhood**.

    **Note:** The **Browse by Neighborhood** option is only available if the **Enable browse by neighborhood** option is selected on the Reservable Module configuration page. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

4.  Complete the following information.

    Fill in the form fields.

<table id="table_mn3_3gf_xdc"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Building

</td><td>

Name of the building for a selected campus. Select a building from the list. For example, Demo Campus.The building names and location names are alphabetically sorted or sorted according to the **Order** that you have configured on the Buildings and Regions tables. When a sort **Order** is configured for a building or region, the building names and locations are sorted accordingly. If the sorting **Order** value isn’t specified for an item, the items are listed on top of the list \(ascending order\), and sorted alphabetically. The building names and location names are alphabetically sorted based on the label name. For example Building A, Building B, and so on.

</td></tr><tr><td>

Floor

</td><td>

Floor of a building where you want to make a reservation.The floor names are either alphabetically sorted or the values are sorted based on the indicated sort order. You can configure the sort **Order** in the Floors table. If the sorting **Order** value is not specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The Floor names are alphabetically sorted based on the names and labels.

</td></tr><tr><td>

From**Note:** The time directive fields \(From, time, To\) are also available on the MESP \(Mobile Employee Service Portal\) on the Now Mobile app.

</td><td>

Start date of your reservation. For a single day reservation, only the **From** field is shown and not the option to enter the end date.-   Employees can't select a date and create a reservation if the start date exceeds the Max days in future Reservable module value. Thisn’t value is configured on the Reservable module by your administrator. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

When the Max days in future value is configured by your administrator, you can’t select a date past the max allowed date. The dates in the calendar date picker are inactive for dates that are too far in future.

**Note:** If the Max days in future value isn’t configured, the date selection isn’t restricted. Date selection is based on the Max number of occurrences value. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

-   If you enter an invalid date which is greater than what is specified in the **Max days in future** value, the application resets the date to the current date.


</td></tr><tr><td>

Time

</td><td>

Start time when the reservation begins. Employees can select time using the drop-down list or by entering the time in the field. The time increment value depends on the value set by your administrator. Default reservation time duration available for selection is 30 minutes.The **time\_picker\_interval\_size** property for reservation start time and reservation end time is configured using the Service Portal Widget instances. The start time field increment value depends on the value set in the **time\_picker\_interval\_size**. Default reservation time increment value duration is 30 minutes.

**Note:** You can’t select a date that occurs in the past. The time for a selected location depends on the building time zone.

</td></tr><tr><td>

To

</td><td>

End date of your reservation.Employees can't select a date and create a reservation when the End date exceeds the Max days in future value. The Max days in future value specifies the maximum number of the days in the future up to which the Reservable module can be reserved.

**Note:** In the case of a single day reservation, option to enter the end date isn’t available.

If you enter an invalid date which is greater than what is specified in the **Max days in future** value, the application resets the date to the current date.

**Note:** If the **Max days in future** value isn’t enabled, then the date selection isn’t restricted and is based on the **Max number of occurrences** value configured in the Reservable module. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

</td></tr><tr><td>

Time

</td><td>

End time when you would stop using the workplace item. Employees can select the end time using the drop-down list or by entering the time in the field. The end time increment value depends on the value set by your administrator. Default reservation end time duration is 30 minutes. The **time\_picker\_interval\_size** property for reservation start time and reservation end time is configured using the Service Portal Widget instances. The start time and end time field increment value depends on the value set in the **time\_picker\_interval\_size**. Default reservation time increment value duration is 30 minutes.

**Note:** You can’t select a date that occurs in the past. For example, If the start time is 09:00, you can select an end time after this duration. You can’t select a time before 09:00 on the same day. The time for a selected location depends on the building time zone.

</td></tr><tr><td>

Recurring

</td><td>

Option to reserve the workplace items on a recurring basis. Specify the number of days and the number of times that you want to repeat the reservation in a recurring series.For weekly reservations, select the days of the week for the reservation. The Recurring option is displayed based on the configuration that your admin has set. Also, if there are any recurring reservation conflicts, they’re auto-resolved if your admin has configured the same.

Auto-resolve recurring conflicts&lt;/uicontrol&gt; option is enabled on the Reservable module form. The application tries to auto-resolve recurring reservation conflicts. For more information, see [Auto-resolve recurring reservations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/recurring-reservations.md).

**Note:** Adding extra services option isn’t available for Recurring reservations.

</td></tr><tr><td>

All day

</td><td>

Option to reserve the workplace item for an entire day or a single day. This option appears if your Workplace administrator has enabled the All day reservation setting on the selected **Type**. The start and end times of the reservation depend on the timings set by your organization. The **All day** option is also available on the Space details page. **Note:** The **All day** option's appearance depends on your administrator's configuration. If your admin has mandated all day reservation for a selected **Type**, the reservation is automatically made for the entire day. In case of All day you can only modify the Start date of the reservation.

</td></tr><tr><td>

Add another building

</td><td>

Reserve multiple workplace items spanning multiple buildings. The buildings time zones are different for a same date and time in a reservation.**Note:** This option is available if you have selected **Allow multiple reservations** check box on the **Reservable Module** &gt; **Reservable Module Configuration** tab. For more information, see [Create multi-building reservations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-multi-building-reservation.md).

</td></tr></tbody>
</table>5.  

6.  Click **Search**.

    The available spaces in a neighborhood are displayed.

    **Note:** Space admins or space planners determine if employees are permitted to view the neighborhoods on the location directory.

7.  From the Search results, select **Add** to add a reservable space.

8.  Switch between the **Card view** and **Schedule view** tabs to review and select the available spaces.

    In the schedule view for a selected building, you see the applicable date and time.

    The bottom pane shows the number of items that you've selected from the search results.

9.  Select the **Map view** tab if your organization is using Indoor Mapping for interactive locations and wayfinding.

    The floor map shows the neighborhood spaces based on the availability and employee assignment.

10. Click **Next**.

    Verify the reservation details for selected spaces.

11. Select **Add Services** to add room configurations or catering for selected spaces.

12. Review the Reservation Summary details.

13. Click **Submit Reservation**.

    If any of the items don't require approval, the selected workplace items are reserved. The status of the request is updated to **Confirmed**. If any of the items need approval, your request is submitted for approval. The status of the request is updated to **Awaiting approval**.


**Parent Topic:**[Reserve workplace items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/reserve-workplace-items.md)

**Related topics**  


[Create a reservation]()

[Add invitees as collaborators and create a reservation]()

[Auto-resolve recurring reservations]()

[Set a location as favorite using the Space details page]()

[Reserve a space near your colleague]()

[Create a multi-day reservation]()

[Create multi-building reservations]()

[Create reservation for multiple workplace items]()

[Enable shift-based reservation]()

[Create a reservation along with a shared reservation]()

[Create a reservation including a virtual meeting link]()

[Create a shift reservation]()

[Create a group reservation]()

[Share, modify, or cancel a reservation]()

[Reserve a workplace using the Quick Reservation widget]()

[Download an iCalendar for a reservation]()

