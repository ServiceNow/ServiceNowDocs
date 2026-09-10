---
title: Select channels and processing messages for an AI agent
description: In the guided setup for an AI agent, select whether to use it in the ServiceNow Otto panel or an Otto assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/channels-access-aia-new.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Select channels and processing messages for an AI agent

In the guided setup for an AI agent, select whether to use it in the ServiceNow Otto panel or an Otto assistant.

## Before you begin

Role required: sn\_aia.admin

## About this task

In this section of the AI agent guided setup, you configure where the AI agent can be invoked.

## Procedure

1.  Choose whether to allow users to invoke your AI agent in the ServiceNow Otto panel.

2.  Choose whether to engage via Otto assistants by toggling **Otto assistants**.

    If enabled, you must select which chat assistants have access to the AI agent. You can edit assistants using Assistant Designer. If the list is empty, you may need to create a new assistant.

    Assistant Designer is where chat and voice assistants are configured. The list of options is populated from it, so an assistant that does not exist there can't be selected. If the list is empty, or if you are configuring a voice agent and no voice assistant is offered, create the assistant in Assistant Designer first and return to this step.

3.  If you selected **Otto assistants** as a channel, set the AI agent's in-progress and completion messages.

    You can set an in-progress message, completion message, or both. If you don't want to use a specific type of message, unselect the toggle next to the message field.

    You can also use ServiceNow Otto to generate the messages for you by selecting **Generate messages**. You can change the messages after they're generated.

    This feature is only available for AI agents with the **Chat** modality.

4.  Select **Save**.


## Result

You have completed the channels section of the guided setup for creating an AI agent.

## What to do next

Move to the next section, [Manage memory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/map-ltm-aia-new.md).

