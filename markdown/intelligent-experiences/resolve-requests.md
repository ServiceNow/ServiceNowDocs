---
title: Platform Generate resolution plans agentic workflow
description: Use the Platform Generate resolution plans AI agents agentic workflow to fetch task record details, generate resolution summary steps, and update comments or work notes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 2
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Platform Generate resolution plans agentic workflow

Use the Platform Generate resolution plans AI agents agentic workflow to fetch task record details, generate resolution summary steps, and update comments or work notes.

## Generate resolution plans overview

The Generate resolution plans agentic workflow can help resolve tasks by collecting record details and generating resolution summaries that can be added to comments or work notes. Due to the dynamic nature of AI agents, this agentic workflow can be used for tasks that require complex logic even when provided with minimal details.

The agents, tools, and triggers that are associated with the Generate resolution plans agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and set up

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you must also configure Group Action Framework \(GAF\). See [Set up AI Search for Group Action Framework](../task/setup-ai-search-gaf.md) and [Configure Group Action Framework](../task/configure-gaf.md) for more information on getting started with GAF.

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter these or similar phrases in the Now Assist panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

-   Generate resolution plan for INC0001
-   Create detailed resolution steps for INC0001
-   Resolve INC0001

## AI agents used in the Generate resolution plans agentic workflow

|AI agent name|AI agent description|
|-------------|--------------------|
|Next best action recommendation AI agent|Identifies the steps for resolving tasks by referencing the similar task details and reviewing knowledge articles.|
|Record management AI agent|Fetches, creates, and updates record actions with the provided record details.|
|Web research and recommendation AI agent|Analyzes problems and generates resolution steps using web search tools.|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

**Parent Topic:**[Platform agentic workflows](platform-use-cases.md)

