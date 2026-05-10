---
title: Action-based location tracking for Field Service Management example
description: Make updates to action-based location tracking for more accurate tracking of an agent’s location. That way you can make scheduling adjustments on the fly if you see they’re location is farther away than anticipated.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure the Now Mobile Agent application, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Action-based location tracking for Field Service Management example

Make updates to action-based location tracking for more accurate tracking of an agent’s location. That way you can make scheduling adjustments on the fly if you see they’re location is farther away than anticipated.

## Before you begin

Configuring action-based location tracking 

Role required: admin

## About this task

In the example below you’re adjusting the start travel action item to track the agent for a longer period and more accurately.

Action based tracking will track a Field Service agent’s location when the agent clicks a work order task action button. The duration for tracking is configured by an administrator. Changing action based settings don’t impact status changes if you have manual tracking configured. Action based is customizable to all functions that change the state of a work order task out of the box. For more information on action based tracking, see [Configuring action-based location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/location-tracking-action-config.md).

Manual based tracking will track a Field Service agent for a certain period of time. For example continuously, or for a given set of hours, regardless of if a Field Service agent clicks a work order task action button. For more information on manual based tracking, see [Configuring manual location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/location-tracking-manual-config.md).

The wm\_agent role is required for tracking. This must be applied to the agent in order for customer and geolocation tracking.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Functions**.

2.  Search for and select the **Start Travel** function.

3.  Select **here** if you see the notice that says:

    This record is in the Field Service Mobile application, but Global is the current application. To edit this record, select.

4.  Open the **Location Tracking** tab.

5.  Select the Preview this record icon ![Preview this record](../image/preview-record.png) on the Tracking Properties line.

6.  Select **Open Record**.

7.  Select **here** if you see the notice that says:

    This record is in the Field Service Mobile application, but Global is the current application. To edit this record, select.

8.  Adjust the location tracking settings:

    1.  Change the duration from 1 to 3. That tracks a Field Service agent’s location for three hours instead of the default 1.
    2.  Change the accuracy from medium to high. This shows you the agent’s location within 10 meters instead of the default 100 meters.
    3.  Change the Proximity from 100 meters to 10 meters. That updates the agent’s location when they move more than 10 meters instead of 100.
    4.  Change the Frequency from one hour to one minute. That updates the agent’s location every minute.

        **Note:** Changing the frequency to every minute should only be done if necessary for your tracking purpose use case.

9.  Select Update.


