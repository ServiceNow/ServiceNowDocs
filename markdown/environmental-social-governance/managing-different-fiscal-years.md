---
title: Managing different fiscal years
description: Many global organizations have operations in different countries and each country could follow their own fiscal calendars instead of following the standard Gregorian calendar. When you create fiscal calendars, you enable the entities in other locations to collect data according to their own fiscal calendars.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Managing different fiscal years

Many global organizations have operations in different countries and each country could follow their own fiscal calendars instead of following the standard Gregorian calendar. When you create fiscal calendars, you enable the entities in other locations to collect data according to their own fiscal calendars.

You can create multiple fiscal calendars, including a reporting calendar for global reporting. This reporting calendar must be used in the metric definition and set as the Target calendar. The other calendars, known as Source calendars, are then mapped to the Target calendar.

Consider a parent organization in India with two subsidiaries operating in different countries: the US and Australia. The US government's fiscal year runs from October 1 to September 30, while Australia's fiscal year spans from July 1 to June 30. The parent organization adheres to the Indian fiscal calendar, which is from April 1 to March 31. In this context, metric data is collected according to each country's fiscal year and then aggregated according into the global calendar used for data aggregation. If the metric data for the US is 100 and for Australia is 200, the combined data on the global calendar used by the parent organization would be 300. Here, the US and Australian fiscal calendars are considered source calendars, and the global calendar used by the parent organization is the target calendar.

There are four data collection frequencies that are supported for the fiscal year and they are as follows:

-   Monthly
-   Quarterly
-   Semi-annually
-   Annually

After you create fiscal calendars, you must map the calendars to specify which is your target calendar and your source calendar. You can then use these calendars in metric definitions and metrics. The calendar specified on the metric is used for data collection and the calendar specified on the metric definition is used for data aggregation. This means that if the metric definition has **Global calendar** specified, and the metric has **US calendar** specified, then the Global calendar will be used for data aggregation. For more information on mapping calendars, see [Map target and source calendars](../task/map-target-and-source-calendars.md).

**Note:** The calendars must begin on the first of every month.

**Related topics**  


[Create fiscal calendars](../task/enable-custom-fiscal-year.md)

