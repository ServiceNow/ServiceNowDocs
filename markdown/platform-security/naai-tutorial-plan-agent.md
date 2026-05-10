---
title: Plan your agent
description: Define your use case, decide between an base system and custom agent, choose an activation model, and set your success criteria before you begin building.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 3
breadcrumb: [Create and secure an AI agent in Now Assist, Agentic AI security and governance]
---

# Plan your agent

Define your use case, decide between an base system and custom agent, choose an activation model, and set your success criteria before you begin building.

Time spent planning before you build saves significant rework later. The decisions you make in this phase — what the agent does, how it gets activated, and how you will measure success — shape every configuration choice that follows.

## Define your use case

A well-scoped use case has three characteristics: it involves a repeatable, well-defined task; the agent has access to the data and tools it needs to complete that task; and the outcome is measurable. Good starting candidates are high-volume, low-risk tasks such as incident triage, knowledge article lookup, or password reset routing.

For each candidate use case, answer the following questions before proceeding:

-   What specific task will the agent perform?
-   What data does the agent need access to, and does your organization's security policy allow an agent to access it?
-   What tools \(scripts, flows, knowledge sources\) will the agent use?
-   What does a successful outcome look like, and how will you measure it?
-   What should the agent do if it cannot complete the task?

## Select a base system or custom agent

ServiceNow provides a library of AI agents preconfigured for common use cases. Consider using base system agents when one fits your use case. These preconfigured agents can be faster to deploy, have been tested, and still support custom configuration. Build a custom agent only when no base system agent addresses your use case.

OOTB agents are available in read-only mode. To modify an OOTB agent, you must first duplicate it. See [General guidelines for creating AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gg-creating-aia.md) for guidelines on creating and adapting agents effectively.

## Choose an activation model

ServiceNow supports two ways to activate an AI agent:

-   **Natural language discovery \(user-initiated\)**

    The agent is activated when a user types a message in a conversational channel such as Virtual Agent, Microsoft Teams, or Slack. The platform matches the user's request to the most appropriate agent based on the agent's role and description fields. Supports single AI agents only — agentic workflows cannot be discovered through natural language in Virtual Agent.

-   **Trigger-based activation \(event-initiated\)**

    The agent or agentic workflow is activated automatically when a platform event occurs, such as a record being created or updated, a scheduled time being reached, or an inbound email arriving. No user interaction is required. Supports both single AI agents and agentic workflows.


If your use case requires a user to initiate the interaction through chat, choose natural language discovery. If your use case should run automatically based on platform events, choose trigger-based activation.

## Define success criteria

Define how you will measure whether the agent is working before you build it. This helps prevent moving goalposts during testing and gives you a clear go-live threshold. At minimum, define the following:

-   The primary success metric \(for example, deflection rate, task closure rate, or mean time to resolve\).
-   The minimum acceptable threshold for that metric before go-live.
-   How you will measure it \(for example, via the AI Agent Analytics dashboard or a custom Performance Analytics indicator\).

## Next step

When your use case is defined, your agent type and activation model are chosen, and your success criteria are documented, proceed to [Build your agent](naai-tutorial-build-agent.md).

**Parent Topic:**[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)

