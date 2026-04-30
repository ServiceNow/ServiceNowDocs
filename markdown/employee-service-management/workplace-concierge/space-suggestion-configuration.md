---
title: Space suggestion Configuration
description: Administrators can configure space suggestions for employees to help employees get the most preferred space. Employees can get their preferred workplace suggestions while searching for a space using the Workplace Service Delivery for Mobile. Workplace suggestions for an employee are derived from employee presence data, location preferences, favorite workspaces, past and future reservation data, preferred collaborators, and standard services.
locale: en-US
release: xanadu
product: Workplace Concierge
classification: workplace-concierge
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 4
breadcrumb: [Configure workplace space suggestions for employees, Configure Workplace Concierge, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Space suggestion Configuration

Administrators can configure space suggestions for employees to help employees get the most preferred space. Employees can get their preferred workplace suggestions while searching for a space using the Workplace Service Delivery for Mobile. Workplace suggestions for an employee are derived from employee presence data, location preferences, favorite workspaces, past and future reservation data, preferred collaborators, and standard services.

## Before you begin

The following plugins are required:

-   Workplace Core
-   Workplace Concierge
-   Workplace Reservation Management
-   Workplace Space Management

**Note:** Load the demo data available with Workplace Core after installing the application. The demo data available with Workplace Core provides sample data types to illustrate Space Suggestion Configuration table \[sn\_wsd\_core\_space\_suggestion\_configuration\] use. If you’re using demo data or product data \(seed data\), some fields are pre-filled. If you aren’t using the demo data, you can configure the space suggestions table record as required.

Role required: sn\_wsd\_core.admin, sn\_wsd\_concierge.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Concierge** &gt; **Workplace Suggestions** &gt; **Space Suggestion Configuration**.

2.  Select **New**.

3.  Fill in the form fields.

    **Note:** Make sure only one record exist for each preference type.

<table id="table_up2_l2g_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suggestion type

</td><td>

Option to select a suggestion type to display preferred workplace suggestions to employees in the search results when they are reserving a space.Select any of the following Suggestion types:

-   Location: Location set in the Employee's workplace profile is suggested as the preferred workplace location. Employees can change their preferred location \(Campus, building, Floor\) pm the in-office preferences tab on Workplace Service Delivery for Mobile.
-   Favorites: Spaces favotired by an employee is prioritized and favorite spaces show up first in the search results when an employee searches for a workspace.
-   Past and Future reservations: Workspace suggestions based on employee's past and future reservation data is considered and prioritized while suggesting a space to an employee.
-   Proximity: Employee's preferred workplace collaborators. Preferred collaborators and their in-office days or workday schedule is taken into consideration when proposing a space to an employee.
-   Standard services: Workspace suggestion based on preferred workplace services by an employee.
For more information, see [Manage your in-office presence preferences](../../wsd-for-mobile/task/workplace-preferences-emp-center.md) and [Set Employee Presence](../concept/use-workplace-concierge.md).

</td></tr><tr><td>

Weight

</td><td>

Option to provide a weight \(integer value\) to prioritize the suggestion type while proposing a space to an employee. If the weight given is higher for a **Suggestion type**, application uses the higher weight to prioritize and suggest a space in the search results when proposing a workspace to an employee. Suggestion types with higher weight are ranked first in the search results when an employee searches for a space. For example, if the Suggestion type **Location** is having the weight value of 33, **Proximity** has 32, and **Favorites** has 12, **Location** is given more preference and ranked higher in the search result. Employee's preferred location is suggested first to an employee in the search results, followed by **Proximity**, and **Favorites**.

</td></tr><tr><td>

Active

</td><td>

Option to set the check box value to true.

</td></tr><tr><td>

Suggestion Tag

</td><td>

Option to add a tag or label for a space suggestion type. For example,the tags can be added as**Preferred services**, **Near Collaborators**,**Preferred location**, **Your favorite**,**Reserved frequently**, and so on. The tags are displayed on the **Desk suggestions** card in Workplace Service Delivery for Mobile. For more information, see [Create a reservation for a day in Workplace](../../wsd-for-mobile/task/manage-schedule-emp-center.md).

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Set the properties in Workplace Concierge for employee to enable workplace suggestion types.

    For more information, see [Properties installed with Workplace Concierge](../reference/properties-installed-with-workplace-concierge.md).

    After the configuration is complete and required properties are enabled, employees can start managing their workplace schedule and preferences. For more information, see [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).


**Parent Topic:**[Configure workplace space suggestions for employees](../concept/configure-workplace-suggestions.md)

**Related topics**  


[User Space Suggestions](userspace-suggestions.md)

[Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md)

[Components installed with Workplace Core](../../workplace-service-delivery/reference/components-installed-with-workplace-service-delivery.md)

[Set Employee Presence](../concept/use-workplace-concierge.md)

