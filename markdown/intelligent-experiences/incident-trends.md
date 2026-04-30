---
title: Platform Analyze incident trends agentic workflow
description: Use the Platform Analyze incident trends AI agents agentic workflow to detect recurring incident patterns so that you can flag and resolve them before they escalate.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 3
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Platform Analyze incident trends agentic workflow

Use the Platform Analyze incident trends AI agents agentic workflow to detect recurring incident patterns so that you can flag and resolve them before they escalate.

## Analyze incident trends overview

The Analyze incident trends agentic workflow can help enhance incident management by detecting recurring patterns, predicting disruptions, and enabling a proactive resolution to reduce downtime and improve reliability. Incidents are grouped and indexed by the LLM so that the LLM can analyze common recurring issues and root patterns. The LLM then generates resolution recommendations based on the analysis and displays it to you. You can provide feedback for the LLM to guide additional analysis, and the conversation ends after you confirm satisfaction with the results.

The agents, tools, and triggers that are associated with the Analyze incident trends agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

**Note:** At this time, the Analyze incident trends agentic workflow does not allow filtering or conditions for the incidents analyzed, such as only incidents within a certain date range.

## Prerequisites and set up

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you should have at least 500 incidents on your Incident table.

You must also configure Group Action Framework \(GAF\). See [Group Action Framework](group-action-framework.md) for more information on what GAF is and how to set it up.

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter `analyze incident trends` in the Now Assist panel to run the agentic workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

## Troubleshooting

When running this agentic workflow, it is possible to see an error that states "I couldn't analyze as I didn't have the required resources." This error occurs when GAF is not configured for the table you want to analyze. See [Configure Group Action Framework](../task/configure-gaf.md) for steps to configure GAF for the Incident table. If you are still having issues after GAF is configured, reach out to Now Support.

## Troubleshooting

When running this agentic workflow, it is possible to see an error that states "I couldn't analyze as I didn't have the required resources." This error occurs when GAF is not configured for the table you want to analyze. See [Configure Group Action Framework](../task/configure-gaf.md) for steps to configure GAF for the Incident table. If you are still having issues after GAF is configured, reach out to Now Support.

## AI agents used in the Analyze incident trends agentic workflow

|AI agent name|AI agent description|
|-------------|--------------------|
|Incident trends analyzer|Analyzes the incident data to identify the recurring issues and root causes so that it can provide recommendations.|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

**Parent Topic:**[Platform agentic workflows](platform-use-cases.md)

