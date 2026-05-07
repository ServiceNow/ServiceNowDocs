---
title: Holiday calendars
description: Pull holiday calendars from Workday into the ServiceNow application. Display the Holiday Calendar widget to employees in the configured Service Portal.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Time off request to Workday, Use, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Holiday calendars

Pull holiday calendars from Workday into the ServiceNow application. Display the Holiday Calendar widget to employees in the configured Service Portal.

## Before you begin

Role required: sn\_hr\_workday.admin

Configure the Get holiday calendar WID report. For more information, see [Configure reports HR Service Delivery Advanced Integration with Workday](../concept/awd-config-re.md#).

## Procedure

1.  Navigate to **All** &gt; **Workday Advanced Use Cases** &gt; **Time Off Request** &gt; **Holiday Calendars**.

2.  Click **Get Holiday Calendars** to run the subflow that interacts with Workday to pull holiday calendars.

3.  To create a holiday calendar, click **New**.

    |Field|Description|
    |-----|-----------|
    |Calendar event name|Name of the holiday event. For example, Holidays for Argentina.|
    |Holiday calendar ID|ID for the holiday calendar that is pulled from Workday.|
    |Holiday calendar WID|Unique identifier of the holiday calendar that is pulled from Workday.|
    |Domain|Reference to domain.|
    |Start date|Start date of the calendar event.|
    |Start time|Start time of the calendar event.|
    |End date|End date of the calendar event.|
    |End time|End time of the calendar event.|
    |Holiday Calendar name|Name of the holiday calendar. For example, Christmas day.|

4.  Click **Submit**.


## What to do next

Display holiday calendar widget to employees.

1.  Navigate to **Service Portal** &gt; **Service Portal Configuration** &gt; **Designer**.
2.  In widget, select the **View Workday Holiday Calendar** and add it to the required Service Portal page.

**Parent Topic:**[Time off request to Workday](../concept/w-timeoff.md)

