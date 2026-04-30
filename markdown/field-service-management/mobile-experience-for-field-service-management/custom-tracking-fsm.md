---
title: Action-based location tracking for Field Service Management example
description: Make updates to action-based location tracking for more accurate tracking of an agent’s location. That way you can make scheduling adjustments on the fly if you see they’re location is farther away than anticipated.
locale: en-US
release: xanadu
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-01-07"
reading_time_minutes: 2
breadcrumb: [Configure the Now Mobile Agent application, Setting up Field Service Now Mobile Agent application, Configuring Field Service Management, Field Service Management]
---

# Action-based location tracking for Field Service Management example

Make updates to action-based location tracking for more accurate tracking of an agent’s location. That way you can make scheduling adjustments on the fly if you see they’re location is farther away than anticipated.

## Before you begin

Field Service Management \| Configuring action-based location tracking 

Role required: admin

## About this task

In the example below you’re adjusting the start travel action item to track the agent for a longer period and more accurately.

Action based tracking will track a Field Service agent’s location when the agent clicks a work order task action button. The duration for tracking is configured by an administrator. Changing action based settings don’t impact status changes if you have manual tracking configured. Action based is customizable to all functions that change the state of a work order task out of the box. For more information on action based tracking, see [Configuring action-based location tracking](https://www.servicenow.com/docs/access?context=location-tracking-action-config&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

Manual based tracking will track a Field Service agent for a certain period of time. For example continuously, or for a given set of hours, regardless of if a Field Service agent clicks a work order task action button. For more information on manual based tracking, see [Configuring manual location tracking](https://www.servicenow.com/docs/access?context=location-tracking-manual-config&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

The wm\_agent role is required for tracking. This must be applied to the agent in order for customer and geolocation tracking.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Functions**.

2.  Search for and select the **Start Travel** function.

3.  Select **here** if you see the notice that says:

    This record is in the Field Service Mobile application, but Global is the current application. To edit this record click here.

4.  Open the Location Tracking tab.

5.  Select the Preview this record icon Preview this record on the Tracking Properties line.

6.  Select **Open Record**.

7.  Select **here** if you see the notice that says:

    This record is in the Field Service Mobile application, but Global is the current application. To edit this record click here.

8.  Adjust the location tracking settings:

    1.  Change the duration from 1 to 3. That will track a Field Service agent’s location for 3 hours instead of the default 1.
    2.  Change the accuracy from medium to high. This will show you the agent’s location within 10 meters instead of the default 100 meters.
    3.  Change the Proximity from 100 meters to 10 meters. That will update the agent’s location when they move more than 10 meters instead of 100.
    4.  Change the Frequency from 1 hour to 1 minute. That will update the agent’s location every minute.
    **Note:**

    Changing the frequency to every minute should only be done if necessary for your tracking purpose use case.

9.  Select Update.


