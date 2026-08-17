---
title: Enable store inquiry AI agent trigger
description: The HQ agent can leverage the store inquiry AI agent either manually or by enabling or configuring the trigger.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-enable-store-inquiry-ai-agent.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Enable store inquiry AI agent trigger

The HQ agent can leverage the store inquiry AI agent either manually or by enabling or configuring the trigger.

## About this task

ServiceNow Otto for Retail Service Management and the AI Agents for Retail Service Management together enable the store inquiry AI agent. The HQ agent can leverage the store inquiry AI agent either manually or by enabling or configuring the trigger.

-   A trigger allows the AI agent to launch automatically without requiring a HQ agent request when the trigger condition is met.
-   The trigger shipped with this release launches for the HQ agent when the case state changes from New to Open and the Assigned to field is not empty.
-   By default, the trigger being shipped is disabled and HQ agent can navigate to the AI agent and enable the trigger.

## Before you begin

Role required: sn\_rtl\_stre\_servcs.agent

You must have the Retail Core, Retail Mobile application, and Retail Store Inquiry.

## Procedure

1.  Install the ServiceNow Otto for Retail Service Management plugin and AI Agents for Retail Service Management from the application manager.

2.  Navigate to **Manage agentic workflows and AI agents** &gt; **Store inquiry AI agent** on the AI Agent Studio.

3.  Select the **Trigger** &gt; **Add a new trigger** or select the existing trigger and toggle the **Trigger if ON** option to enable the trigger and save it to launch the AI agent automatically.


## What to do next

**Configure AI agent security**

You can enable security implementation on AI agents and agentic workflows through access control lists \(ACLs\) and user identities. These ACLs determine which users have permissions to discover and invoke an agentic workflow or AI agent.

Configure and manage these ACLs for agentic workflows and AI agents in the AI Agent Studio.

See [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md) for more information on implementing security for AI agents.

