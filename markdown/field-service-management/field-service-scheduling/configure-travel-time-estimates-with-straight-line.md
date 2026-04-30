---
title: Configure travel time estimates with latitude and longitude
description: Use the straight-line travel estimate provider in Schedule Optimization that provides built-in time and distance travel estimates based on latitude and longitude.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-04-22"
reading_time_minutes: 1
breadcrumb: [Setting up a travel estimate provider, Create a scheduling attribute, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure travel time estimates with latitude and longitude

Use the straight-line travel estimate provider in Schedule Optimization that provides built-in time and distance travel estimates based on latitude and longitude.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Map Integrations for Field Service** &gt; **Travel Time Estimate Configuration** &gt; **All**

2.  Select **New** to create a new configuration.

3.  On the form, provide a name for the travel time estimate provider and an optional description.

4.  In the **Select a travel estimate provider** field, select Straight-line.

5.  Update the speed limit for the region in the **General** tab.

    The default speed is set to 25 mph.

6.  Update the values in the **Multipliers** tab.

    Use multipliers to adjust the baseline straight-line travel time to help make the estimate more realistic by reflecting real-world conditions. The estimated travel time is multiplied by a value based on the time bracket it falls into.

    |Travel time|Multiplier|Description|
    |-----------|----------|-----------|
    |Under 15 minutes|2|Increases short-trip estimates to be more realistic.|
    |Between 15 and 60 minutes|1|The baseline estimate is unmodified.|
    |Between 60 and 180 minutes|0.8|Slightly reduces longer trip times.|
    |Over 180 minutes|0.5|Reduces very long trip times by half.|

7.  Select **Submit**.

8.  Add travel band modifiers to adjust travel for specific times of day.

    **Note:** Travel bands can vary in duration, ranging from 30 minutes to 4 hours, and can't overlap.

    1.  Select an existing Straight-line record.

    2.  Scroll down and select the **Travel Band Modifiers** tab.

    3.  Select **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Start time|The beginning time of the travel band or time window during which the modifier applies.|
        |End time|The ending time of the travel band or time window during which the modifier applies.|
        |Multiplier|A numerical factor applied to the base travel time to adjust for traffic or other conditions during the specified time range.|
        |Days of week|The days of the week when the travel band modifier is active.|
        |Active|Option to activate the travel band configuration.|

    5.  Select **Submit**.

    6.  Select **Update**.


