---
title: Implement an automation opportunity \(Lux UI\)
description: Deploy a matched AI agent or a new agent to automate a resolution for an identified automation opportunity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-implement-automation-opportunity.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [AI Agent Advisor in AI Admin Center, Use, AI Agent Advisor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Implement an automation opportunity \(Lux UI\)

Deploy a matched AI agent or a new agent to automate a resolution for an identified automation opportunity.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to implement an automation opportunity with AI Agent Advisor.

Each automation opportunity includes a set of recommended resolution steps that describe how to automate the identified opportunity. AI Agent Advisor also maps each resolution step to an existing AI agent on your platform when a match is available. Review the details of an opportunity before deciding whether to deploy an agent for it.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  In the **Automation opportunities** section of the home page or on the Automation opportunities page, select an automation opportunity to view its details.

    The opportunity opens in a side panel showing the opportunity details. The panel displays summary information for the opportunity along with any resolution steps, example records, and matching agents, depending on the opportunity.

    \[Omitted image "ai-admin-center-lux-advisor-details-panel-1.png"\] Alt text: Side panel showing resolution steps and example records for an opportunity.

    For an opportunity that has a matching prebuilt AI agent, the panel displays the agent description and the matched automation opportunities that the AI agent can support. You can select a matched opportunity to view its description.

    \[Omitted image "ai-admin-center-lux-advisor-details-match.png"\] Alt text: Side panel showing a matching prebuilt AI agent and its matched opportunities.

    For more information on finding an automation opportunity, see [View your automation opportunities \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-view-automation-opportunities.md).

3.  Select **View sample issues** to review records from the source table.

    Select a record number to open the record and view its details.

4.  Expand the **Resolution steps** section to review and edit the steps for accuracy and completeness in planning your AI agent.

5.  Choose whether the AI agent will communicate as a **Chat Agent** or **Voice Agent**.

6.  Select **View all steps and tools** to see all the resolution steps.

    The **Resolution steps** screen shows the implementation steps and the matched AI tools for each step.

7.  When the steps are ready to implement for a custom AI agent, select **Build in AI Agent Studio**.

    For an opportunity that has a matching prebuilt AI agent, select **Manage in AI Agent Studio**.

    AI Agent Studio opens.

8.  Complete the development of the AI agent using AI Agent Studio capabilities.

    The resolution steps are mapped to the set of instructions and added as tools for the AI agent.

    For more information, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-aia-new.md).


**Parent Topic:**[AI Agent Advisor in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/using-ai-agent-advisor-in-now-assist-center.md)

