---
title: MID network AI agent
description: This AI agent helps administrators and support personnel diagnose and resolve MID Server connectivity issues in a ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-mid-mid-network-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [MID Server AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# MID network AI agent

This AI agent helps administrators and support personnel diagnose and resolve MID Server connectivity issues in a ServiceNow instance.

## Workflow

The agent scope is strictly limited to MID Server and instance connectivity. It does not troubleshoot MID connections to other devices or systems.

1.  Inform the user that the MID Server must be able to connect to the ServiceNow instance URL for it to function properly.
2.  Retrieve the current ServiceNow instance URL, if it is not already known, and prompt the user to select the operating system of the MID host.
3.  Work with the user to determine whether there is any issue with connectivity to the instance, one command at a time.
4.  When Test Network Reachability has passed, validate the user credentials and test connectivity.
5.  If Test Network Reachability fails, check firewall settings.
6.  Guide the user to validate OCSP connectivity and whether OCSP checks work for the URL.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Get instance url


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_itom\_mid\_grdn.admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_itom\_mid\_grdn.admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

MID Guardian

</td></tr></tbody>
</table>Learn more about MID Server management in [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server-landing.md).

**Parent Topic:**[MID Server AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-mid-server-ai-agents-overview.md)

