---
title: Enable the in-product experience for agentic workflows
description: Enable the AI Workflows panel and UI actions for agentic workflows on forms in the Core UI and workspaces to track agentic AI executions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-02-04"
reading_time_minutes: 1
keywords: [agentic ai]
breadcrumb: [In-product agentic AI, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Enable the in-product experience for agentic workflows

Enable the AI Workflows panel and UI actions for agentic workflows on forms in the Core UI and workspaces to track agentic AI executions.

## Before you begin

Role required: admin

## About this task

Agentic workflows can perform work on certain records, and you can track their progress or provide input in the AI Workflows panel available for forms and workspaces. See [In-product agentic AI](../concept/in-product-agentic-ai.md) for more details about the functions and features of the AI Workflows panel.

The following task describes the process for enabling the system property that allows you to see the AI Workflows panel and see UI actions for agentic workflows: **com.glide.agentic\_processes\_view.enabled**.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow. See [Select channels and access for agentic workflows](channels-access-aw.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Select **New**.

3.  In the **Name** field, enter `com.glide.agentic_processes_view.enabled`.

4.  In the **Value** field, enter `true`.


## Result

The In-product agentic experience, including the AI Workflows panel, is available.

## What to do next

Monitor agentic workflow execution on forms in the Core UI and workspaces, or create UI actions to grant users access.

