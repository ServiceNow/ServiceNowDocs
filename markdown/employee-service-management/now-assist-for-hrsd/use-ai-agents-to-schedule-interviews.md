---
title: Schedule interviews agentic workflow
description: Use the schedule interviews agentic workflow to collect necessary inputs from recruiters or recruitment coordinators and schedule interviews seamlessly from the Now Assist panel.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 1
keywords: [AI agents, Agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Schedule interviews agentic workflow

Use the schedule interviews agentic workflow to collect necessary inputs from recruiters or recruitment coordinators and schedule interviews seamlessly from the Now Assist panel.

## Schedule interviews agentic workflow overview

Use the schedule interviews agentic workflow to automate the interview scheduling process. This agentic workflow manages all tasks, including gathering inputs to understand the context, finding overlapping slots, drafting personalized messages, and creating and sending invites. The agentic workflow also creates interview records to verify that everything is easily trackable.

To be able to use the agentic workflow, you must do the following:

-   In the HR Talent AI Agent Collection plugin, update the status of the ExchangeCalendarUtil restricted caller access \(RCA\) record from Requested to Allowed. This update grants access to the Outlook API calls.

    **Note:** This update is only applicable if the Microsoft Outlook integration is available in your instance.

-   For panel interviews, the sn\_talent\_aia.common\_slot\_threshold property defines the confidence level for common slot identification. This value is set to 80 by default and can be updated as required.

To access the agentic workflow to review or customize it as an admin:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Schedule interviews**.

To access the agentic workflow as a recruiter or recruitment coordinator, initiate it from the Now Assist panel.

## Schedule interviews AI agents

The following table lists the agent that is part of the schedule interviews agentic workflow.

<table id="table_szl_yq4_lgc"><thead><tr><th>

AI Agent

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Interview schedule AI agent

</td><td>

Gathers input from the recruiter or recruitment coordinator to obtain the necessary details for scheduling interviews and then identifies the best time slot options for interviews. It uses a combination of attendees' declared scheduling preferences and available calendar time slots to present a prioritized order of time slots that reduce the likelihood of rescheduling. When beneficial, it recommends the self-scheduling option, which presents applicants with panelist-compatible time slots sorted by confidence level, allowing them to select their preferred time.

Next, it drafts personalized email content for applicants to include in the interview invite. Users can choose to start from a preconfigured template or use AI to generate the content. Finally, it creates and shares invites by compiling the confirmed information from the previous steps, and completes the scheduling process by creating an interview record to ensure trackability.

</td></tr></tbody>
</table>