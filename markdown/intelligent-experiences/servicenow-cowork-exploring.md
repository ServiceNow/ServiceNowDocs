---
title: Exploring ServiceNow Cowork
description: ServiceNow Cowork is an autonomous AI agent that performs complex tasks, executes multi-step workflows, interacts with enterprise applications, and takes actions based on defined policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/servicenow-cowork-exploring.html
release: zurich
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [explore, ServiceNow Cowork, Cowork, autonomous AI agent, Overview]
breadcrumb: [ServiceNow Cowork, Enable AI experiences]
---

# Exploring ServiceNow Cowork

ServiceNow Cowork is an autonomous AI agent that performs complex tasks, executes multi-step workflows, interacts with enterprise applications, and takes actions based on defined policies.

## ServiceNow Cowork overview

ServiceNow Cowork completes tasks by identifying the required actions, running those actions, and adjusting its approach when conditions change or an action fails. Cowork executes within the security, access, and governance policies of your enterprise environment. Administrators define policies that control which actions Cowork can take autonomously. Users can delegate complex tasks that require several steps.

Cowork combines natural language interaction with direct access to ServiceNow APIs, Microsoft 365, file systems, GitHub and a sandboxed execution environment. With these capabilities together, it completes workflows end to end without needing constant human direction. Rather than running through a fixed sequence of predefined steps, Cowork analyzes each task, selects an approach, and executes the actions needed to complete it. Cowork works across your connected systems and delivers a completed result rather than a progress update.

With Cowork, enterprise professionals can delegate work across their systems, and administrators can deploy and govern it.

**Note:** Cowork operates as a native desktop application on macOS. The agent runs locally and stores all data on your device. No data leaves the device unless you explicitly connect an integration that sends it externally.

## ServiceNow Cowork users

<table id="servicenow-cowork-exploring-users"><thead><tr><th>

User

</th><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow Cowork admin

</td><td>

sn\_app\_cowork.admin

</td><td>

Sets policies and approval gates, governs connectors and MCP servers, and controls which models are available.

</td></tr><tr><td>

ServiceNow Cowork user

</td><td>

sn\_app\_cowork.user

</td><td>

Uses the Cowork to perform tasks, interact with AI agents, use connectors, answers approval prompts, runs skills, workflows, and subagents.

</td></tr></tbody>
</table>## ServiceNow Cowork key features and benefits

-   -   **Autonomous task execution**

    Cowork takes an objective and determines the steps needed to complete it. It plans, executes actions, checks results, retries and adjusts the approach when something fails. Policies determine where approvals are required.

-   -   **Enterprise governance and controls**

    Organizations can monitor what agents accessed and what actions were performed. Administrators control agent permissions and activity through policies and AI Control Tower.

-   -   **Skills and workflows**

    Skill packs extend what the agent can do and repair their own scripts when they fail. Workflows are reusable step sequences.

-   -   **Works across applications**

    Cowork is not limited to the ServiceNow applications. It can interact with files, terminals, APIs, and enterprise systems to complete a task or a set of tasks.

-   -   **Governed connections**

    Administrators control which external services Cowork can connect to through Model Context Protocol \(MCP\) servers. Connections can be disabled or isolated as needed.

-   -   **Extensibility**

    Cowork connects to skills, sub-agents, MCP servers, and external services through a built-in settings library.

-   -   **Tiered approvals**

    Approval rules are configured as hard gates or soft gates. Hard gates block actions until approval is granted. Soft gates allow actions to execute without requiring approval first, but approval remains available if needed. An auto mode capability automatically routes lower-risk calls past the approval prompt.

-   -   **Usage insights and skill telemetry**

    Usage insights report adoption rates, intervention frequency, policy events, and cost signals. Skill telemetry tracks performance metrics and compliance across deployed skills.

-   -   **Semantic memory and knowledge graph**

    Cowork keeps two memory layers. Long-term memory stores preferences, decisions, and facts that persist across sessions. The knowledge graph, which automatically builds a structured map of people, projects, decisions, and action items from conversations and activity, is also maintained.

-   -   **Automatic insight capture**

    Cowork captures activity and meetings, extracts decisions and action items, and delivers a structured summary with follow-up tasks.

-   -   **Usage insights and skill observability**

    Administrators can view Cowork usage telemetry through usage insights for sessions, conversation counts, connector activity, and policy events. Skill observability tracks invocation counts, success rates, latency, and token consumption per skill, with detailed traces available in AI Control Tower.


## What to explore next

To learn more about configuring and using ServiceNow Cowork, see:

-   [Configuring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-configuring.md)
-   [Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-using.md)
-   [ServiceNow Cowork reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-reference.md)

-   **[ServiceNow Cowork architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/cowork-architecture.md)**  
ServiceNow Cowork separates the client, the agent host, and an isolated sandbox so that planning happens on the host and agent commands run inside a container with its own network policy. Cowork runs on the desktop and connects to your ServiceNow instance, which governs what Cowork can do.
-   **[Policy management and governance in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/policy-management-cowork.md)**  
Policies are governance rules on your ServiceNow instance that control what ServiceNow Cowork can do, which actions need approval, and which actions are blocked.

**Parent Topic:**[ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-landing.md)

