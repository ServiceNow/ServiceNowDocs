---
title: ServiceNow Arc architecture
description: ServiceNow Arc separates the client, the agent host, and an isolated sandbox so that planning happens on the host and agent commands run inside a container with its own network policy. Arc runs on the desktop and connects to your ServiceNow instance, which governs what Arc can do.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/cowork-architecture-arc.html
release: australia
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 2
keywords: [architecture, sandbox]
breadcrumb: [Explore, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# ServiceNow Arc architecture

ServiceNow Arc separates the client, the agent host, and an isolated sandbox so that planning happens on the host and agent commands run inside a container with its own network policy. Arc runs on the desktop and connects to your ServiceNow instance, which governs what Arc can do.

The architecture has three layers: the ServiceNow instance, which governs Arc through the policies you define; the Arc desktop application, which runs tasks; and the connected systems that Arc works with.

\[Omitted image "arc-architecture.png"\] Alt text: Arc high level architecture diagram

## ServiceNow instance

The ServiceNow instance governs Arc, logs its activity, and provides access to your data.

AI Control Tower manages policy and auditing, for Arc when needed. It syncs policies to Arc and registers each Arc installation. Each installation sends AI Control Tower a periodic heartbeat, so AI Control Tower can show which installations are active and healthy. Administrators can use the kill switch in AI Control Tower to stop Arc from taking further actions. For more information, see [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md).

Generative AI Controller \(GAIC\) logs every LLM \(large language model\) call that Arc makes. User initiated requests consume assists and are recorded in the Generative AI Log under the feature name ServiceNow Arc Execution. Requests that Arc makes on its own, such as evaluating actions in Auto mode, don't consume assists. For more information, see [Exploring Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-generative-ai-controller.md).

Data and System of Action provides access to records, automation, and agents. Arc reaches these resources through Action Fabric, the interface that connects Arc to ServiceNow data and actions. For more information, see [MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mcp-platform-manager-landing.md).

## ServiceNow Arc desktop application

ServiceNow Arc runs on the user's desktop and has two main parts: the Arc runtime and the secure sandbox.

The Arc runtime includes the agent loop, sub-agents, skills, and memory. The agent loop plans a task, runs each step, checks the result, and adjusts when a step fails. Skills and connectors extend what Arc can do, and memory stores preferences, decisions, and context across sessions.

The secure sandbox is an isolated environment on the device where tool execution, connectors, and the LLM client run under policy control. The LLM client sends requests to the large language model. Connectors run only when AI Control Tower policy allows them, so every action stays within the limits your administrator sets.

## Connected systems

Users provide a task to Arc through chat. Arc uses its connectors to gather context and take action in connected systems, including Slack, Microsoft 365, GitHub, Model Context Protocol \(MCP\) endpoints, and the ServiceNow instance. The same policy managed connectors handle both incoming work and outgoing actions.

Arc runs tasks on the user's desktop. The Arc runtime, memory, and tool execution stay on the device. Some data leaves the device:

-   Requests from the LLM client to the large language model, which GAIC logs
-   Policy sync and registration with AI Control Tower
-   Data that connectors send to connected systems

**Parent Topic:**[Exploring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-exploring.md)

