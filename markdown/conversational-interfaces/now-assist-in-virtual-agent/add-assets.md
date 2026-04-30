---
title: Add assets to a chat assistant
description: Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 2
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Add assets to a chat assistant

Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users.

## Before you begin

See [Add a Knowledge Graph schema to a chat assistant](add-kg-schema-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users.

When viewing or editing an existing assistant, you can view or edit the assets that are associated with an assistant. Assets can also be added to an assistant from the Asset Library and/or Topic Migration.

**Note:** If you're an existing customer who previously turned on or off a skill type for an existing assistant, you can add or remove any individual asset when editing an assistant.

## Procedure

1.  Select **Add assets**.

    By default, no assets are mapped to the assistant.

    ![Add assets to an assistant.](../image/NAinVA-assets-122025.png "Add assets")

    The **Add assets from library** modal appears where you can multi-select assets that you want to assign to the assistant. Asset types include:

    -   Topics define what the assistant can talk about and bring structure to back-and-forth conversation.
    -   Subflows are reusable building blocks of logic that your assistant calls on to complete multi-step processes.
    -   Actions are single, simple steps that help your assistant complete tasks.
    -   Custom skills skills are AI-powered capabilities you build to extend what your assistant can do.
    -   AI agents independently reason, plan, and take action to complete tasks, based on your instruction.
    **Note:** There are variations for Now Assist panel assistants.

    For Now Assist panel - Platform assistant, the available asset types are topics, subflows, actions, custom skills, and agentic workflows. Agentic workflows are a group of AI agents that work together to independently solve problems.

    **Note:** If you want to use AI agents for your Now Assist panel - Platform assistant, contact Support.

    For Now Assist panel - Developer assistant, only topics are available.

    ![Select assets from library.](../image/NAinVA-select-assets-122025.png "Select assets from library")

2.  Select **Save**.

    The list view appears where you can manage assets that are associated with an assistant. The table is not editable from this view. To further edit the assets, navigate to the assistant edit flow.

    ![View list of added assets and manage assets.](../image/NAinVA-manage-assets-122025.png "Asset list")

    To unmap an asset, select **Manage assets** and uncheck the desired asset.

3.  Select **Save and continue**.


## What to do next

See [Display your chat assistant on a portal, channel, or mobile app](display-assistant-portal-channel.md).

See [Display your assistant on Platform or ServiceNow Studio](display-nap-assistant.md).

