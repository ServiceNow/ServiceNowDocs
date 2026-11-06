---
title: Agentic workflow in Now Assist for Core Business Suite
description: Agentic workflows in Now Assist for Core Business Suite support the Core Business Suite setup process through a conversational interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/using-ai-agent-workflows-na-cbs.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Core Business Suite \(CBS\), Configure Core Business Suite using Otto, Configure, Core Business Suite]
---

# Agentic workflow in Now Assist for Core Business Suite

Agentic workflows in Now Assist for Core Business Suite support the Core Business Suite setup process through a conversational interface.

<table id="table_gyx_brq_l2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

AI agentic workflow for the CBS setup

</td><td>

Supports Core Business Suite configuration through a guided, conversational setup flow. The workflow walks administrators through setup steps, tracks configuration progress, and identifies the next configuration actions. If a setup step does not complete successfully, the workflow provides contextual guidance to address the issue and continue the setup process.

</td><td>

-   CBS configuration agent
-   IA orchestration agent
-   Manage groups and roles agent
-   Notification agent
-   CBS bulk upload agent

</td></tr></tbody>
</table>## AI agents used in the AI Agentic Workflow for the CBS Setup

The following AI agents are used to support the conversational setup process for Core Business Suite.

|AI agent Name|Description|
|-------------|-----------|
|CBS configuration agent|Invokes CBS‑specific scripts and tools to complete CBS tasks through a conversational setup flow.|
|IA orchestration agent|Coordinates CBS and business unit setup steps by sequencing installation and configuration actions based on user input and the current system state.|
|Manage groups and roles agent|Creates and assigns groups and roles across CBS business units to support setup requirements without manual navigation.|
|Notification agent|Configures notification settings for CBS business units to support request, approval, and workflow notifications.|
|CBS bulk upload agent|Processes bulk data uploads for Workplace Services and Source‑to‑Pay business units by importing records and configuration data.|

For more information on the AI agents, see [AI Agent Studio \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-ai-agents.md).

**Parent Topic:**[ServiceNow Otto for Core Business Suite \(CBS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/now-assist-cbs.md)

