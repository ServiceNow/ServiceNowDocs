---
title: Create a flexible service
description: Create a flexible service and provide it as an extra service to employees. Employees can use the flexible service and other basic standard services when they make a reservation.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a flexible service

Create a flexible service and provide it as an extra service to employees. Employees can use the flexible service and other basic standard services when they make a reservation.

## Before you begin

**Warning:** Starting with Workplace Reservation Management version 2.1.2, you cannot create any extra services or flexible services directly using the Workplace Reservation Management application. Beginning from Workplace Reservation Management version 2.1.2, you can create an extra service only as a workplace service using the Workplace Case Management application only. The Workplace Case Management application is automatically available for installation after the upgrade. If you have installed Workplace Reservation Management version 2.1.2 or above directly \(as a first time user\), there will be no impact and the following conditions does not apply to you.

-   After the upgrade, the existing flexible services are removed from the Workplace Reservation Management application and are listed as workplace services in the Workplace Case Management application.

    For more information on how to create an extra service after the upgrade, refer to [Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md).

-   Each category of a flexible service is created as a workplace service. The flexible services that belonged to that category are created as Workplace Service Items of that workplace service.
-   The locations to which the flexible services were available are listed in the Workplace Service Item Locations Related list of that workplace service.
-   There is no effect to employee experience on the Reservation portal.
-   All the extra services requested by employees along with their reservation in the past six months are restored automatically. The extra service requests are logged in the Requested Service Items \[sn\_wsd\_case\_service\_item\_request\] table of the Workplace Case Management application.
-   To migrate the subcategories and to create the case and task templates automatically, you must run the Script include `Choice and Template Migration Script`. The instructions on how to run the script are included in the Script include description.

Role required: sn\_wsd\_rsv.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Flexible Services**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_aff_dh4_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the flexible service.

</td></tr><tr><td>

Description

</td><td>

Short description about the service.

</td></tr><tr><td>

Category

</td><td>

Category of the flexible service. To add a new category, do the following: 1.  Right-click **Category** and select **Configure choices**.
2.  On the Configure Category Choices form, in the **Enter a new item** field, enter the name of the category that you want to add.
3.  Click **Add**.


</td></tr><tr><td>

Sub Category

</td><td>

Subcategory of the selected category of the flexible service. You can also add a subcategory by following the same steps as when adding a category.

</td></tr><tr><td>

Active

</td><td>

Option to activate the flexible service.

</td></tr><tr><td>

Image

</td><td>

Image of the flexible service.

</td></tr><tr><td colspan="2">

**Service Configuration**

</td></tr><tr><td>

Preparation duration

</td><td>

Time required to prepare the flexible service. For example, if the flexible service is a catering service, then specify the time that is required to prepare the items.The workplace location will be blocked for the specified duration to prepare before the reservation starts. Enable the \[sn\_wsd\_rsv.is\_blocker\_mandatory\] system property to create a blocker reservation.

</td></tr><tr><td>

Cleanup duration

</td><td>

Time required to clean up the items that are provided in the flexible service.The workplace location will be blocked for the specified duration to clean up after the reservation ends. Enable the \[sn\_wsd\_rsv.is\_blocker\_mandatory\] system property to create a blocker reservation.

</td></tr><tr><td>

Quantity enabled

</td><td>

Maximum quantity of items that are available to reserve.

</td></tr><tr><td>

Price per unit

</td><td>

Pricing of the flexible service.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The flexible service is added to the application.

## What to do next

Add the flexible service to a workplace space or room, so that the service is available to employees when they make a reservation. For more information, see [Add a flexible service to workplace item](add-flex-service-to-workplace-item.md).

-   **[Add a flexible service to workplace item](add-flex-service-to-workplace-item.md)**  
Enable employees to request for extra services. Add an extra service to a workplace space or room, and make the service available to employees when they make a reservation.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

