---
title: Configuring manual location tracking
description: Configure manual location tracking system properties to control how location tracking registers the activity of your users, while performing their tasks.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enabling/selecting options, Location tracking, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configuring manual location tracking

Configure manual location tracking system properties to control how location tracking registers the activity of your users, while performing their tasks.

## Before you begin

Role required: admin

## About this task

There are two system properties which control how location tracking registers user activity in manual tracking mode. The values of both the conditions must be met to record a new location:

-   **glide.geolocation.proximity** – This system property measures the minimum distance in meters that a user must move to be considered a new location. The default is 500 meters.
-   **glide.geolocation.tracking.frequency** – This system property measures the amount of time in seconds when an update of the user’s location is recorded. The default is 300 seconds.

**Note:**

-   Manual location tracking is only supported on the Mobile Agent app.
-   Consider that the higher the frequency or proximity value the more drain on the battery of the user's device. These higher settings may also affect data protection and privacy of the user.

## Procedure

1.  Navigate to **All** and then enter `sys_properties.list` in the navigation filter.

2.  Select the location tracking mobile properties that you want to configure.

<table id="choicetable_dtv_3vz_2wb"><thead><tr><th align="left" id="d36656e104">

System property

</th><th align="left" id="d36656e107">

Procedure

</th></tr></thead><tbody><tr><td id="d36656e113">

**glide.geolocation.tracking.frequency**

</td><td>

1.  In the **System Properties** field, search for the name **glide.geolocation.tracking.frequency**.
2.  In the **Value** field for the selected system property, select the value and change it to your desired amount.


</td></tr><tr><td id="d36656e140">

**glide.geolocation.proximity**

</td><td>

1.  In the **System Properties** field, search for the name **glide.geolocation.proximity**.
2.  In the **Value** field for the system property, select the value and change it to your desired amount.


</td></tr></tbody>
</table>3.  Right-click in the header and select **Save**.


**Parent Topic:**[Enabling and selecting location tracking options](location-tracking-enable.md)

