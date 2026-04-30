---
title: Platform Classify tasks agentic workflow
description: Use the Platform Classify tasks AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 2
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Platform Classify tasks agentic workflow

Use the Platform Classify tasks AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.

## Classify tasks overview

The Classify tasks agentic workflow can help improve efficiency and accuracy by automatically gathering information, prioritizing tasks, assigning teams, detecting sentiment, and generating task summaries.

The agents, tools, and triggers that are associated with the Classify tasks agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and set up

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you must also configure Group Action Framework \(GAF\). See [Set up AI Search for Group Action Framework](../task/setup-ai-search-gaf.md) and [Configure Group Action Framework](../task/configure-gaf.md) for more information on getting started with GAF.

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter these or similar phrases in the Now Assist panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

-   Populate the priority and assignment group for INC0001
-   Populate the empty fields on INC0001
-   Find the priority for INC001

## AI agents used in the Classify tasks agentic workflow

|AI agent name|AI agent description|
|-------------|--------------------|
|Record management AI agent|Fetches, creates, and updates records with the provided details.|
|Record field value prediction AI agent|Predicts the fields of a record after being given a sys\_id.|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

**Parent Topic:**[Platform agentic workflows](platform-use-cases.md)

