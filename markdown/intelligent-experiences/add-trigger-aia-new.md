---
title: Add a trigger to an AI agent
description: In the guided setup for an AI agent, add triggers to run the AI agent automatically when certain conditions are met.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-trigger-aia-new.html
release: australia
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a trigger to an AI agent

In the guided setup for an AI agent, add triggers to run the AI agent automatically when certain conditions are met.

## Before you begin

Role required: sn\_aia.admin

## About this task

Adding a trigger is optional. If you want your AI agent to be used only in chats, you don't need to add a trigger. Only add a trigger if you want to invoke the AI agent automatically when some event occurs. Triggers can be added, edited, and removed at any time, and an agent with no trigger can still be used in chat.

A trigger determines how often and how widely the agent runs, so scope the condition before activating it. A condition that matches a large set of records invokes the agent for each of them, and a scheduled trigger processes a capped number of records per run, ten by default. [Test the agent manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) against a single record that meets the condition first.

If you don't want to add a trigger, skip to the next step, [Select channels and messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/channels-access-aia-new.md).

## Procedure

1.  Select a trigger type from the dropdown.

    The trigger type determines when the AI agent will be invoked.

2.  Enter details for the trigger.

    1.  Enter a name for the trigger.

    2.  Select the table on which the trigger will run.

    3.  Define the conditions that must be met for the trigger to activate.

        You must define at least one condition to create a trigger.

    4.  Enter the objective for the AI agent in the **Objective for this AI agent** field.

3.  Define user identity and data access for the trigger.

    1.  Choose how to define the user identity for this trigger.

        You can use an AI user identity, an existing table, or a new custom script. The user identity determines what data the AI agent can access when the trigger runs.

    2.  Select the AI user identity.

        **Note:** This trigger runs as a type of user identity with roles and associated data access rules it can impose on the AI agent. Review the AI agent's access rules to prevent any rule conflicts or gaps.

4.  Configure the trigger channel.

    1.  Select where the AI agent will launch.

        You can choose to launch the AI agent in the ServiceNow Otto panel or Virtual Agent.

    2.  Choose whether to show an alert to users by toggling **Show an alert to users**.

5.  Select **Save**.

    If you choose a scheduled trigger, additional options are available, such as the day of the week and time when you want the trigger to run.

    **Note:** When running a scheduled trigger, not every record is included in the execution. By default, the value is 10. If you want to change this number, you must set the **sn\_aia.max\_scheduled\_trigger\_query** system property to a different value.

    If you choose an email trigger, the target emails must exist on the Reply \[sys\_reply\] table. New emails aren’t available as triggers.

6.  Repeat the preceding steps for additional triggers.


## Result

You have added triggers to your AI agent to run it automatically under the specified conditions.

## What to do next

Scroll down to the next section of the guided setup, **Channel and display**, to [configure where the AI agent can be invoked and set processing messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/channels-access-aia-new.md).

