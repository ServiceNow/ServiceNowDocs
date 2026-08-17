---
title: System properties for AI Control Tower
description: Several system properties that affect core AI Control Tower are available.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-reference-system-properties.html
release: zurich
topic_type: reference
last_updated: "2026-06-10"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# System properties for AI Control Tower

Several system properties that affect core AI Control Tower are available.

These properties exist in the System Properties \[sys\_properties\] table. The admin role is necessary to set system properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.oauth.tool.scan.skill.enabled

</td><td>

Controls whether MCP server tool scanning is performed by a ServiceNow skill customized for AI Control Tower AI asset security. This scan is a more thorough scan that can detect more potential threats than the AI Guardian scan. As a general guideline, use this scan instead of the AI Guardian scan.-   Type: Boolean
-   Default value: `true`
-   Location: The System Properties \[sys\_properties\] table

</td></tr><tr><td>

glide.oauth.tool.scan.guardian.enabled

</td><td>

Controls whether MCP server tool scanning is performed by AI Guardian. For more information, see .-   Type: Boolean
-   Default value: false
-   Location: The System Properties \[sys\_properties\] table

</td></tr><tr><td>

sn\_ai\_security.analyzer\_max\_record\_age\_hours

</td><td>

See [System properties for AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference-system-properties.md).

</td></tr><tr><td>

sn\_ai\_governance.asset\_dedup.agent.enabled

</td><td>

The main switch for intelligent agentic AI asset deduplication. When fails, all deduplication scheduled jobs and AI agent-driven semantic tag generation are inactive.

</td></tr><tr><td>

sn\_ai\_security.veza.api.key

</td><td>

See [System properties for AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference-system-properties.md)

</td></tr><tr><td>

sn\_ai\_security.veza.api.url

</td><td>

See [System properties for AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference-system-properties.md).

</td></tr></tbody>
</table>