---
title: Platform Suggest survey responses agentic workflow
description: Use the Platform Suggest survey responses AI agents agentic workflow to assist requesters in filling out surveys for their requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/enable-ai-experiences/survey-suggest.html
release: xanadu
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 2
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Platform Suggest survey responses agentic workflow

Use the Platform Suggest survey responses AI agents agentic workflow to assist requesters in filling out surveys for their requests.

## Suggest survey responses overview

The Suggest survey responses agentic workflow can help simplify and increase survey responses. Many requesters end up not filling out surveys after requests have been fulfilled, and this agentic workflow helps them to make informed decisions to answer survey questions quickly.

The agentic workflow is activated when an incident closes. When a user is assigned a survey after an incident is closed, they will receive an email with AI-suggested answers to their survey. They then have the option to accept the AI-generated answers for the survey with a link at the bottom of the email. They can also choose to fill out the survey manually.

The agents, tools, and triggers that are associated with the suggest survey responses agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and set up

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

You must have an email configuration for sending surveys to users. For more information, see Survey trigger conditions.

## AI agents used in the Suggest survey responses agentic workflow

|AI agent name|AI agent description|
|-------------|--------------------|
|Survey filling answer suggester|Suggests answers to questions based on record details.|
|Survey filling data collector|Collects the data related to the record and the survey questions to collect feedback.|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/platform-use-cases.md).

**Parent Topic:**[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/platform-use-cases.md)

