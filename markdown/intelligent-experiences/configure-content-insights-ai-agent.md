---
title: Configure Content insights AI agent
description: Configure the Content Insights AI agent to control which roles can access it, how it is triggered, and which chat assistants surface it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-content-insights-ai-agent.html
release: australia
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
keywords: [Content Insights, AI agent, configure]
breadcrumb: [Information Extraction skill, Configure, Content Understanding, Enable AI experiences]
---

# Configure Content insights AI agent

Configure the Content Insights AI agent to control which roles can access it, how it is triggered, and which chat assistants surface it.

## Before you begin

Role required: AI Agent Admin \[sn\_aia.admin\]

## About this task

The Content Insights AI agent requires configuration before users can interact with it. You define access roles, triggers, and the chat assistants that surface the agent.

## Procedure

1.  Open AI Agent Studio.

2.  Locate the Content Insights AI agent.

    Select **Explore All** or **AI agents** to browse the list of agents, or search for the agent by name.

3.  Select the Content Insights AI agent.

4.  From the options menu \(\[Omitted image "cu-options-menu.png"\] Alt text: Options menu icon\), select **Duplicate** to create an editable copy.

    **Note:** All edits apply to the copy. The original agent remains unchanged.

5.  In the **Define security controls** section, select **Define user access**.

6.  Select edit \(\[Omitted image "cu-edit.png"\] Alt text: Edit icon\).

    The Edit ACL dialog opens.

7.  Add the roles that require access to the agent, and then select **Update**.

    Determine which roles on your instance must use the agent, and add those roles. For example, you might add a requester role or a fulfiller role.

8.  In the **Add triggers** section, select **Add triggers**.

    The Add a trigger dialog opens.

9.  Select a trigger and then select **Add**.

    You add triggers to define the conditions or events that start the agent. For example, add a trigger for an inbound email.

10. In the **Select channels and status** section, configure the channels and status for the agent.

    1.  Turn on the **Allow** toggle to enable the agent on ServiceNow Otto for Virtual Agent.

    2.  In the **Chat assistants** field, select an assistant to add the agent to.

11. Select **Save and test**.

12. Test and deploy the agent.

    1.  Run a test on the testing page.

    2.  Deploy the agent.


## Result

The Content Insights AI agent is deployed and available to users with the access roles you defined. The agent activates through the triggers and channels you configured.

