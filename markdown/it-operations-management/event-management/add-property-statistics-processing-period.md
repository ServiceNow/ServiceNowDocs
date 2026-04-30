---
title: Configure statistics processing period
description: Set the time period, in seconds, for collecting event processing statistics. For example, you can set a time period twice as long as the default 60 seconds to collect more statistics.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View event processing statistics, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure statistics processing period

Set the time period, in seconds, for collecting event processing statistics. For example, you can set a time period twice as long as the default 60 seconds to collect more statistics.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Use the **evt\_mgmt.enable\_event\_processing\_stats** property to configure the XMLStatsEm script time to collect event processing statistics. The default value of this property is 60 and the unit is second. Set the property values to run the script over a longer or shorter period. For example, set a shorter period of statistics collection so fewer CPU resources are used.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the **evt\_mgmt.enable\_event\_processing\_stats** property.

3.  Either configure the value of an existing **evt\_mgmt.enable\_event\_processing\_stats** property to run the XMLStatsEm script over a shorter or longer time period or create a new property if it does not exist already.

    -   If the property exists, set the property to the required time period to enable the XMLStatsEm script time to collect event processing statistics and click **Update**.
    -   If the property does not exist, click **New**, fill in the form, and click **Update**.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the property you are creating.|
        |Description|Narrative that describes the property and its function.|
        |Choices|Comma-separated values for a choice list. If you need a different choice list label and value, use an equal sign \(=\) to separate the label from the value. For example, Blue=0000FF, Red=FF0000,Green=00FF00 displays Blue, Red, and Green in the list, and saves the corresponding hex value in the property value field.|
        |Type|Data type, that is selected from a list \(for example, integer, string, or true\|false\).|
        |Value|Desired value for the property. When retrieving properties using the **gs.getProperty\(\)** method, treat the results as strings. For example, a true\|false property returns 'true' or 'false' \(strings\), not the Boolean equivalent.|
        |Read roles|Roles that have read access to this property.|
        |Write roles|Roles that have write access to this property.|


**Parent Topic:**[View event processing statistics](monitor-event-processing-metrics.md)

**Related topics**  


[Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

