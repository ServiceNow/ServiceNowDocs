---
title: Revert app changes with Build Agent
description: Restore your development to a previous state when you want to undo recent changes. Use checkpoints created during Build Agent conversations to revert both code and chat history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/revert-app-changes-using-build-agent.html
release: zurich
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Revert app changes with Build Agent

Restore your development to a previous state when you want to undo recent changes. Use checkpoints created during Build Agent conversations to revert both code and chat history.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

2.  Open Build Agent.

    **Note:** The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the corner of your browser.

3.  Open a previous chat to revert your changes by selecting the chats icon \[Omitted image "sn-studio-ba-chats-icon.png"\] Alt text:.

    \[Omitted image "ba-chats-selection.png"\] Alt text: Build Agent panel with chat selection icon

4.  Select the chat that contains checkpoints you can revert to.

5.  View all available checkpoints by selecting the checkpoints icon \[Omitted image "sn-studio-ba-checkpoint-icon.png"\] Alt text:

    \[Omitted image "ba-chats-checkpoint.png"\] Alt text: Build Agent chat panel for Planner Tracker summary and checkpoints list with highlighted checkpoints button

6.  Select the checkpoint you want to revert back to, and select **Restore**.


## Result

Build Agent reverts your changes both in your application and in the chat.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

