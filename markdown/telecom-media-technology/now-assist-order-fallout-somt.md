---
title: Now Assist for Sales CRM for Telecommunications AI agent Order fallout AI agent
description: Use the AI agent to automatically create the fallout records based on reported issues on the task's notes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI agents in SOMT, Use agentic workflows, Now Assist for Sales CRM for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Sales CRM for Telecommunications AI agent Order fallout AI agent

Use the AI agent to automatically create the fallout records based on reported issues on the task's notes.

## Order fallout AI agent overview

Use the Order fallout AI agent to:

-   Eliminate manual review of completed orders by automatically analyzing work notes.
-   Reduce manual effort in the fallout creation and assignment process.
-   Ensure that all relevant fallouts are captured and linked to original order tasks.

The agent automatically creates a fallout in case of an order task failure. The agent identifies the correct category in which the fallout must be created. The agent doesn’t create a fallout if the fallout is already created.

This agent analyzes the order fulfillment tasks when a task status is changed to on hold and automatically creates relevant fallout records based on issues identified in work notes. It leverages Now LLM Service to match task observations with predefined fallout types, streamlining the post-fulfillment issue tracking process.

Order fallout AI agent performs the following task:

1.  Analyzes all the order task work notes.
2.  Identifies reported issues.
3.  Matches issues with available fallout types.
4.  Creates appropriate fallout records.

To modify the Order fallout AI agent, [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

To add tools and information, see [Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-tool-aia.md) for details.

**Important:** In the Select channels and status page, make sure that the **Active** button is turned on to activate the AI agent.

Role required: sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

## Order fallout AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.
2.  Select **Order fallout AI agent**.

## Testing the AI agent

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test use cases**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

