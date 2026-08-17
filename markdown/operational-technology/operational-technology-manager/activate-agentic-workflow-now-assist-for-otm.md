---
title: Activate the Import OT device spreadsheet into OT CMDB agentic workflow
description: You must activate the agentic workflow from the AI Agent Studio. The Operational Technology \(OT\) Manager Foundation agent included with the application and used in the agentic workflows is active by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/activate-agentic-workflow-now-assist-for-otm.html
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the OT Manager Foundation, Configure, Operational Technology Manager, Operational Technology]
---

# Activate the Import OT device spreadsheet into OT CMDB agentic workflow

You must activate the agentic workflow from the AI Agent Studio. The Operational Technology \(OT\) Manager Foundation agent included with the application and used in the agentic workflows is active by default.

## Before you begin

Role required: sn\_aia.admin

## About this task

**Important:** This agentic workflow is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  Under the **Agentic workflows** tab, select the **Import OT device spreadsheet into OT CMDB** agentic workflow.

3.  In the **Define key requirements** screen, review and update the information as needed then select **Save and Continue**.

    **Note:** In the Define who can access the agentic workflow section for the Import OT device spreadsheet into OT CMDB agentic workflow, a user must have the ot\_excel\_import\_user role to access the agentic workflow.

4.  In the **Select a UI display** screen next to the **ServiceNow Otto panel** option, select the **Display** toggle to show the conversation with the agent in the panel.

5.  Select **Save and test**.

6.  Verify the **Status** toggle is on to confirm the OT Excel import task AI agent is active and running.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  Under the **AI agents** tab, select the **OT Excel import task AI agent**.

    3.  In the **Toggle display** screen, select the **Status** toggle if the toggle isn't already selected.


**Parent Topic:**[Configuring the OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/configuring-na-otm.md)

