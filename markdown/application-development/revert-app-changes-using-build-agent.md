---
title: Revert app changes with Build Agent
description: Restore your development to a previous state when you need to undo recent changes. Use checkpoints created during Build Agent conversations to revert both code and chat history.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Revert app changes with Build Agent

Restore your development to a previous state when you need to undo recent changes. Use checkpoints created during Build Agent conversations to revert both code and chat history.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

2.  Open Build Agent.

    **Note:** The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the corner of your browser.

3.  Open a previous chat to revert your changes by selecting the chats icon ![](../../servicenow-studio/image/sn-studio-ba-chats-icon.png).

    ![Build Agent panel with chat selection icon](../image/ba-chats-selection.png "Chat selection")

4.  Select the chat that contains checkpoints you can revert to.

5.  View all available checkpoints by selecting the checkpoints icon ![](../../servicenow-studio/image/sn-studio-ba-checkpoint-icon.png)

    ![Build Agent chat panel for Planner Tracker summary and checkpoints list with highlighted checkpoints button](../image/ba-chats-checkpoint.png "Checkpoints in chat panel")

6.  Select the checkpoint you want to revert back to, and select **Restore**.


## Result

Build Agent reverts your changes both in your application and in the chat.

**Parent Topic:**[Use Build Agent](use-build-agent.md)

