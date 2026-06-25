---
title: Update the measurement details of a workplace location
description: Specify the size of a location. If the location is an area, floor or building, then you can update or recalculate the total and usable size.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-space-management/update-measurement-details-of-workplace-location.html
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Update the measurement details of a workplace location

Specify the size of a location. If the location is an area, floor or building, then you can update or recalculate the total and usable size.

## Before you begin

Ensure that the space, room, area, floor, or building is active.

Role required: sn\_wsd\_spcmgmt.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select the applicable module.

    -   **Spaces**
    -   **Rooms**
    -   **Areas**
    -   **Floors**
    -   **Buildings**
    For example, if you want to update the size of a space, select **Spaces**.

3.  Go to the **Measurement details** section and update the measurements.

    |Field|Description|
    |-----|-----------|
    |Size|Size of the area, floor, or building. This field appears if you selected the Spaces or Rooms module.|
    |Total size|Total size of the area, floor, or building.|
    |Usable size|Usable size of the area, floor, or building.|
    |Measurement unit|Measurement unit that is used to view the sizes. This field is automatically set based on the value selected in the **sn\_wsd\_spcmgmt.default\_area\_measurement\_unit** system property.|

4.  Recalculate the size.

    Click the recalculate size icon \(\[Omitted image "recalculate-size-icon.png"\] Alt text: Recalculate size icon.\) next to the **Total size** or **Usable size** field.The recalculate size icon appears if you change the sizes manually. If the size of any child location of the selected location changes, the sizes are automatically recalculated.

5.  Click **Update**.

6.  To recalculate the sizes of multiple workplace locations at a time, do the following:

    1.  Select the workplace location module on which you want to perform the recalculation.

        For example, to recalculate the sizes of multiple buildings, go to **Workplace Core** &gt; **Space Administration** &gt; **Buildings**.

    2.  Select the locations on which you want to perform recalculation.

        For example, if you are in the Buildings module, select the check box next to each building that you want to recalculate.

    3.  Perform recalculation on all the locations at the same time.

        Select the check box on the bottom, next to the **Action on selected rows...** option.

    4.  Click **Action on selected rows...**.

        After clicking, do the following:

        -   **Recalculate Total Sizes**: Select this option to recalculate the **Total size** of all the locations.
        -   **Recalculate Usable Sizes**: Select this option to recalculate the **Usable size** of all the locations.

## Result

The size of the workplace location is updated.

**Parent Topic:**[Managing workplace locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus]()

[Add a building using Workplace Space Management]()

[Add a floor using Workplace Space Management]()

[Add an area using Workplace Space Management]()

[Add a room using Workplace Space Management]()

[Add a space using Workplace Space Management]()

[Allocate a cost center, department, or workplace entity]()

[Configure a workspace or desk as flexible or permanent]()

[Change the status of a workplace location]()

[Configure a BOMA type]()

[Map a space type with BOMA type]()

[Create a Space Recommender rule]()

[Raise a space assistance request]()

[Create a view-by configuration]()

[Create a KPI Configuration]()

[Reviewing allocation changes]()

