---
title: Reserve a space using the reservation agent
description: The Create a reservation agent enables employees to reserve a space with a single prompt query or utterance.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Making reservations using the Create a reservation agent, Using Now Assist in Virtual Agent, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Reserve a space using the reservation agent

The Create a reservation agent enables employees to reserve a space with a single prompt query or utterance.

## Before you begin

Make sure that you have installed and configured the following applications:

-   Now Assist in Virtual Agent.

    Confirm that the enhanced chat is configured for the Employee Center portal by virtual\_agent\_admin. Select Employee Center from the Portals tab and select the enhanced chat. For more information, see [Display your chat assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).

-   Workplace Reservation Management
-   Workplace Concierge
-   Workplace Indoor Mapping
-   Workplace Core

**Note:** Adding workplace services to a reservation, creating group reservations, multi-building reservations, making a reservation by using the Browse near a person reservable path option, or recurring reservations are currently not supported by the workplace reservation AI agent.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  From the Employee Center portal home page, select the Now Assist in Virtual Agent chat interface.

    The Virtual Agent shows a greeting message and provides an explanation of what employees can expect.

3.  Enter an utterance or query to reserve a space.

    Employees can quickly reserve a space using a single utterance or prompt. For example, enter `I want to reserve a workstation for the afternoon. What is available?`.

    While the LLM processes the utterance, animated dots in the chat window let employees know that the reservation agent is working on their request. After you enter an utterance and a search result is found, a synthesized response may appear. A synthesized response includes a brief summary of the requested information and search results.

    ![Now Assist for Virtual Agent showing employee preferred space for reservation.](../image/wsd-now-assist-virtual-agent-start-resv.png)

    Each response includes feedback icons. The user can indicate if the response was helpful by selecting thumbs up or select thumbs down if the response wasn't helpful.

4.  The reservation agent shows an available building location for reservation and asks employees to confirm the space selection.

    **Note:** Selecting **No** prompts the reservation agent to fetch another location or a space for reservation. At a time, the reservation agent shows three space suggestions.

    ![Now Assist for Virtual agent shows maximum of three preferred spaces for reservation](../image/wsd-creat-rsv-agent-two.png)

5.  The reservation displays a navigational link to the Advanced Reservation portal when it is not able to find a suitable space.

    It provides the link to the Reservation portal when employees don't select a space from the suggested spaces shown by the reservation agent. At a time, the reservation agent provides three space suggestions. Employees can search for spaces manually on the reservation portal page and reserve a space.

    ![Agent confirms that it cannot find a space for the employee and provides a navigation link to the Advanced Reservation Portal.](../image/wsd-rsv-create-agent-five-rsv-portal-link.png)

6.  When the request is complete, Now Assist in Virtual Agent chat interface displays a message to confirm if employees need any additional help from the Virtual Agent.

    ![Agent completes the request and asks employees to confirm if they require any other help from it.](../image/wsd-create-rsv-agent-last-step.png)


**Parent Topic:**[Making reservations using the Create a reservation agent](../concept/using-reservation-agent.md)

