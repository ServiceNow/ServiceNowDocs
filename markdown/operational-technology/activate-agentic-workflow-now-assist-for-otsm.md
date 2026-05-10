---
title: Activate an agentic workflow for Now Assist for Operational Technology Service Management \(OTSM\)
description: You must activate the agentic workflows from the AI Agent Studio. The Now Assist for OTSM agent included with the application and used in the agentic workflows are activated by default.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic AI for OTSM, Now Assist for OTSM, Operational Technology]
---

# Activate an agentic workflow for Now Assist for Operational Technology Service Management \(OTSM\)

You must activate the agentic workflows from the AI Agent Studio. The Now Assist for OTSM agent included with the application and used in the agentic workflows are activated by default.

## Before you begin

Ensure that the following skills are activated for Now Assist for OTSM:

-   OT incident summarization skill
-   OT resolution notes generation skill

For more information about activating the skills, see [Configure Now Assist for OTSM](../concept/configuring-now-assist-otsm.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  Under the **Agentic workflows** tab, select the **Generate OT KB articles** agentic workflow.

    **Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

3.  In the **Define key requirements** screen, review and update the information as needed then select **Save and Continue**.

    **Note:** In the Define who can access the agentic workflow section, a user must have the **sn\_ot\_incident\_write** role to access the agentic workflow.

4.  In the **Add a preferred trigger** screen, ensure the **OT incident upon being resolved** trigger is set to **Active** by selecting the trigger to open the **Edit trigger** window and turning on the **Active** toggle.

5.  In the **Select a UI display** screen next to the **Now Assist panel** option, select the **Display** toggle so that the conversation with the agent is displayed in the Now Assist panel.

6.  Select **Save and test**.

    The agent can now execute the request for the agentic workflow.


