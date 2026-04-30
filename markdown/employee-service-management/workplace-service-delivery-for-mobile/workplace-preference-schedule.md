---
title: Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile
description: Employees can plan their hybrid workplace schedule using the Workplace Service Delivery for Mobile. They can reserve a space for a day or make bulk reservations using Workplace.
locale: en-US
release: yokohama
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: concept
last_updated: "2025-07-23"
reading_time_minutes: 4
breadcrumb: [Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile

Employees can plan their hybrid workplace schedule using the Workplace Service Delivery for Mobile. They can reserve a space for a day or make bulk reservations using Workplace.

Employees can indicate their preferred office location \(office, remote, or visiting another office\), get desk suggestions based on their location preferences, add workplace services available for a location, add preferred collaborators and match their in-office days with collaborators in-office days to increase productivity and collaborate effectively. While reserving or viewing a space, employees can see if the selected space is part of a neighborhood.

**Note:** The option to add your workplace preferences and suggestions are also available on the Employee Center portal. Employees are expected to use the Workplace Service Delivery for Mobile app to reserve a space and to view or modify their preferred workplace locations and workplace schedule suggestions. Reserve a workspace using your mobile app before coming to the office. Get desk suggestions based on your preferred location, past and future reservations, proximity \(preferred collaborators\), favorite spaces, neighborhoods, and standard services.

When proposing a space to an employee for reservation, the application considers the following employee preferences and Space Suggestions table configurations:

-   Location preferences \(campus, building, floor, and neighborhood\)
-   Favorite space or spaces set by an employee
-   Past and future reservation data
-   Preferred collaborators
-   Start time and end time \(based on building time zone and Reservable module configuration for a location\).

Application also considers the following configurations when fetching your preferred workplace locations:

-   Filter and fetch locations from the Available Reservable Modules:
    -   Fetch locations from all Reservable Modules that are marked for workplace experience in the Space types property \[ sn\_wsd\_concierge.suggestions\_space\_types\]. For more information see [Properties installed with Workplace Concierge](../../workplace-concierge/reference/properties-installed-with-workplace-concierge.md)
    -   Verifies if it matches one of the allowed space types in the sn\_wsd\_concierge.suggestions\_space\_types property.
-   Filter locations by Building: For each Reservable Module, application checks if employee's preferred location exists in the specified building. It retains Reservable Modules that are available in a building.
-   Selects the Best Reservable Module:Looks at all matching Reservable modules and picks the best one based on the following:
    -   If a module has no **Max days in future** Reservable Module property restriction, it is selected.
    -   Then, it considers and selects the Reservable Module with the highest value in the **Max days in future** property configuration.

Administrators can configure the following to provide better workspace suggestions to employees:

-   Space Suggestions table configuration based on Suggestion types \(location, proximity, past and future reservation data, standard services, and collaborators\). Each of these Suggestion type is a given a weight value \(integer value\). While proposing a space to an employee, application takes into account these weight values and accordingly ranks it in the search results based on the priority or weightage given to a Suggestion type. If any of the spaces doesn't fulfill the criteria, the employee is shown the next available preferred space. If a preferred workspace is not available for an employee they are also given the option to manually search for available spaces using the advanced reservation option.

    For more information, see [Space suggestion Configuration](../../workplace-concierge/task/space-suggestion-configuration.md)

-   Employee presence configuration in Workplace Concierge

    For more information, see [Set Employee Presence](../../workplace-concierge/concept/use-workplace-concierge.md).

-   Properties enabled for Workplace suggestions and preferences.

    For more information, see [Properties installed with Workplace Concierge](../../workplace-concierge/reference/properties-installed-with-workplace-concierge.md).


For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

-   **[Manage your in-office presence preferences](../task/workplace-preferences-emp-center.md)**  
Employees can customize and manage their in-office or workday presence preferences.
-   **[Create a reservation for a day in Workplace](../task/manage-schedule-emp-center.md)**  
Reserve your preferred workspace in Workplace using the Workplace Service Delivery for Mobile app.
-   **[Create bulk reservations in Workplace](../task/mobile-workplace-bulk-reservations.md)**  
Create bulk reservations in Workplace using the Workplace Service Delivery for Mobile. Employee can manage multiple planned reservations from the Workplace page.
-   **[Review and edit your reservations in Workplace](../task/mobile-workplace-edit-rsv.md)**  
Update or edit reservations in Workplace using the Workplace Service Delivery for Mobile application. Update your location, date, and time of your existing reservations.

**Parent Topic:**[Workplace Service Delivery for Mobile](wsd-mobile-overview.md)

