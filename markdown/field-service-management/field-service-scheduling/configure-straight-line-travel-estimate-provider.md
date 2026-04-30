---
title: Configure the travel estimate provider
description: Use straight-line travel estimate provider to use the built-in time and distance travel estimates based on latitude and longitude. Use Beans.AI, the map provider that Schedule Optimization supports, for more accurate travel time estimates.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up a travel estimate provider, Create a scheduling attribute for Schedule Optimization, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configure the travel estimate provider

Use straight-line travel estimate provider to use the built-in time and distance travel estimates based on latitude and longitude. Use Beans.AI, the map provider that Schedule Optimization supports, for more accurate travel time estimates.

## Before you begin

Role required: wm\_admin

## Procedure

1.  **All** &gt; **Schedule Optimization** &gt; **Configuration** &gt; **Scheduling Attributes**

2.  Choose Straight-line or Beans.ai in the travel estimate provider field.

    **Note:** Beans.ai operates on a bring your own license \(BYOL\) licensing model. If Beans.ai is not configured, travel estimates will default to straight-line.

3.  Open the **Straight line travel estimate configuration** record.

4.  On the form, fill in the name and description fields.

5.  Add the speed limit for the region in the **General** tab.

6.  Enter a value in the **Multipliers** tab.

    The multipliers defined in the straight-line calculation, are the values that the estimated straight-line travel time is multiplied by, depending on the time bracket the estimate falls in. If the travel time is less than 15 minutes, multiply by two or more, to increase the estimated travel time. If the travel time is greater than 15 minutes, multiply by 0.5 or less to decrease the estimated travel time.


