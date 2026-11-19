---
title: Use the Research AI agent activity
description: Use the Research AI agent activity in the Research stage of the Case Playbook for Complaints to invoke the Complaint Case Research AI agent and review its recommendations without leaving the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/now-assist-for-csm/acc-complaint-case-handling-research-activity.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 1
breadcrumb: [Accelerate complaint case handling collection, Use agentic AI in CSM, ServiceNow Otto for CSM, Customer Service Management]
---

# Use the Research AI agent activity

Use the **Research AI agent** activity in the Research stage of the Case Playbook for Complaints to invoke the Complaint Case Research AI agent and review its recommendations without leaving the playbook.

## About this task

The **Research AI agent** activity embeds the Complaint Case Research AI agent directly into the Case Playbook for Complaints. It's the first activity displayed under the **Research** stage.

By default, this activity is included in the playbook when the Complaint Case Research AI Agent trigger is inactive in the Accelerate Complaint Case Handling agentic workflow. For more information about the trigger, see [Configure AI Agents for CSM - Complaint Case workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/now-assist-for-csm/acc-complaint-case-handling-agentic-wkfl.md). If you don't want to include this activity, you can edit the complaint playbook to remove it.

## Before you begin

Role required: sn\_now\_canvas\_ai.interactive\_view\_user

Only the user who invokes the agent can interact with the activity and view the output of the AI agent's execution.

## Procedure

1.  Open a complaint case and go to the **Playbook** tab.

2.  In the **Research** stage, select the **Research AI agent** activity.

3.  Select **Start Now Assist** to invoke the agent.

    The agent reviews the case and displays a recommended plan, such as case tasks based on similar complaint cases.

4.  Reply with **Yes** or **No** to accept or decline the recommendations.

    **Note:**

    If you reply with **Yes**, the recommended case tasks are the case tasks that the agent creates.


