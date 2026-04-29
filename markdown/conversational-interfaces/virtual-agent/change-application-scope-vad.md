---
title: Change the application scope for Virtual Agent Designer topics
description: Set the application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the ITSM Virtual Agent Conversations scope \(and not the scope for the ITSM NLU \(Natural Language Understanding\) Model for Virtual Agent Conversations\).
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Virtual Agent Designer, Application scope, Unified navigation, Globe icon, Virtual Agent topic]
breadcrumb: [Creating a Virtual Agent topic, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Change the application scope for Virtual Agent Designer topics

Set the application scope before you create or update a topic. For example, if you're creating ITSM topics, verify that you're in the **ITSM Virtual Agent Conversations** scope \(and not the scope for the ITSM NLU \(Natural Language Understanding\) Model for Virtual Agent Conversations\).

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

When you open or create a topic, your current application scope is displayed in a status bar on the topic page. The status bar is visible in all tabs in your topic. If you open a topic not in your current scope, a warning banner appears on the canvas, and you can’t edit the topic. You can still activate or deactivate, publish, or duplicate the topic. If you duplicate the topic, the duplicate sets to your current scope.

If you have multiple topics open at once, every topic shows its individual scope, and all topics not set to the current scope are locked.

![image.app-scope-canvas-views-2]

## Procedure

1.  In the unified navigation bar, select the globe icon \(![](../images/icon-scope.png)\).

2.  Select **Application Scope**, then choose the appropriate scope for your conversations.

    For example, select **Workflow Studio**.

    **Note:** If you're using domain separation, you can change the domain that you're working in. Select **Domain scope: global** to change the domain. Any topics created within a domain are restricted to users of that domain. For more information, see [Domain separation and Virtual Agent](../concept/domain-separation-virtual-agent.md).


## Result

The application scope updates, and the new scope is displayed in the topic page when you refresh or open the topic. When the scope isn’t global, a ring appears around the globe icon \(![](../images/globe-icon-red-ring.png)\).

If the new scope matches a topic that was locked before, the warning banner disappears and you can edit the topic.

## What to do next

Return to creating or updating your topic. If you have multiple topics open, you can sort them by activating the **Group tabs by app scope** toggle switch in **Preferences**. For more information, see [Assistant Designer Asset library](../reference/vad-topics-page.md).

**Parent Topic:**[Creating a Virtual Agent topic](create-virtual-agent-topic.md)

