---
title: Make auto mode available to Arc users
description: Turn on auto mode for the users a policy covers and choose which tools can use it, so users can let an AI model reviewer approve lower risk actions instead of answering every prompt.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/make-auto-mode-available.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [auto mode, auto approval, capability overrides, tool gates]
breadcrumb: [Configure, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Make auto mode available to Arc users

Turn on auto mode for the users a policy covers and choose which tools can use it, so users can let an AI model reviewer approve lower risk actions instead of answering every prompt.

## Before you begin

Role required: sn\_app\_arc.admin

## About this task

Auto mode needs two things: the auto approval capability turned on, and at least one tool gate set to auto approval. The capability is off by default. Until both are in place, users see **Auto** unavailable in the chat, and a tool gate set to auto approval behaves like a tool gate that requires approval.

In auto mode, deny gates, hard gates, connector scopes set to ask first, and sandbox rules still apply.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Arc** &gt; **Policies** &gt; **Arc Agent Policy**.

2.  Open the policy assigned to the users who need auto mode.

3.  Turn on the auto approval capability.

    1.  Select the **Capability Overrides** tab, and then select **New**.

    2.  In the **Capability** field, select `feature:auto_approval`.

    3.  In the **Override Value** field, enter `true`.

    4.  Confirm that **Active** is selected, and then select **Submit**.

4.  For each tool that can use auto mode, set its tool gate to **Auto Approval**.

    Use auto approval for frequently used tools where repeated prompts slow users down. Keep tools that make sensitive changes under hard gates.

5.  Select **Update**.


## Result

Users covered by the policy can select **Auto** for a chat, and a notice above the chat tells them **Your organization turned on auto mode**. If you later turn off the capability or remove every auto approval tool gate, users' saved choices return to **Standard**.

## What to do next

Usage Insights records when users switch modes, which tool calls auto mode approves, and which it sends to the user for approval.

**Parent Topic:**[Configuring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-configuring.md)

