---
title: Configure workplace space suggestions for employees
description: Configure the workplace space suggestions table to fetch workspace suggestions. Application provides workspace suggestions based on employee preferences when they are reserving a space.
locale: en-US
release: yokohama
product: Workplace Concierge
classification: workplace-concierge
topic_type: concept
last_updated: "2025-07-20"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Configure workplace space suggestions for employees

Configure the workplace space suggestions table to fetch workspace suggestions. Application provides workspace suggestions based on employee preferences when they are reserving a space.

Workplace Concierge and Workplace Core administrators can configure workplace suggestions while suggesting a space to an employee. Employees can have access to a space matching their needs to complete a set of activity like reserving a space, selecting their in-office presence days, preferred collaborators, and workplace services.

**Note:** The option to add your workplace preferences and suggestions are also available on the Employee Center portal. Employees are expected to use the Workplace Service Delivery for Mobile app to reserve a space and to view or modify their preferred workplace locations and workplace schedule suggestions. Reserve a workspace using the Workplace Service Delivery for Mobile app. Get desk suggestions based on your preferred location, past and future reservations, proximity \(preferred collaborators\), favorite spaces, neighborhoods, and standard services.

When an employee searches for a workspace using Workplace Service Delivery for Mobile, the application provides space suggestions to an employee based on the following criteria:

-   Availability of the space based on the Reservable module \(Desks\) configuration in Workplace Reservation Management
-   Employee presence preferences set in Workplace Concierge for primarily \(or solely\) suggesting the building or location the employee plans to visit while in office.
-   Favorite locations \(campus, building, floor, or neighborhoods\) set by an employee
-   Preferred workplace services added in workplace preferences
-   Past and future reservations data
-   Proximity \(preferred collaborators\)
-   Workplace services

The employee can set their workplace schedule and in-office preferences in Workplace Service Delivery for Mobile. When suggesting a space to an employee, application uses these preferences. For more information see, [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).

-   **[User Space Suggestions](../task/userspace-suggestions.md)**  
Employee recommended workspace suggestions are cached in the User Space Suggestions \(sn\_wsd\_core\_user\_space\_suggestions\) table record. This table gets automatically updated when employees use the workplace preferences option to update their reservations, workplace services, presence and collaborators information. Application uses this cached data while proposing a workspace suggestion to an employee.
-   **[Space suggestion Configuration](../task/space-suggestion-configuration.md)**  
Administrators can configure space suggestions for employees to help employees reserve their preferred workspace. Employees can reserve a workspace based on their preferences using the Workplace Service Delivery for Mobile app. Workplace suggestions for an employee are derived from employee presence data, location preferences, employee's favorite workspaces, past and future reservation data, preferred collaborators, and standard services.

**Parent Topic:**[Configure Workplace Concierge](configure-workplace-concierge.md)

**Related topics**  


[Install Workplace Concierge](../task/install-workplace-concierge.md)

[Configure calendar sections on the Presence dashboard](../task/configure-presence-dashboard-sections.md)

[Components installed with Workplace Core](../../workplace-service-delivery/reference/components-installed-with-workplace-service-delivery.md)

[Properties installed with Workplace Concierge](../reference/properties-installed-with-workplace-concierge.md)

[Set Employee Presence](use-workplace-concierge.md)

