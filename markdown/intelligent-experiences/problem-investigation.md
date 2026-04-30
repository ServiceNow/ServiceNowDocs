---
title: Platform Investigate IT problems agentic workflow
description: Use the Platform Investigate IT problem AI agents agentic workflow to perform root cause and risk assessments so that you can create an actionable resolution plan for a problem.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 2
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Platform Investigate IT problems agentic workflow

Use the Platform Investigate IT problem AI agents agentic workflow to perform root cause and risk assessments so that you can create an actionable resolution plan for a problem.

## Investigate IT problems overview

The Investigate IT problems agentic workflow can help to assist agents and subject matter experts \(SMEs\) in investigating problems in their IT landscape. A problem can be associated with many incidents, and any investigator must be aware of a large number of details when looking at a problem. The agentic workflow can help provide insights from the incident and problem details and suggest plans or possible solutions.

The agents, tools, and triggers that are associated with the investigate IT problems agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and set up

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

Because this agentic workflow analyzes problems and incidents related to those problems, you must have records on the Problem and Incident table.

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter `investigate the problem PRB001` or similar phrases in the Now Assist panel to trigger the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

## Troubleshooting

If a Problem has a large number of related incidents, you may run into an error that states "This model's maximum context length is 128000 tokens. However, your messages resulted in \[X\] tokens. Please reduce the length of the messages." This maximum token count is in place for all Now Assist skills, so there is currently no way to work around this error. You can try the agentic workflow again using a different Problem.

## AI agents used in the Investigate IT problems agentic workflow

|AI agent name|AI agent description|
|-------------|--------------------|
|Problem investigator|Identifies the root causes, performs an impact assessment, and plans resolutions.|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

**Parent Topic:**[Platform agentic workflows](platform-use-cases.md)

