---
title: User Space Suggestions
description: Employee recommended workspace suggestions are cached in the User Space Suggestions \(sn\_wsd\_core\_user\_space\_suggestions\) table record. This table gets automatically updated when employees use the workplace preferences option to update their reservations, workplace services, presence and collaborators information. Application uses this cached data while proposing a workspace suggestion to an employee.
locale: en-US
release: yokohama
product: Workplace Concierge
classification: workplace-concierge
topic_type: task
last_updated: "2025-04-28"
reading_time_minutes: 2
breadcrumb: [Configure workplace space suggestions for employees, Configure, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# User Space Suggestions

Employee recommended workspace suggestions are cached in the User Space Suggestions \(sn\_wsd\_core\_user\_space\_suggestions\) table record. This table gets automatically updated when employees use the workplace preferences option to update their reservations, workplace services, presence and collaborators information. Application uses this cached data while proposing a workspace suggestion to an employee.

## Before you begin

The following plugins are required:

-   Workplace Core
-   Workplace Concierge
-   Workplace Reservation Management
-   Workplace Space Management

**Note:** Administrators don't have to configure or make updates to this table record. The data in this table is automatically updated based on the employee presence and workplace preferences data.

Role required: sn\_wsd\_core.admin, sn\_wsd\_concierge.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Concierge** &gt; **Workplace Suggestions** &gt; **User Space Suggestions**.

    **Note:** The table record summarization is for illustration only and administrators don't have to make changes to this record.

2.  Select **New**.

    In the User Space suggestions new record, complete the following field information.

<table id="table_h5x_132_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Indicates an employee user.

</td></tr><tr><td>

Space types

</td><td>

Indicates the Space type column option in the Spaces table record. For example, Workplace/Desks. For more information, see:

-   [Properties installed with Workplace Concierge](../reference/properties-installed-with-workplace-concierge.md)
-   [Add a space using Workplace Space Management](../../workplace-space-management/task/add-a-space.md)
-   [Add a space type configuration](../../workplace-service-delivery/task/add-space-type-configuration-wsd.md)


</td></tr><tr><td>

Building

</td><td>

Indicates the building proposed to an employee or a building selected by an employee based on workplace preferences and suggestions. For more information, see [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md) and [Set Employee Presence](../concept/use-workplace-concierge.md).

</td></tr><tr><td>

Suggestions

</td><td>

System ID of the default Reservable module that is used. For example, the **Desks** Reservable module.

</td></tr></tbody>
</table>    **Note:** The cached data in the User Space suggestions \(sn\_wsd\_core\_user\_space\_suggestions\) is purged after 48 hours by the application.


**Parent Topic:**[Configure workplace space suggestions for employees](../concept/configure-workplace-suggestions.md)

**Related topics**  


[Space suggestion Configuration](space-suggestion-configuration.md)

[Set Employee Presence](../concept/use-workplace-concierge.md)

[Manage your in-office presence preferences](../../wsd-for-mobile/task/workplace-preferences-emp-center.md)

[Create a reservation for a day in Workplace](../../wsd-for-mobile/task/manage-schedule-emp-center.md)

