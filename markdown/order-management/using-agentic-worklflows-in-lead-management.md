---
title: Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)
description: Use the Now Assist for Sales Force Automation \(SFA\) AI agent collection to complete tasks autonomously.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist for SFA]
---

# Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)

Use the Now Assist for Sales Force Automation \(SFA\) AI agent collection to complete tasks autonomously.

The Help nurture new leads agentic workflow works with a team of AI agents to assist you with managing the life cycle of leads, either independently or under supervision.

## Prerequisites to use an agentic workflow

The prerequisites to use an agentic workflow are as follows:

-   Make sure that the Now Assist panel is turned on.
-   Set up the work schedule for sales agents:
    -   Navigate to **All** &gt; **Agent schedule** &gt; **Work schedule**.
    -   Create a work schedule for sales agents.
-   Duplicate the agentic workflow and activate the triggers.

<table id="table_hzb_sd4_cfc"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help nurture new leads

</td><td>

-   Outlines the steps required to engage the lead with the sales agent.
-   Sends initial outreach and follow-up emails.
-   Retrieves emails, classifies the intent, and routes it to the right sales agent to take action.
-   Schedules, reschedules, or deletes the appointments based on sales agent availability.
-   Manages the leads who want to opt out or are uninterested.

</td><td>

-   Lead outreach AI agent
-   Inbound email AI agent
-   Appointment management AI agent
-   Lead disinterest AI agent

</td></tr></tbody>
</table>**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   **[Help nurture new leads agentic workflow](help-nurture-new-leads-agentic-workflow.md)**  
Use the Help nurture new leads agentic workflow to process the entire lead record process.

**Parent Topic:**[Now Assist for Sales Force Automation \(SFA\)](now-assist-for-sales-and-order-management-som.md)

