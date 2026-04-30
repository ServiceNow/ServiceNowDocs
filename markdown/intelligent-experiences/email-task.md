---
title: Platform Process emails for tasks agentic workflow
description: Use the Platform Process emails for tasks AI agents agentic workflow to process incoming emails and convert them to actionable tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 2
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Platform Process emails for tasks agentic workflow

Use the Platform Process emails for tasks AI agents agentic workflow to process incoming emails and convert them to actionable tasks.

## Process emails for tasks overview

The process emails for tasks agentic workflow can help decrease manual data entry, accelerate response times, and improve task organization by automatically converting incoming emails into tasks. The agentic workflow extracts details from the email to populate fields, categorizes and prioritizes the task, and assigns the task to the associated group. The workflow can also write and send new emails.

Once the agentic workflow is activated and configured, users can send emails and have task records created based on the content of the emails. These can be new records or updates to existing ones.

The agents, tools, and triggers that are associated with the process emails for tasks agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and set up

To set up this workflow, reach out to Now Support.

**Note:** You must deactivate other capabilities which create incidents or tasks from emails if you want to use this agentic workflow.

## AI agents used in the Process emails for tasks agentic workflow

|AI agent name|AI agent description|
|-------------|--------------------|
|Record management AI agent|Fetches, creates, and updates record actions with the provided record details.|
|Email action and information AI agent|Extracts action items and details from emails, predicts information for child task records, and copies email attachments to records. This agent also has tools to compose emails and send them to recipients.|
|Email to new Task Creation|Creates tasks from emails.|
|Email on Existing Parent Lead|Handles emails which have parent records and create or update tasks from them.|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

**Parent Topic:**[Platform agentic workflows](platform-use-cases.md)

