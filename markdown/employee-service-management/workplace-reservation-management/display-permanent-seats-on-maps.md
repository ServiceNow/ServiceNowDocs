---
title: Display permanent seat assignments on floor maps
description: Display permanent space assignments along with employee names on maps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/display-permanent-seats-on-maps.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 8
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Display permanent seat assignments on floor maps

Display permanent space assignments along with employee names on maps.

## Before you begin

Verify that you’ve installed the following to display permanent seating assignment on the map:

-   Indoor Mapping
-   Workplace Space Mapping
-   Workplace Case Management

Employees must have a dedicated workspace allocation in their workplace profiles. Permanent seats along with employee names are displayed on the map based on the following considerations:

-   If an employee is assigned two or more workspaces, then only the primary work location is displayed on the map.
-   If privacy settings are enabled for an employee, the employee name isn’t displayed on the floor map. Selected space shows **Private user**.
    -   If two employees are sharing a space with privacy settings enabled, the floor map for a selected space doesn’t show the employee name but shows **Private user**.
    -   If two employees are sharing a space and only one of them has the privacy settings enabled, the floor map shows **Private user** for the employee who has privacy enabled.

Role required: admin

## Procedure

1.  To enable permanent seat assignment display on the floor maps, enable the following map property and place type field options:

    1.  Navigate to **All** &gt; **Space Mapping** &gt; **Map properties.**.

    2.  Select the edit page option on the Map properties page.

    3.  Select **Enable display of permanent seat assignments on map** \(sn\_wsd\_space\_map.display\_seat\_assignment\).

        **Note:** This property is displayed in the Map properties menu only when the Workplace Indoor Mapping plugin is installed.

    4.  Select **Yes** to enable the property.

        Activating this property to display permanent seat assignments along with employee names on floor maps. By default, this property is set to **No**.

2.  Navigate to **All** &gt; **Workplace Reservation Management**.

    1.  The following web application widgets display the permanent seat assignments on a map:

        -   Make a reservation
        -   Space Details
        -   Location Directory
        -   General request \(Order something\)
3.  On the Make a reservation page, perform the following steps:

    For more information about how to make a reservation or update an existing reservation, see [Create a reservation]().

    1.  Select a location and building.

    2.  Select a space from the search result.

    3.  Select **Map view**.

    4.  On the map, select a floor from the **Floor** drop-down list.

    5.  Zoom in to display spaces.

    6.  On the map, select the **gear settings icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: gear settings to display the map setting options\)**.

    7.  Enable the **Display employees permanent seat assignments on floor maps** toggle button.

    8.  Select **Apply**.

        The map shows permanent seat assignments for employees along with their names.

4.  From the Reservation Portal home, select the **Location Directory** widget.

    You can access the Location Directory widget from the Employee Center portal. Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Workplace Services** &gt; **Site Safety** &gt; **Location Directory**.

    1.  On the Interactive floor map, select a location and floor from the drop-down options.

    2.  Zoom in to see spaces or permanent seating assignments for employees.

    3.  On the map, select the **gear settings icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: gear settings to display the map setting options\)**.

    4.  Enable the **Display employees permanent seat assignments on floor maps** toggle button.

        Employee names along with their assigned seats are displayed for a selected space.

5.  Navigate to **All** &gt; **Self-service** &gt; **Employee Center** &gt; **Workplace Services** &gt; **General Request** to browse the workplace service catalog and request workplace services.

    1.  On the General Request form, fill in the request details and select the clickable link **Find the space on a floor map**.

        Select a space and open the **Find the space on a floor map** link to view an interactive floor map.

        -   Request a desk change.
        -   Request furniture.
        -   Submit a general request.
    1.  Select **Request a desk change**.

    2.  Complete the steps for a move request.

        For more information, see [Raise a move request for a space change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/request-desk-change.md).

    3.  Select the **Find the space on a floor map** link.

    4.  Select a building and floor on the interactive floor map.

    5.  Zoom in and select a space.

    6.  On the map, select the **gear settings icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: gear settings to display the map setting options\)**.

    7.  Enable the **Display employees permanent seat assignments on floor maps** toggle button.

        Employee names along with their permanent seats are displayed for a selected space.

    1.  Select **Request a furniture.**

    2.  Complete the steps for ordering furniture or equipment.

        For more information, see [Request furniture for a space](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/request-furniture.md).

    3.  Select the **Find the space on a floor map** link.

    4.  Select a building and floor on the interactive floor map.

    5.  Zoom in and select a space.

    6.  On the map, select the **gear settings icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: gear settings to display the map setting options\)**.

    7.  Enable the **Display employees permanent seat assignments on floor maps** toggle button.

        Employee names along with their assigned seats are displayed for a selected space.

    1.  Select **Submit a general request.**

    2.  Complete the steps for submitting a general workplace service request.

        For more information, see [Raise help request for a workplace inquiry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/submit-gen-workplace-serv-req.md).

    3.  Select the **Find the space on a floor map** link.

    4.  Select a building and floor on the interactive floor map.

    5.  Zoom in and select a space.

    6.  On the map, select the **gear settings icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: gear settings to display the map setting options\)**.

    7.  Enable the **Display employees permanent seat assignments on floor maps** toggle button.

        Employee names along with their assigned seats are displayed for a selected space.

6.  Navigate to the My favorites page from the Employee Center page.

    1.  Select a favorite space or navigate to **Workplace services** &gt; **Quick Links** &gt; **Create reservation**.

    2.  To make a reservation, enter the required information.

        For more information, see [Set a location as favorite using the Space details page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/set-a-location-as-favorite.md).

    3.  Select **Map view**.

    4.  On the map, select the **gear settings icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: gear settings to display the map setting options\)**.

    5.  Enable the **Display employees permanent seat assignments on floor maps** toggle button.

        Employee names along with their assigned seats are displayed for a selected space.


**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Assign spaces to an area]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a reservable view]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Create a quick reservation time slot]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Microsoft Teams]()

[Connect Workplace Reservation Management with Zoom]()

[Display name of the person reserving a space]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

