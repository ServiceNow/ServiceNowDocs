---
title: Use case: Using UI Builder Agent
description: Learn UI Builder features and accelerate page configuration using conversational AI.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Use case, Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Use case: Using UI Builder Agent

Learn UI Builder features and accelerate page configuration using conversational AI.

## Scenario

A citizen developer at a retail company is creating an employee self-service portal using UI Builder. They are relatively new to the platform and are working on a page that requires a three-column layout, along with a button that links to an external HR system. Additionally, they would like to verify whether any client scripts are running on the page before making any layout changes.

## Problem

The developer is not yet familiar with UI Builder ’s configuration options. Looking up documentation for each task interrupts their workflow and slows progress. They are unsure how to apply a multi-column layout, add a button with an external link, or check whether existing scripts might be affected by their layout changes.

## Solution

The UI Builder agent is available directly within the UI Builder page editor as a chat-based assistant. The developer can ask questions about features, request page modifications, and get configuration insights — all without leaving the editor. The agent provides instant answers backed by the latest ServiceNow documentation and can directly apply changes to the page on the developer’s behalf.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](../task/install-ui-generation.md) and [Grant UI Builder admin role](../task/grant-ui-builder-admin-role.md).

## Configuration steps

Perform the following steps to use UI Builder agent:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Open the employee self-service portal experience.
3.  Open the page to edit and open the Now Assist panel from the page editor.
4.  In the chat panel, do the following:
    -   Ask the UI Builder agent if there are any client scripts on the page: `Are any client scripts used on my page?`

        The agent provides a detailed breakdown of the page’s current scripts and configurations.

    -   Ask the UI Builder agent how you can apply a three-column layout: `How can I apply a three-column layout to this page?`

        The agent explains the available layout options and relevant steps.

    -   Ask the UI Builder agent to add a three-column layout to the page: `Apply a three-column layout to this page.`

        The agent implements the layout change.

    -   Ask the UI Builder agent to add a button with label and navigation: `Add a button with the label 'Visit HR Portal' that links to https://hr.example.com in a new window`.

        The agent adds and configures the button component.

5.  Review the changes in the page editor and make any necessary adjustments to the styling.

## Outcome

The developer sets up a three-column layout and adds a linked button component in a single session, with guidance from the UI Builder agent. They also gain confidence in their page's script configuration before making any changes. Tasks that would have typically required multiple searches through documentation are now completed without leaving the editor.

**Parent Topic:**[UI Generation use cases](../task/ui-generation-use-cases.md)

**Related topics**  


[UI Builder Agent](uib-builder-agent-concept.md)

[Using UI Builder agent](using-ui-builder-agent.md#)

