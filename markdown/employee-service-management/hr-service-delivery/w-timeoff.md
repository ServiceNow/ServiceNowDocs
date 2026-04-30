---
title: Time off request to Workday
description: You can submit a time off request to Workday from Employee Center.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Time off request to Workday

You can submit a time off request to Workday from Employee Center.

The following sections explain how to configure time off settings, and raise a time off request from Employee Center.

## Time off settings

-   Configure the reports for time offs, absence tables, holiday calendars, and work schedule calendars. See [Configure reports HR Service Delivery Advanced Integration with Workday](awd-config-re.md#).
-   Import set up data for time offs. See [Time offs](../task/config-w-daytimeoff.md).
-   Get Holiday Calendars from Workday. See [Holiday calendars](../task/holiday-calendar-awd.md).
-   Get Work Schedule Calendars from Workday. See [Work schedule calendars](../task/schedule-calen-awd.md).

## Time off request

Request a time off to Workday from Employee Center. For more information, see [Request a time off](../task/request-timeoff.md).

## Limitations

-   Custom validations that are supported in Workday are not handled in the ServiceNow application. For example, if an organization has a time off plan configured to enter time off quantity in multiples of 2 or 4, such validations are not supported for such time off plans in the ServiceNow application.
-   A maximum of 25 days of leave, including holidays and non-working days, can be applied from the ServiceNow application.

-   **[Time offs](../task/config-w-daytimeoff.md)**  
Complete the one time set up of pulling time offs from Workday into the ServiceNow application.
-   **[Work schedule calendars](../task/schedule-calen-awd.md)**  
Pull work schedule calendars from Workday into the ServiceNow application.
-   **[Holiday calendars](../task/holiday-calendar-awd.md)**  
Pull holiday calendars from Workday into the ServiceNow application. Display the Holiday Calendar widget to employees in the configured Service Portal.
-   **[Request a time off](../task/request-timeoff.md)**  
Request a time off to Workday from Employee Center.

**Parent Topic:**[Using](using-hr-service-delivery-advanced-integration-with-workday.md)

