---
title: Build your agent
description: Create your agent in AI Agent Studio, configure its tools and knowledge sources, and set the access controls that determine who can invoke it and what data it can access.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 3
breadcrumb: [Create and secure an AI agent in Now Assist, Agentic AI security and governance]
---

# Build your agent

Create your agent in AI Agent Studio, configure its tools and knowledge sources, and set the access controls that determine who can invoke it and what data it can access.

This phase covers the core build work in AI Agent Studio. Security configuration — access controls and role masking — is part of this phase, not a separate step. Configure it while you build the agent, not after.

## Create the agent

Navigate to **All** &gt; **AI Agent Studio** to begin. Every AI agent is composed of four core elements:

-   **Agent identity**

    Defines who the agent is, what domain it operates in, and how it should behave. This is the persistent system-level context that frames every decision the agent makes.

-   **Descriptions**

    Define the categories of requests the agent can handle. Each description has a name, trigger utterances that route conversations to it, and specific instructions. Think of descriptions as the agent's skill domains.

-   **Tools**

    Give the agent the ability to take actions and retrieve data. Tools include script tools \(server-side JavaScript\), sub-flows \(Flow Designer workflows\), and retrievers \(knowledge source searches\).

-   **Instructions \(the prompt\)**

    Defines who the agent is, what it can do, how it should behave, and what it must never do. This is the most important configuration artifact. See General guidelines for creating AI agents and agentic workflows for guidelines on writing effective agent instructions.


## Configure tools

Tools give your agent the capabilities it needs to complete its tasks. Add only the tools your agent needs for its defined use case — tools expand the agent's access to platform data and actions, so limiting them to what is necessary is part of applying least-privilege principles.

**Important:** When configuring tools, consider the access each tool requires. A script tool using **GlideRecord** bypasses table-level ACLs — use **GlideRecordSecure** instead to ensure ACL checks are enforced.

## Configure access controls

Access controls must be configured before you test or deploy your agent. There are two distinct layers to configure:

**Who can invoke the agent \(ACLs\):** ACLs determine which users can discover and invoke your agent. Configure a separate ACL for each agent and each agentic workflow. For instructions, see Define security controls for an AI agent for AI agents and Define security controls for an agentic workflow for agentic workflows.

**What the agent can access \(user identity\):** User identity determines what data the agent has access to once invoked. Choose one of the following:

-   **Dynamic user \(recommended default\)**

    The agent runs with the roles of the user who invoked it. Use this option unless the agent requires elevated access that the invoking user does not have.

-   **AI user**

    The agent runs as a dedicated AI user account with fixed assigned roles, regardless of who invoked it. Use this option only when the agent needs access that cannot be granted through the invoking user's roles.


For a full explanation of how ACLs and user identities interact across the agent, agentic workflow, and tool layers, see Implement access control in Now Assist AI agents.

## Apply role masking

If your agent runs as a dynamic user, use role masking to define an allow-list of roles the agent can inherit from the invoking user. This enforces least-privilege access during tool execution and helps prevent agentic overreach — the agent cannot use roles beyond what is explicitly permitted, even if the invoking user has broader access.

See Role masking in Now Assist AI agents for an explanation of how role masking works across the agent, workflow, and tool layers, and see Define security controls for an AI agent for configuration steps.

## Next step

When your agent is built, tools are configured, and access controls are set, proceed to [Configure security controls](naai-tutorial-configure-security.md).

**Parent Topic:**[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)

