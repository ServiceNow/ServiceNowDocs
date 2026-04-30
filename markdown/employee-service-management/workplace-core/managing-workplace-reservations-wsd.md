---
title: Managing workplace reservations for employees
description: Reserve available areas or spaces for your employees and review pending reservation requests from employees in Workplace Core so you can verify physical distancing measures when they return to the workplace. Once you make reservations, employees are notified about the locations to which they have access. The Workplace Service Delivery also offers more advanced workplace reservation options in the Workplace Reservation Management application.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Managing workplace reservations for employees

Reserve available areas or spaces for your employees and review pending reservation requests from employees in Workplace Core so you can verify physical distancing measures when they return to the workplace. Once you make reservations, employees are notified about the locations to which they have access. The Workplace Service Delivery also offers more advanced workplace reservation options in the Workplace Reservation Management application.

## Creating workplace reservations for employees

-   **Reserving workplace areas**

    As a workplace manager, you can make reservations for employees for areas on the floors of your office buildings. When employees return to the office, they can work from any of the spaces from the reserved area. The number of employee reservations that you can make for an area of your workplace depend on the capacity defined for that area. If the **Capacity** field of an area is set to **0** or left empty, reservations cannot be made for that area.

-   **Creating a single space reservation**

    Using the shifts that you defined, you can create a space reservation for an employee for a single day or multiple days.

-   **Creating space reservations in bulk**

    You can generate in one action reservations for multiple employees who are assigned to a shift for a specific date range. For example, you can use this feature to create reservations for employees of a specific department who would all be assigned to the same shift.

-   **Child reservation records for employee space reservations**

    When you reserve a workplace for an employee, the reservation generates child reservation records for every applicable working day of the specified period. The applicable days are determined by the shift schedule that you select for this reservation. The reservation that you initially created acts as the parent reservation record.

    If a child reservation conflicts with an existing reservation for any day in the specified period, the child reservation is not created for that day. You can manually create a reservation for a different workplace for that day.

    For example, say you created a reservation for the workplace 2CN1612 for Mark Andrews in the afternoon shift from 06-01-2020 to 06-10-2020. Eight child reservation records for Mark Andrews for the workplace 2CN1612 would be created for each working day between 06-01-2020 and 06-10-2020. However, if a reservation for 2CN1612 on 06-08-2020 exists for another employee Jane Doe, the child reservation for Mark Andrews on 06-08-2020 is not created. You can manually create a reservation for Mark Andrews for a different workplace for 06-08-2020.

    If you update the details of a parent reservation later, all its child reservations except the ones with dates in the past are updated accordingly.


## Working with space reservation requests from employees

After an employee requests a workplace for a given date range and the manager approves the request, the application checks the availability of the requested space. If the workplace is unavailable for any or all days of the specified period, the request moves to the Pending state. As a workplace manager, you can review these pending reservation requests and allocate a different workplace to the employee to complete the request.

-   **[Define the capacity of workplace areas](../task/define-capacity-of-workplace-areas-wsd.md)**  
Set the capacity for areas of your workplace in Workplace Core to enable reservations for the area. The capacity ensures a limit to the workplace reservations for these areas so you can ensure safety guidelines.
-   **[Create workplace reservations for an employee](../task/reserve-workspaces-for-employees-wsd.md)**  
Create workplace reservations for an employee in the Workplace Core application using the shifts and shift schedules that you defined.
-   **[Create workplace reservations for multiple employees](../task/reserve-spaces-bulk-assignment-multiple-employees-wsd.md)**  
Automatically generate workplace reservations in bulk for all employees assigned to a shift for a single day or multiple days.
-   **[Review pending workspace reservation requests](../task/review-pending-reservation-requests.md)**  
Review pending workplace reservation requests from employees in Workplace Core and assign available workplaces to complete these requests.

**Parent Topic:**[Manage workplace safety activities](manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet](../task/import-excel-spreadsheet-workspace-data-wsd.md)

[Add a space type configuration](../task/add-space-type-configuration-wsd.md)

[Configure a workplace card](../task/configure-workplace-card.md)

[Block a workplace location](../task/block-workplace-location.md)

[Configure Workplace entity and entity types](workplace-entity.md)

[Enable favorites option for Workplace Service Portal](../task/confgure-favourites-option-for-ws-portal-wsd.md)

[Create a workplace performer criteria](../task/create-workplace-performer-criteria.md)

[Mapping employees to their designated workspaces](mapping-employees-to-existing-work-locations-wsd.md)

[Assign the workplace user role to employees](../task/assign-workplace-user-role-to-employees-of-a-location-wsd.md)

[Configuring shifts for your workplace](configuring-shifts-for-your-workplace-wsd.md)

[Managing workplace shifts that you own](managing-shifts-you-own-wsd.md)

[Setting and tracking arrivals at the workplace](scheduling-employees-arrival-to-the-workplace-wsd.md)

[Approve employee workplace reservation requests](../task/approve-workplace-reservation-requests-wsd.md)

[Managing workplace tasks](managing-workplace-maintenance-tasks.md)

[Workplace knowledge management](workplace-knowledge-mgmt-wsd.md)

[QR code management](qr-code-mgmt.md)

[Location migration](location-migration.md)

[View workplace service usage analytics with User Experience Analytics](../reference/appsee-intergration-wsd.md)

