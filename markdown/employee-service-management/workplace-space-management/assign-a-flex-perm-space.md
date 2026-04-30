---
title: Configure a workspace or desk as flexible or permanent
description: Define if a space is flexible or permanent. On the Reservation portal, the availability of a space for a user profile depends on its assignment type.
locale: en-US
release: yokohama
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a workspace or desk as flexible or permanent

Define if a space is flexible or permanent. On the Reservation portal, the availability of a space for a user profile depends on its assignment type.

## Before you begin

Ensure the following:

-   The space is added in the application. Otherwise, refer to [Add a space using Workplace Space Management](add-a-space.md).
-   The **Space type** field of the space is set to **Workspace/desk**.

Role required: sn\_wsd\_spcmgmt.manager

## About this task

You can specify if a desk or workspace is a permanent space or flexible. If you set a space as permanent, then the space will not be displayed to employees when they are making a reservation on the portal.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select **Spaces**.

3.  Select the space that you want to assign as a flexible or permanent space.

4.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

        The form view changes.

5.  In the **Assignment type** field, select any one of the following options:

    -   **None**: The **Assignment type** is set to **None** by default. The space is available both for reservation on the Reservation portal and for the workplace user profiles created in the Workplace Core application.
    -   **Flexible**: Select this option if the space is a flexible workspace. If you select this option, the space is made available for reservation on the Reservation portal. However, the space, as it is set as **Flexible**, cannot be assigned to a user profile as it may cause anomalies. Only **Permanent** spaces can be assigned to a user profile.
    -   **Permanent**: Select this option if the space is a permanent workspace. If you select this option, the space is displayed as available only for users created in the Workplace Core application. The space will not be available for reservation on the Reservation portal.

        If you are changing the **Assignment type** from **None** or **Flexible** to **Permanent**, then all the future reservations made on this space will be automatically canceled. A notification is sent about the cancellation.

6.  Click **Update**.


## Result

The space is configured as flexible or permanent based on the assignment type that you selected.

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building-1.md)

[Add a floor using Workplace Space Management](add-a-floor-1.md)

[Add an area using Workplace Space Management](add-an-area.md)

[Add a room using Workplace Space Management](add-a-room.md)

[Add a space using Workplace Space Management](add-a-space.md)

[Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md)

[Update the measurement details of a workplace location](update-measurement-details-of-workplace-location.md)

[Change the status of a workplace location](change-active-status-of-workplace-location.md)

[Configure a BOMA type](configure-a-boma-type.md)

[Map a space type with BOMA type](map-a-space-type-with-boma-type.md)

[Create a Space Recommender rule](create-a-space-recommender-rule.md)

[Raise a space assistance request](raise-a-space-recommendation-request.md)

[Create a view-by configuration](create-view-by-config.md)

[Reviewing allocation changes](../concept/reviewing-allocation-changes.md)

