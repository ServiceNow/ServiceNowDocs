---
title: Create an emission factor
description: Create your own custom emission factors if you don’t want to use the standard emission factors provided by the ESG content accelerator application. An emission factor is a representative value that relates the quantity of a pollutant released to the atmosphere with the activity associated with the release of that pollutant.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the emission factor library, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create an emission factor

Create your own custom emission factors if you don’t want to use the standard emission factors provided by the ESG content accelerator application. An emission factor is a representative value that relates the quantity of a pollutant released to the atmosphere with the activity associated with the release of that pollutant.

## Before you begin

Role required: sn\_esg.program\_manager, sn\_esg.admin

## About this task

An emission factor is a coefficient that enables conversion of activity data into emissions. It’s the average emission rate of a given source, relative to the units of an activity or process. When you create an emission factor, you can select the unit from which you want to convert the data into the unit that you want to use to measure your emissions. For example, you can convert miles, which is the activity data, to the emissions the activity causes.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Emission Factor Library** &gt; **Factor**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the emission factor. For example, `Cars-Mini-Diesel-miles-KgCO2e`.|
    |From unit|Unit in which the data is collected.|
    |To unit|Unit to which the data must be converted.|
    |Emission activity|Emission activity or source of the factor.|

4.  Select **Submit**.


## Result

-   Two related lists are now available on the emission factor: 'Emission Factor Location', which was previously available and displays linked locations, and 'Calculated Metric Definition', a new addition that displays linked calculated metric definitions.
-   You can now use this emission factor in a calculated metric definition.

-   **[Add locations to an emission factor](add-locations-to-an-emission-factor.md)**  
Add locations to an emission factor after you create the factor. The reason you must add locations to a factor is that an organization may have different locations and each location may have a different factor value for different periods.
-   **[Recalculate emission factor](recalculate-emission-factor.md)**  
When an emission factor value is updated, you can recalculate the emission factor to initiate the system to automatically recalculate the data for all linked calculated metric definitions \(CMD\), using the new value for dates within the emission factor's validity period. This ensures that metrics data remains consistent and accurate, reflecting the latest changes.

**Parent Topic:**[Set up the emission factor library](../concept/set-up-the-emission-factor-library.md)

