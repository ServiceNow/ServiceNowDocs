---
title: Configure statistics processing period
description: Set the time period, in seconds, for collecting event processing statistics. For example, you can set a time period twice as long as the default 60 seconds to collect more statistics.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View event processing statistics, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure statistics processing period

Set the time period, in seconds, for collecting event processing statistics. For example, you can set a time period twice as long as the default 60 seconds to collect more statistics.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Use the **evt\_mgmt.event\_processing\_stats\_period** property to configure the XMLStatsEm script time to collect event processing statistics. The default value of this property is 60 and the unit is second. Set the property values to run the script over a longer or shorter period. For example, set a shorter period of statistics collection so fewer CPU resources are used.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the **evt\_mgmt.event\_processing\_stats\_period** property.

    Either configure the value of an existing **evt\_mgmt.event\_processing\_stats\_period** property to run the XMLStatsEm script over a shorter or longer time period or create a new property if it does not exist already.

    -   If the property exists, set the property to the required time period to enable the XMLStatsEm script time to collect event processing statistics and click **Update**.
    -   If the property does not exist, click **New**, fill in the form, and click **Submit**.

**Related topics**  


[bundle-platadm.t_AddAPropertyUsingSysPropsList]

