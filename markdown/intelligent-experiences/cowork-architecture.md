---
title: ServiceNow Cowork architecture
description: ServiceNow Cowork separates the client, the agent host, and an isolated sandbox so that planning happens on the host and agent commands run inside a container with its own network policy. Cowork runs on the desktop and connects to your ServiceNow instance, which governs what Cowork can do.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/cowork-architecture.html
release: zurich
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 2
keywords: [architecture, sandbox]
breadcrumb: [Explore Cowork, ServiceNow Cowork, Enable AI experiences]
---

# ServiceNow Cowork architecture

ServiceNow Cowork separates the client, the agent host, and an isolated sandbox so that planning happens on the host and agent commands run inside a container with its own network policy. Cowork runs on the desktop and connects to your ServiceNow instance, which governs what Cowork can do.

The high level architecture has three layers: the ServiceNow instance, Cowork, which governs Cowork based on the policy defined, the Cowork desktop application, which runs tasks; and the connected systems that Cowork works with.

\[Omitted image "servicenow-cowork-architecture.png"\] Alt text: Cowork high level architecture diagram

## ServiceNow instance

The ServiceNow instance governs Cowork, logs its activity, and provides access to your data.

AI Control Tower manages policy and auditing, for Cowork when needed. It syncs policies to Cowork and registers each Cowork installation. Each installation sends AI Control Tower a periodic heartbeat, so AI Control Tower can show which installations are active and healthy. Administrators can use the kill switch in AI Control Tower to stop Cowork from taking further actions. For more information, see [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-landing.md).

Generative AI Controller \(GAIC\) logs every LLM \(large language model\) call that Cowork makes. User initiated requests consume assists and are recorded in the Generative AI Log under the feature name ServiceNow Cowork Execution. Requests that Cowork makes on its own, such as evaluating actions in Auto mode, don't consume assists. For more information, see [Exploring Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/generative-ai-controller/exploring-generative-ai-controller.md).

Data and System of Action provides access to records, automation, and agents. Cowork reaches these resources through Action Fabric, the interface that connects Cowork to ServiceNow data and actions. For more information, see .

## ServiceNow Cowork desktop application

ServiceNow Cowork runs on the user's desktop and has two main parts: the Cowork runtime and the secure sandbox.

The Cowork runtime includes the agent loop, sub-agents, skills, and memory. The agent loop plans a task, runs each step, checks the result, and adjusts when a step fails. Skills and connectors extend what Cowork can do, and memory stores preferences, decisions, and context across sessions.

The secure sandbox is an isolated environment on the device where tool execution, connectors, and the LLM client run under policy control. The LLM client sends requests to the large language model. Connectors run only when AI Control Tower policy allows them, so every action stays within the limits your administrator sets.

## Connected systems

Users provide a task to Cowork through chat. Cowork uses its connectors to gather context and take action in connected systems, including Slack, Microsoft 365, GitHub, Model Context Protocol \(MCP\) endpoints, and the ServiceNow instance. The same policy managed connectors handle both incoming work and outgoing actions.

Cowork runs tasks on the user's desktop. The Cowork runtime, memory, and tool execution stay on the device. Some data leaves the device:

-   Requests from the LLM client to the large language model, which GAIC logs
-   Policy sync and registration with AI Control Tower
-   Data that connectors send to connected systems

**Parent Topic:**[Exploring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-exploring.md)

