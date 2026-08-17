---
title: Activate an agentic workflow for ServiceNow Otto for Operational Technology \(OT\) Service Management
description: Activate the agentic workflows for ServiceNow Otto for Operational Technology \(OT\) Service Management from the AI Agent Studio so that the AI agents can execute requests autonomously. The ServiceNow Otto for OT Service Management agents included with the application are activated by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-incident-management/activate-agentic-workflow-now-assist-for-otsm.html
release: australia
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Agentic AI for Operational Technology Service Management, Use, Operational Technology Incident Management, Operational Technology]
---

# Activate an agentic workflow for ServiceNow Otto for Operational Technology \(OT\) Service Management

Activate the agentic workflows for ServiceNow Otto for Operational Technology \(OT\) Service Management from the AI Agent Studio so that the AI agents can execute requests autonomously. The ServiceNow Otto for OT Service Management agents included with the application are activated by default.

## Before you begin

Verify that the following skills are activated for ServiceNow Otto for OT Service Management:

-   OT incident summarization skill
-   OT resolution notes generation skill

For more information about activating the skills, see [Configure Now Assist for OTSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-incident-management/configuring-now-assist-otsm.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  Under the **Agentic workflows** tab, select the **Generate OT KB articles** agentic workflow.

    **Important:** This agentic workflow is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

3.  In the **Define key requirements** screen, review and update the information as needed then select **Save and Continue**.

    **Note:** In the Define who can access the agentic workflow section, a user must have the sn\_ot\_incident\_write role to access the agentic workflow.

4.  In the **Add a preferred trigger** screen, ensure the **OT incident upon being resolved** trigger is set to **Active** by selecting the trigger to open the **Edit trigger** window and turning on the **Active** toggle.

5.  In the **Select a UI display** screen next to the **ServiceNow Otto panel** option, select the **Display** toggle to display the conversation with the agent in the ServiceNowOtto panel.

6.  Select **Save and test**.

    The agent can now execute the request for the agentic workflow.


**Parent Topic:**[Agentic AI for Operational Technology Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-incident-management/now-assist-otsm-use-cases.md)

