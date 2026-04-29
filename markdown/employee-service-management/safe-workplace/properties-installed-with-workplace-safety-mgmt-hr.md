---
title: Properties installed with Workplace Core
description: Customize the properties available with Workplace Core.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Install Workplace Core, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Properties installed with Workplace Core

Customize the properties available with Workplace Core.

These properties are available for Workplace Core.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_ybm_p5w_qlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_core.AUTO\_ASSIGN\_LOCATION

</td><td>

Enables auto-assignment of workspaces when employees make workspace reservation requests.-   Type: true\|false
-   Default value: false

 **Note:** Once this feature is enabled, the fields related to workplace locations such as **Area**, **Space preference**, and **Space** do not appear on the Workspace Reservation form. Enable this feature only if all employees have a designated workspace in their user profiles in the User Workplace Profile \[sn\_wsd\_core\_workplace\_profile\] table. For more information, see [Mapping employees to their designated workspaces](../../workplace-service-delivery/concept/mapping-employees-to-existing-work-locations-wsd.md).

</td></tr><tr><td>

sn\_wsd\_core.CANCEL\_RES\_BUILDING

</td><td>

Determines whether the reservations made for spaces should be canceled based on the value of the **Is reservable** field.-   Type: true\|false
-   Default value: false

 If this property is set to **true**, then the application cancels all the workspace reservations that are made for the areas and spaces of those buildings or floors for which the value of the **Is reservable** field is set to **false**.

</td></tr><tr><td>

sn\_wsd\_core.CLEANING\_TASK\_MAX\_DURATION

</td><td>

Determines the duration \(in days\) by when you want the pre-cleaning and post-cleaning tasks to be executed.-   Type: Integer
-   Default value: 7

</td></tr><tr><td>

sn\_wsd\_core.floor\_plan.portal.show\_non\_reservables

</td><td>

Determines whether non-reservable workspaces appear in grey on the floor plan in the Workplace Service Portal.-   Type: true\|false
-   Default value: false

 **Note:** Changing this value to true can negatively affect performance.

</td></tr><tr><td>

sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details

</td><td>

Determines whether reservation details appear when users point to booked spaces on the floor plan in Workplace Service Portal.-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

sn\_wsd\_core.REQUEST\_MAX\_DURATION

</td><td>

Determines the maximum number of days that an employee can request a space reservation for at one time. This property is applicable when an employee requests a space reservation for multiple days.

-   Type: Integer
-   Default value: 7

</td></tr><tr><td>

sn\_wsd\_core.show\_book\_uber

</td><td>

Determines the visibility of the **Book Uber** button on the Now® Mobile app.If this property is set to **true**, then employees can select **Book Uber** from their confirmed reservations on their mobile devices. Users are redirected to the Uber mobile app.

-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

sn\_wsd\_core.wsd\_inbound\_email

</td><td>

Checks for emails that are received for the ServiceNow® Workplace Service Delivery and Workplace Case Management applications.This property has been renamed from the **sn\_wsd\_case.wsd\_inbound\_email** property in Workplace Case Management version 1.0.1.

 This property is available only for Workplace Safety Management 2.0.3 or later.

-   Type: String
-   Default value: askwsd@example.com
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_wsd\_core.floor\_transform\_map

</td><td>

Enables you to configure customized transform maps. -   Type: string
-   Default value: 2528fbf70f201010dbc3d2d92f767e04

</td></tr><tr><td>

sn\_wsd\_core.ENABLE\_RSV\_CHECK\_IN

</td><td>

Enables reservation check-in and check-out via email.If this property is set to **true**, then employees can check in and check out a reservation.

-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

sn\_wsd\_core.dfx.rebuild\_cache.max\_floors

</td><td>

Enables you to specify the maximum number of floors to build for an entity cache at any time.-   Type: Integer
-   Default value: 20

</td></tr><tr><td>

sn\_wsd\_core.CANCEL\_RES\_LOCATION

</td><td>

Enables you to cancel all future reservations made on a location level. Set the **Is reservable** field to **false** for the location.-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

sn\_wsd\_core.ALLOW\_USER\_SHIFT\_FILTERING

</td><td>

Enables a user to create shift-based reservations only if the user is part of that shift.-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

sn\_wsd\_core.ALLOW\_AVAILABILITY\_FILTERING

</td><td>

Displays only the available buildings and floors in the reservation record producers.-   Type: true\|false
-   Default value: false

 **Note:** If the property is set to **true**, then the selected workplace locations take a longer time to load.

</td></tr><tr><td>

sn\_wsd\_core.MULTI\_DAY\_AVAILABILITY

</td><td>

Displays only the available areas and spaces in multi-day reservation record producers.-   Type: true\|false
-   Default value: false

 **Note:** If the property is set to **true**, then the selected workplace locations take a longer time to load.

</td></tr><tr><td>

ARRIVAL\_REQUEST\_MAX\_FUTURE\_DAYS

</td><td>

Enables you to specify the maximum number of days in the future until when employees can schedule their arrival.-   Type: Integer
-   Default value: 7

</td></tr></tbody>
</table>**Parent Topic:**[Install Workplace Core](../task/install-workplace-safety-mgmt-hr.md)

