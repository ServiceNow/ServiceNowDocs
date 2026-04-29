---
title: Platform Issue Readiness AI agent
description: The Issue Readiness AI agent analyzes the current state of a task to assess and determines whether it is ready to be worked on.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [task readiness]
breadcrumb: [Platform AI agents, Now Assist AI assets, Enable AI experiences]
---

# Platform Issue Readiness AI agent

The Issue Readiness AI agent analyzes the current state of a task to assess and determines whether it is ready to be worked on.

## Issue Readiness AI agent overview

The Issue Readiness AI agent takes the information on a record, analyzes it, determines whether all relevant information is present on the record, and makes a decision about whether the task is ready for work. Using the AI agent can help fulfillers focus on actionable work by reducing manual checks for missing supporting details or back-and-forth conversations. Instead of having to check whether tasks are waiting on pending approvals or unanswered questions, fulfillers can see what actionable work is available and prioritize it.

## Prerequisites and setup

To access this AI agent, you must have Now Assist Agent for Platform installed on your instance, which is installed with any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

## Role masking

Required role:

AI agents use [role masking](aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](../task/define-sec-controls-aia.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to evaluate for readiness. For example, you can add the itil role to the AI agent's list of approved roles so that it can access Incident records.

## Accessing the Issue Readiness AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Go to the **AI Agents** tab.
3.  Select **Issue Readiness**.

## Testing the Issue Readiness AI agent

You can manually test the AI agent execution on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aia.md). Select the AI agent, start a manual test, and use utterances in the Task field like the ones below.

## Sample utterances

After the agent has been activated in AI Agent Studio, enter phrases such as the following or similar queries to run the AI Agent in Virtual Agent, the Now Assist panel, or Microsoft Teams.

-   Is INC001234 ready for work?
-   Do I have enough details on CSM0001234 to start?

**Parent Topic:**[Platform AI agents](platform-ai-agents.md)

