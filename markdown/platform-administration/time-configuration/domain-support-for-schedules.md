---
title: Domain support and schedules
description: Domain separation is supported in schedules. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Activate the Domain Support \[com.glide.domain\] plugin to enable the domain separation functionality for schedules.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Schedules, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain support and schedules

Domain separation is supported in schedules. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Activate the Domain Support \[com.glide.domain\] plugin to enable the domain separation functionality for schedules.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Overview

The records in the Schedule \[cmn\_schedule\], Schedule Page \[cmn\_schedule\_page\], and Timeline Page \[cmn\_timeline\_page\] tables have a defined domain.

-   The child tables use the **domain\_master** attribute to derive the domain from the parent table.
-   You can find the **domain\_master** attribute on the dictionary record for the respective table.

The following diagram illustrates the scope of domain separation in different schedule tables:

![domain support for schedules](../image/domain-support-for-schedules-3.png "Domain support for schedules")

## Custom domain support implementations

Domain separation support does not automatically occur when you migrate to a new release containing a custom implementation of domain support for tables such as Schedule Entry \[cmn\_schedule\_span\]. This action avoids changing any specific configurations that you may have in place.

To implement the base system domain support for schedules, a sys.script utility is provided. To run this utility, navigate to **Background** &gt; **Scripts – Background**. The script is listed under the com.glide.schedules plugin as `fix_schedule_domain_support.js`.

-   The utility attempts to add the **Domain** \[sys\_domain\] column to the Schedule \[cmn\_schedule\], Schedule Page \[cmn\_schedule\_page\], and Timeline page \[cmn\_timeline\_page\] tables.
-   It then attempts to add the domain\_master attribute to the Schedule Entry \[cmn\_schedule\_span\], Other Schedule \[cmn\_other\_schedule\], Timeline Sub Item \[cmn\_timeline\_sub\_item\], and Timeline Page Span Style \[cmn\_timeline\_page\_style\] tables.
-   If the script finds existing records between a child and parent record that have differing domain, the script does not introduce the **domain\_master** attribute to the child table.

For example, consider the relationship of the Schedule \[cmn\_schedule\] \(parent\) and Schedule Entry \[cmn\_schedule\_span\] \(child\) tables. If the **Domain** \[sys\_domain\] column is available on both tables in the upgrading instance, the utility must migrate to the base system implementation of domain support for schedules.

-   If the script detects records where the child Schedule Entry \[cmn\_schedule\_span\] domain differs from its parent Schedule \[cmn\_schedule\] domain, it stops executing and logs a warning message.
-   If the script does not find differing records, it deactivates and limits read access to the **Domain** \[sys\_domain\] and **Domain Path** \[sys\_domain\_path\] columns on the Schedule Entry \[cmn\_schedule\_span\] table.
-   Finally, the script adds the domain\_master=schedule attribute to the dictionary file for the Schedule Entry \[cmn\_schedule\_span\] table.

**Note:** The **domain\_master** attribute ensures that the child and parent record domains remain the same as the domain for the child that is derived from the specified reference field.

**Parent Topic:**[Schedules](c_UseSchedules.md)

**Related topics**  


[Default schedules](../reference/r_DefaultSchedules.md)

[Holidays](c_Holidays.md)

[Create a holiday schedule for multiple regions](../task/t_CreateAHolidaySchedMultiRegions.md)

[Parent and child schedules](c_ParentAndChildSchedules.md)

[Define a schedule](../task/t_DefineASchedule.md)

[Schedule for the fifth instance of a week date](../task/t_FifthInstanceOfADayOfTheWeek.md)

[Repeat a monthly schedule](../task/t_RepeatAMonthlySchedule.md)

[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

