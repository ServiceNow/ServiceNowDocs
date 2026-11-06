---
title: Exploring ServiceNow Arc
description: ServiceNow Arc is an autonomous AI agent that performs complex tasks, executes multi-step workflows, interacts with enterprise applications, and takes actions based on defined policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/servicenow-cowork-exploring.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [explore, ServiceNow Arc, Arc, autonomous AI agent, Overview]
breadcrumb: [ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Exploring ServiceNow Arc

ServiceNow Arc is an autonomous AI agent that performs complex tasks, executes multi-step workflows, interacts with enterprise applications, and takes actions based on defined policies.

## ServiceNow Arc overview

ServiceNow Arc completes tasks by identifying the required actions, running those actions, and adjusting its approach when conditions change or an action fails. Arc executes within the security, access, and governance policies of your enterprise environment. Administrators define policies that control which actions Arc can take autonomously. Users can delegate complex tasks that require several steps.

Arc combines natural language interaction with direct access to ServiceNow APIs, Microsoft 365, file systems, GitHub and a sandboxed execution environment. With these capabilities together, it completes workflows end to end without needing constant human direction. Rather than running through a fixed sequence of predefined steps, Arc analyzes each task, selects an approach, and executes the actions needed to complete it. Arc works across your connected systems and delivers a completed result rather than a progress update.

With Arc, enterprise professionals can delegate work across their systems, and administrators can deploy and govern it.

**Note:** Arc operates as a native desktop application on macOS and Windows. The agent runs locally and stores all data on your device. No data leaves the device unless you explicitly connect an integration that sends it externally.

## ServiceNow Arc users

<table id="servicenow-cowork-exploring-users"><thead><tr><th>

User

</th><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow Arc admin

</td><td>

sn\_app\_arc.admin

</td><td>

Sets policies and approval gates, governs connectors and MCP servers, and controls which models are available.

</td></tr><tr><td>

ServiceNow Arc user

</td><td>

sn\_app\_arc.user

</td><td>

Uses the Arc to perform tasks, interact with AI agents, use connectors, answers approval prompts, runs skills, workflows, and subagents.

</td></tr></tbody>
</table>## ServiceNow Arc key features and benefits

-   -   **Autonomous task execution**

    Arc takes an objective and determines the steps needed to complete it. Policies determine where approvals are required.

-   -   **Enterprise governance and controls**

    Organizations can monitor what agents accessed and what actions were performed. Administrators control agent permissions and activity through policies and AI Control Tower.

-   -   **Skills and workflows**

    Skill packs extend what the agent can do and repair their own scripts when they fail. Workflows are reusable step sequences.

-   -   **Works across applications**

    Arc is not limited to the ServiceNow applications. It can interact with files, terminals, APIs, and enterprise systems to complete a task or a set of tasks.

-   -   **Governed connections**

    Administrators control which external services Arc can connect to through Model Context Protocol \(MCP\) servers. Connections can be disabled or isolated as needed.

-   -   **Extensibility**

    Arc connects to skills, sub-agents, MCP servers, and external services through a built-in settings library.

-   -   **Tiered approvals**

    Approval rules are configured as hard gates or soft gates. Hard gates block actions until approval is granted. Soft gates also require approval, but users can select **Always Allow** to save the decision, so later actions of the same type run without a prompt. When an administrator makes auto mode available, users can turn it on for each chat, and an AI model reviewer approves lower risk actions without a prompt.

-   -   **Semantic memory and knowledge graph**

    Arc keeps two memory layers. Long-term memory stores preferences, decisions, and facts that persist across sessions. The knowledge graph, which automatically builds a structured map of people, projects, decisions, and action items from conversations and activity, is also maintained.

-   -   **Automatic insight capture**

    Arc captures activity and meetings, extracts decisions and action items, and delivers a structured summary with follow-up tasks.

-   -   **Usage insights and skill observability**

    Administrators can view Arc usage telemetry through usage insights for sessions, conversation counts, connector activity, and policy events. Skill observability tracks invocation counts, success rates, latency, and token consumption per skill, with detailed traces available in AI Control Tower.


## What to explore next

To learn more about configuring and using ServiceNow Arc, see:

-   [Configuring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-configuring.md)
-   [Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)
-   [ServiceNow Arc reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-reference.md)

-   **[ServiceNow Arc architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)**  
ServiceNow Arc separates the client, the agent host, and an isolated sandbox so that planning happens on the host and agent commands run inside a container with its own network policy. Arc runs on the desktop and connects to your ServiceNow instance, which governs what Arc can do.
-   **[Policy management and governance in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-management-cowork.md)**  
Policies are governance rules on your ServiceNow instance that control what ServiceNow Arc can do, which actions need approval, and which actions are blocked.

**Parent Topic:**[ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-landing.md)

