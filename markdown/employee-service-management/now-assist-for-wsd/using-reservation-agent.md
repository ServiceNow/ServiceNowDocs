---
title: Making reservations using the Create a reservation agent
description: The Create a reservation agent enables employees to find an available space and create workplace reservations quickly. Employees can interact with the reservation agent using the Now Assist in Virtual Agent enhanced chat interface in Employee Center. They can also use the Now Mobile chat interface for interacting with the Virtual Agent.
locale: en-US
release: yokohama
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-01-11"
reading_time_minutes: 4
breadcrumb: [Using Now Assist in Virtual Agent, Workplace Service Delivery, Employee Service Management]
---

# Making reservations using the Create a reservation agent

The Create a reservation agent enables employees to find an available space and create workplace reservations quickly. Employees can interact with the reservation agent using the Now Assist in Virtual Agent enhanced chat interface in Employee Center. They can also use the Now Mobile® chat interface for interacting with the Virtual Agent.

The reservation agent estimates where the employees are located for a given workday. It considers their workplace profile \(assigned space to an employee\) and the spaces they most frequently reserve. Based on this information, the reservation agent finds and suggests spaces for reservations. The employees can suggest a different space, time or location using the chat interface. The agent also provides employees with an option to select a space manually from the reservation portal. The option to select a space manually is provided by the reservation agent when it is not able to find a space that is requested by the employee or when the employee wants to search for a different space than what is suggested by the reservation agent.

While searching for a space and making a reservation, the reservation agent considers the following:

-   Date and time information when the employee is requesting to book a space for reservation.

    For example, if the reservation agent doesn't find a date in the utterance "Reserve a space for me", the reservation agent reserves a space for the current date and for all day. If time is provided, it tries to find an available space for the suggested time. For example, if you enter the prompt “Reserve a space for me from 3 pm to 4 pm” in the Virtual Agent chat interface, it reserves a space for you from 3 pm to 4 pm.

    If no time is provided, it reserves a space for All day. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

    -   When the **All day meaning** Reservable module configuration value is set to **Office hours**, the reservation agent makes a reservation for daytime. For example, if the office Start time is 9 am and End time is 5 pm, the reservation agent reserves a space based on the start day and end day reservation properties.
    -   **All day meaning** Reservable Module value set to **Full day**.

        The reservation agent reserves a space based on the 24-hour clock or 12-hour clock notations. For 24-hour time format, it reserves the space from \(00 to 23.59\). For 12-hour time format, it reserves a space from \(9 am- 12 pm\) and evening \(1 pm to 5 pm\) based on the office working hours. For more information, see [Properties installed with Workplace Reservation Management](../../wsd-reservation-management/reference/properties-installed-with-wsd-reservation-mgmt.md).

-   **Max days in future** value in the Reservable Module. This value is set by your workplace administrator. The reservation agent reserves a space and provides dates for reservation based on the highest value given in the **Max days in future** configuration. If the **Max days in future** value is empty, the reservation agent provides a navigational link to the Advanced Reservation Portal. Employees can select the link to navigate to the Advanced Reservation portal and select a space manually. For more information, see [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).
-   The reservation agent also checks the Workplace Concierge employee presence dashboard for insights on employees in-office days. For more information, see [Configure workplace space suggestions for employees](../../workplace-concierge/concept/configure-workplace-suggestions.md).

    If Workplace Concierge isn’t installed, the reservation agent uses the workplace profile information \(assigned space to an employee\) to reserve an available space. It uses the primary location that is set for an employee to fetch the building location and available spaces for reservation.

    If the workplace profile isn’t available, the reservation agent considers the past reservation data of an employee and shows space suggestions based on the past reservation data \(most frequently reserved spaces, date, and time\). If the reservation agent isn’t able to fetch or predict a location, it asks employees to enter manually their preferred workplace locations in the Virtual Agent chat interface. It provides space suggestions based on employee prompt inputs.

-   **Workplace Locations** tab information in a Reservable Module. The application provides suggestions from the configured workplace locations only. For example, if about 10 building locations are added to the Workplace Locations tab in a Reservable Module, employees can select a space only from one of these 10 buildings for reservation. Employees can’t reserve a space, which isn’t added to the workplace locations. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

