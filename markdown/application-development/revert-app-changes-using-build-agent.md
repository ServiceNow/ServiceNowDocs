---
title: Revert app changes with Build Agent
description: Restore your development to a previous state when you want to undo recent changes. Use checkpoints created during Build Agent conversations to revert both code and chat history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/revert-app-changes-using-build-agent.html
release: zurich
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [revert app changes, build agent checkpoint, restore checkpoint, undo changes build agent, chat history revert, build agent ServiceNow Studio, app development rollback, checkpoint restore, Now Assist, AI Agents, generative AI, agentic AI]
audience: administrator
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Revert app changes with Build Agent

Restore your development to a previous state when you want to undo recent changes. Use checkpoints created during Build Agent conversations to revert both code and chat history.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

2.  Select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel to open Build Agent.

3.  Select the chat that contains checkpoints you can revert to.

4.  View all available checkpoints by selecting the checkpoints icon \[Omitted image "sn-studio-ba-checkpoint-icon.png"\] Alt text:

    \[Omitted image "ba-chats-checkpoint.png"\] Alt text: Daily Planner Tracker chat panel showing completed Install and UI Diagnostics steps, each marked with a green check mark.

5.  Select the checkpoint you want to revert back to, and select **Restore**.

    \[Omitted image "ba-restore-button.png"\] Alt text: Daily Planner Tracker checkpoint panel with the Restore button highlighted.


## Result

Build Agent reverts your changes both in your application and in the chat.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

