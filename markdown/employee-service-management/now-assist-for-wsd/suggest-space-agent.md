---
title: Using the workplace collaboration Agent for space suggestions
description: The Workplace Collaboration Agent provides insights on your team members in-office attendance. Based on this information, the reservation agent finds and reserves a space for reservation and collaboration. The collaboration agent considers your colleague's in-office days, location, and suggests a space for collaboration when you are in office.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Using the workplace collaboration Agent for space suggestions

The Workplace Collaboration Agent provides insights on your team members in-office attendance. Based on this information, the reservation agent finds and reserves a space for reservation and collaboration. The collaboration agent considers your colleague's in-office days, location, and suggests a space for collaboration when you are in office.

The Create a reservation agent helps employees find a space for reservation. The Workplace collaboration agent provides suggestions for reservations based on colleague’s attendance and proximity. Employees can find and reserve a workspace near a colleague. The collaboration agent helps in improving collaboration and workplace productivity. The collaboration agent provides insights on your colleagues in-office days.

**Note:** Desks reservations are supported by the Workplace collaboration agent.

When providing suggestions for collaboration, the Collaboration agent prioritizes the Employee Presence Exceptions data first, then it checks for Employee Presence Routine, and lastly, it considers your current reservations. It gives priority to Employee Presence Exceptions data over Employee Presence Routine and current reservations in the system. If employee's current reservation data and location in available and no workplace presence information is there, the agent prioritizes employee's current reservations over workplace location while suggesting spaces for collaboration. For more information, see [Workplace Concierge](../../workplace-concierge/concept/workplace-concierge-feat.md).

Your collaborators can be categorized as:

-   Employee collaborators information derived from Employee Presence Exceptions and Employee Presence Routine in Workplace Concierge.
-   Collaborator information is also derived from the invitees that you frequently add to your reservations with while making a reservation.
-   Colleagues with whom you collaborate frequently. Your team members and your manager. If you are a manager, your collaborators are your team members reporting to you.

The workplace collaboration agent improves employee's reservation and collaboration experience by providing the following:

-   Determines your collaborators \(your team members, your presence collaborators \(if available\), and your reservation attendees\).
-   Provides insights when collaborators are in office.
-   Provides insights about team members who are in office for a specific day.
-   Helps to reserve a space near a colleague.
-   When multiple collaborators with same name exists, the collaboration agent asks employees to select their preferred collaborator from a list of similar names. The collaboration agent makes suggestions and tries to find your preferred collaborator. For example, if there are two Abel in your organization, but you frequently collaborate with Abel Tuter, the collaboration agent selects Abel Tuter as your preferred collaborator.
-   Provides ability to change the workplace preferences of an employee \(remote to in-office and vice versa\). If employees change their remote day to in-office day, an exception is created by the application in the Employee Presence Exceptions table.

**Note:** If you are planning to sit near a colleague, and if your colleague has a desk reservation for one hour and doesn't have an All day reservation, you can make a reservation for one-hour only. If an employee doesn't have any Employee Presence Exceptions and has no reservations made for a day while in office, the collaboration agent prioritizes the employee's workplace profile location and spaces around that location is suggested to the employee for collaboration.

-   **[Get space suggestions using the Workplace collaboration agent](../task/collaboration-agent.md)**  
The Workplace collaboration agent provides space recommendations and insights for collaboration based on employee's workplace presence data, team members or frequent collaborators, attendees in your reservation, and workplace profile \(assigned space\).

**Parent Topic:**[Using Now Assist in Virtual Agent](create-rsv-agent-ovw.md)

**Related topics**  


[Making reservations using the Create a reservation agent](using-reservation-agent.md)

[Set Employee Presence](../../workplace-concierge/concept/use-workplace-concierge.md)

[Components installed with Workplace Concierge](../../workplace-concierge/reference/components-installed-with-workplace-concierge.md)

