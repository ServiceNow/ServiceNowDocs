---
title: Meeting scheduler AI agent
description: Now Assist for Integration Hub application provides standalone AI agent that mimics human-like intelligence to perform tasks in your ServiceNow instance. Meeting scheduler AI agent that can be used to organize Zoom or Teams meetings and create regular calendar events.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-11-04"
reading_time_minutes: 3
breadcrumb: [Available AI agents for Integration Hub, Now Assist for Integration Hub, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Meeting scheduler AI agent

Now Assist for Integration Hub application provides standalone AI agent that mimics human-like intelligence to perform tasks in your ServiceNow instance. Meeting scheduler AI agent that can be used to organize Zoom or Teams meetings and create regular calendar events.

This AI agent retrieves details of available rooms, details of the relevant users you want to invite such as, email address and timezone, finds an available time slot, creates a calendar event, and generates a Zoom URL for the meeting. The logged-in user who runs the AI agent is marked as the meeting's organiser or host. This AI agent can create 3 types of events:

-   A regular calendar event: This is a meeting placeholder with no URL and location.
-   Teams event: This a meeting where attendees can join Microsoft Teams meeting.
-   Zoom event: This a meeting where attendees can join the meeting using Zoom URL.

**Important:** To use this AI agent, ensure that you have activated the [Microsoft Exchange Online Spoke](../../integrationhub-store-spokes/concept/ms-exch-online-spoke.md) and configured the client credential alias. To generate Zoom URL for the meeting, you must activate and configure the [Zoom Spoke](../../integrationhub-store-spokes/concept/zoom-spoke.md).

In this example, Manish \(the logged-in user\) uses the Meeting scheduler AI agent from Now Assist panel to schedule a meeting with Vivek and provides details about the date, place, and meeting agenda. In this case, the AI agent schedules the meeting with most relevant user \(based on collaboration and organizational context\) named Vivek. If the AI agent is not able to retrieve details of the most relevant user from Microsoft Exchange Online, details of all users whose names match Vivek are retrieved from the ServiceNow User table \[sys\_user\] and displayed, and logged-in user Manish can choose the required user.

AI agent then displays the list of available time slots. Manish can select the feasible time slot. You can also view the AI steps. If a time slot at the mentioned time is unavailable, AI agents expands the search window to 2 days and displays the list of available slots.

![Schedule a meeting using the Meeting scheduler AI agent.](../images/na-meeting-scheduler-ai-agent1.jpg)

Manish can review the meeting details and proceed with scheduling the meeting.

![Summary of the meeting details.](../images/na-meeting-scheduler-ai-agent2.jpg)

Once the meeting is created, the details are displayed.

![Meeting details.](../images/na-meeting-scheduler-ai-agent3.jpg)

The event is added to your Outlook calendar and you can also view the meeting details in Outlook.

Using AI agent, Manish can also modify the meeting by adding room of the required capacity and in a specified location, adding more attendees, changes date or time, and so on.

![Event is added to the Outlook calendar.](../images/na-meeting-scheduler-ai-agent4.jpg)

![Event details on Outlook.](../images/na-meeting-scheduler-ai-agent5.jpg)

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

