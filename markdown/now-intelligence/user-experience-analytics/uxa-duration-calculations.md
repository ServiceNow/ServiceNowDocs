---
title: Duration calculations
description: Durations in User Experience Analytics have specific calculations. Review these equations to understand the average duration per page and percentage time on site values.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, User Experience Analytics, Platform Analytics]
---

# Duration calculations

Durations in User Experience Analytics have specific calculations. Review these equations to understand the average duration per page and percentage time on site values.

## Average duration per page

The average duration per page is calculated as the sum of the duration on a page divided by the count of impressions on that page minus the count of exits from that page.

For example, there are 10 appearances of the Dashboard Overview within the specified date range. They spend a total of 720 seconds on the page. On four of these appearances, the Dashboard Overview ended the session without interaction on the page. Therefore, the calculation for average duration is 720 / 10 - 4 = 120 seconds.

## Percentage time on site

The percentage time on site is calculated as the sum of duration on a page divided by the sum of all page durations multiplied by 100.

For example, the Service Portal application contains three pages tracked by User Experience Analytics: Home, Knowledge, and Request. The total time spent on the Home page in the specified date range is 900 seconds; on the Knowledge page, 300 seconds; on the Request page, 300 seconds. The percentage time on the Home page is calculated as \(900 / 900 + 300 + 300\) \* 100 = 60%

**Parent Topic:**[User Experience Analytics reference](../content-framework/landing-page/user-experience-analytics-reference.md)

