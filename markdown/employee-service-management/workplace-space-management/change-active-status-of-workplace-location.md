---
title: Change the status of a workplace location
description: Change the availability of a workplace location to Active, Future, Temporary, or Retired. The availability of a workplace location for any workplace-related activities is determined based on the status that is set.
locale: en-US
release: yokohama
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Change the status of a workplace location

Change the availability of a workplace location to Active, Future, Temporary, or Retired. The availability of a workplace location for any workplace-related activities is determined based on the status that is set.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

Set a status for a location. Specify the dates for when the status must be applied. Depending on when you want to plan to set the status, specify a planned start and end date. After you confirm a date for when the status change must be applied, specify the actual start and end date.

-   You can specify the status for Campus and below hierarchy locations. The status changes are applied from higher to lower hierarchy.
-   The status change is applied to only those child locations that have the same status. For example, if you have changed the status of a floor from **Active** to **Future**, then the status of only those rooms of that floor that have the status as **Active** are changed to **Future**. If there are rooms that have the status as **Temporary**, **Future** or **Retired**, then their status remains unchanged. The status change is applied the same way to child workplace locations, that is to the spaces of that room.
-   If you change the status of a location to **Future** or **Retired**, then the **Active** field is turned off and that location is unavailable for any workplace-related activities.
-   When you create a record for a workplace location, the **Status**, **Planned start date**, **Planned end date**, **Actual start date**, and **Actual end date** fields are automatically filled with the parent location's field values of that location.
-   The **Planned start date** and **Planned end date** must be on or between the **Planned start date** and **Planned end date** fields of the parent location.
-   If there are any child locations that are currently reserved, have an active workplace case, or are assigned as a permanent location to a user, you cannot change the status of a location from **Active** to either **Future** or **Retired**.
-   If you change the status of a location to **Future** or **Retired**, employees cannot reserve that location and any of its child locations. The locations are not displayed to employees while making a reservation. If an employee sets any one of the locations as the employee's favorite, then the **Reserve** option for that location is turned off in the employee's My favorites page.
-   If the status of any of the child locations is **Active** or **Temporary**, then the status of its parent location cannot be changed to **Future** or **Retired**. For example, if a space is **Active** or **Temporary**, you cannot change the status of the Floor to **Future** or **Retired**.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select **Spaces**.

3.  Click **New**.

4.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

    The form view changes.

5.  Change the status in the **Status** field.

6.  Select the **Planned start date** for when you are planning to activate/reactivate the location.

7.  Select the **Planned end date** by when you are planning to retire the location.

8.  Select the **Actual start date** for when the location is active.

9.  Select the **Actual end date** on which the location must be retired.

10. Click **Update**.


## Result

The status of the location is changed and applied to all the child locations.

A schedule job runs every month and a reminder email is sent to the workplace managers regarding the activation or retirement of locations. The managers must manually change the status of the locations that are listed in the email.

-   The reminder email includes information regarding the locations that require activation based on the **Planned start date**. The email also includes the locations that require retirement based on the **Actual end date**.
-   Apart from the monthly emails, reminder emails regarding the location activation or retirement are sent on the following days:
    -   For activation:
        -   One week before the **Planned start date**.
        -   On the **Planned start date**.
    -   For retirement:
        -   One week before the **Actual end date**.
        -   On the **Actual start date**.

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building-1.md)

[Add a floor using Workplace Space Management](add-a-floor-1.md)

[Add an area using Workplace Space Management](add-an-area.md)

[Add a room using Workplace Space Management](add-a-room.md)

[Add a space using Workplace Space Management](add-a-space.md)

[Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md)

[Configure a workspace or desk as flexible or permanent](assign-a-flex-perm-space.md)

[Update the measurement details of a workplace location](update-measurement-details-of-workplace-location.md)

[Configure a BOMA type](configure-a-boma-type.md)

[Map a space type with BOMA type](map-a-space-type-with-boma-type.md)

[Create a Space Recommender rule](create-a-space-recommender-rule.md)

[Raise a space assistance request](raise-a-space-recommendation-request.md)

[Create a view-by configuration](create-view-by-config.md)

[Reviewing allocation changes](../concept/reviewing-allocation-changes.md)

