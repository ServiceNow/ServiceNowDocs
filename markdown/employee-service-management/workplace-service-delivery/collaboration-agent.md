---
title: Get space suggestions using the collaboration agent
description: The Workplace collaboration agent provides space recommendations and insights for collaboration based on employee's workplace presence data, team members or frequent collaborators, attendees in your reservation, and workplace profile \(assigned space\).
locale: en-US
release: xanadu
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: task
last_updated: "2026-01-09"
reading_time_minutes: 6
breadcrumb: [Using the Workplace collaboration Agent for space suggestions, Using Now Assist in Virtual Agent, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Get space suggestions using the collaboration agent

The Workplace collaboration agent provides space recommendations and insights for collaboration based on employee's workplace presence data, team members or frequent collaborators, attendees in your reservation, and workplace profile \(assigned space\).

## Before you begin

The collaboration agent provides employees with insights about colleagues or team members who are in office. It makes space suggestions based on your collaboration requirements.

Make sure that you have installed and configured the following applications:

-   Now Assist in Virtual Agent.

    Confirm that the enhanced chat is configured for the Employee Center portal by virtual\_agent\_admin. Select Employee Center from the Portals tab and select the enhanced chat. For more information, see [Display your assistant on a portal or channel](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

-   Workplace Reservation Management
-   Workplace Concierge
-   Workplace Indoor Mapping
-   Workplace Core

**Note:** Adding workplace services to a reservation, creating group reservations, multi-building reservations, or recurring reservations are currently not supported by the Workplace Collaboration Agent. Collabration agent supports Desks reservations.

Employees can invoke the collaboration agent by initiating a chat with the Now Assist in Virtual Agent from the Employee Service Center portal.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  From the Employee Center home page, select the search box to initiate chat with Now Assist in Virtual Agent.

    The Virtual Agent shows a greeting message and provides an explanation of what employees can expect.

3.  Enter an utterance or query to reserve a space.

    Employees can quickly reserve a space using a single utterance or prompt. For example, enter `Reserve a space for me near Abel Tuter`.

    While the LLM processes the utterance, animated dots in the chat window let employees know that the bot is working on their request. After you enter an utterance and a search result is found, a synthesized response may appear. A synthesized response includes a brief summary of the requested information and search results.

    ![Now Assist for Virtual Agent showing employee preferred space for reservation.](../image/wsd-now-assist-virtual-agent-start-resv.png)

    The Virtual Agent response includes feedback icons. Employees can indicate if the response was helpful by selecting thumbs up or select thumbs down if the response wasn't helpful.

4.  The collaboration provides insights about team members who are in office.

    It suggests a space based on your collaboration requirements.The Agent shows an available building location for reservation and asks employees to confirm the space selection.

    **Note:** Selecting **No** prompts the agent to fetch another location or a space for reservation.

    For example, if you enter "I am visiting office campus in Italy and want to collaborate with Abel. What space is available?

    The agent may respond as following:

    It is great to see you in the office and connect with your collaborators! Abel will be in the office next Tuesday.We have found an available workspace for you:

    -   ﻿﻿Space Name: B1-03-01
    -   ﻿﻿Building: AMS-B1
    -   Date: Thursday, 30th October 202
    -   Time: 1:00pm to 5:00pm \(Europe/Amsterdam\)
    Would you like to proceed with reserving this workspace?

    ![Collaboration agent getting information to reserve a space near a colleague.](../image/now-assist-collab-agent-rsv-space-one.png)

    ![Collaboration agent showing in-office presence information for a colleague.](../image/now-assist-collab-agent-presence-two.png)

    If you respond "yes, that sounds good", the agent creates a reservation and sends you a notification.

5.  Chat with the collaboration agent to know which of your team members are available in your in office days.

    |Employee Prompt|Agent responses|
    |---------------|---------------|
    |I am visiting the Hyderabad office and want to collaborate with Sarah. What is the best day?|Sarah is in office on Tuesdays and Wednesdays.|
    |Which space is available for Tuesday?|Space A in Hyderabad is available.|
    |Book this space for me|I have reserved this space for you.|

    The Collaboration agent also shares insights on the team members available on a particular day. For example, "Who will be in office on Friday? You can also get insights on a team member if they are visiting office "Is Daniel coming to office today?". The agent also makes a reservation for you for a specified day near a team member. "

    ![Collaboration Agent fetiching information about team members who are present in office. Agentic Studio showing decision logs for collaboration agent.](../image/now-assist-collab-agentic-studio-activity-one.png)

6.  Make a reservation for a specified day near a team member.

    ![Collaboration agent showing best available space for reservation near a colleague.](../image/now-assist-collab-agent-reservation-one-hour.png)

<table id="table_q4w_f4h_xhc"><thead><tr><th>

Employee Prompt

</th><th>

Agent responses

</th></tr></thead><tbody><tr><td>

Can you book me a space near Sarah for Jan 30?

</td><td>

According to Sarah's presence information, Sarah is office on this day, but has not reserved a space as of now. Sarah's office presence schedule is:

-   Monday: Remote
-   Tuesday: In office


</td></tr><tr><td>

Sounds good.

</td><td>

Space B is available, which is near the space Sarah normally reserves. Shall I reserve this?

</td></tr><tr><td>

Book this space for me

</td><td>

I have reserved this space for you.

</td></tr></tbody>
</table>    -   While executing the Workflow, the collaboration agent makes the following considerations and checks.

        -   Location: Employee's building location is derived using the following logic:
            -   The building and floor for today's \(current date\) reservation.
            -   Employee presence information
            -   Workplace profile primary location or assigned space

                In case, no desks reservation are found, the collaboration agent checks if there is a workplace profile and a location \(desk\) assigned to an employee while making space suggestions near a collaborator. If workplace profile primary location is not available, the collaboration agent determines the collaborators location \(building/space\) based on the employee's workplace presence information.

        -   When the employee enters a name, the collaboration agent tries to identify the collaborator. It takes into account the following factors:
            -   Your team \(this includes your manager. If you are a manager and not an individual contributor, the agent also considers employees reporting to you as your collaborators\).
            -   Workplace presence Collaborator information. This includes Employee Presence Routine and Employee Presence Exceptions. For more information, see [Components installed with Workplace Concierge](../../workplace-concierge/reference/components-installed-with-workplace-concierge.md) and [Set Employee Presence](../../workplace-concierge/concept/use-workplace-concierge.md)
            -   Your current reservations in the system and invitees added by you.
            -   Your workplace profile and the primary location assigned to you.
            -   If multiple colleagues are found with the same name, the agent allows you to select a colleague from a list of employee names.
    -   Time: All day reservation is considered first, and then, the reservation Start time and End time reservation is taken into consideration. For more information, see [Properties installed with Workplace Reservation Management](../../wsd-reservation-management/reference/properties-installed-with-wsd-reservation-mgmt.md).

        In the case multiple desk reservations exist, earliest start time is used to find an available space for collaboration.

    -   Date: If no date is provided, the collaboration agent assumes that the reservation is for today or the current date. By default, All day reservation is suggested. Employees can change this and suggest a different start time and end time for a reservation.
    **Note:** Adding of workplace services \(projectors, catering, and so on\) are not supported by the Collaboration agent.

7.  Collaboration Agent provides a link to the Reservation portal if it is unable to find a suitable space for you.

    You can navigate to the Reservation portal and manually search for your preferred space.

8.  When the request is complete, Virtual Agent displays a message to confirm if any additional help is required.


