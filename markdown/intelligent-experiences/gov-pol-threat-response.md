---
title: Threat Response policies
description: Automatically contain an AI agent the moment it crosses a risk threshold you define, instead of waiting for someone to notice and act.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-threat-response.html
release: australia
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Policies, Threat Response, containment]
breadcrumb: [Explore, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Threat Response policies

Automatically contain an AI agent the moment it crosses a risk threshold you define, instead of waiting for someone to notice and act.

## Key benefits

-   Contain a misbehaving or compromised agent the moment a defined threat is detected, without waiting for someone to notice and react.
-   Apply the same containment rule across every platform your agents run on, instead of building a separate mechanism for each one.
-   Reduce how long a risky agent stays active, since the response happens automatically instead of depending on when someone happens to check.

## How Threat Response policies work

You choose a threat category and define its scope; the policy then watches continuously for conditions matching that category within that scope. Between a threat being detected and someone noticing and manually shutting down the affected agent, there's normally a window where that agent keeps acting. A Threat Response policy closes that window: once a matching detection occurs, it contains the affected agent automatically, without waiting on a person to be available, notice, and react.

The same policy applies across every enforcement point you've configured. An organization running agents across ServiceNow and multiple cloud providers doesn't need a separate containment mechanism for each one; a single rule reaches all of them, each enforced through that platform's own native access control.

The following connectors are supported:

-   AWS Bedrock
-   AWS Bedrock Agent Core
-   Gemini Enterprise Agent Platform \(agents with unique identities only\)
-   Azure AI Foundry
-   ServiceNow Agents
-   Agent Client Collector \(ACC\)

A connection between AI Control Tower and an identity provider is optional. Okta is supported.

A policy can also be changed without leaving stale enforcement behind: editing one reverses what it previously enforced and reapplies enforcement for the updated conditions, so a refined rule doesn't leave an old block sitting in place alongside a new one.

## Use cases

-   **Containing an agent that deviates from its goal**

    An agent is given a defined task, but through a misconfiguration, a bad tool call, or unexpected input, it starts acting outside that task. Left running, it keeps taking those actions until someone catches it.

    A Threat Response policy scoped to the Agentic Goal Deviation threat category watches for exactly this. When a detection matches the category and the policy's scope, the affected agent is taken offline automatically.

    The agent stays offline until someone reinstates it from Security. The policy itself keeps running and will contain the next agent that matches its conditions.

-   **Containing an agent under repeated prompt injection attempts**

    An agent that processes external or user-submitted content, such as documents or messages, can be exposed to prompt injection: hidden instructions embedded in that content that try to override its original task. A single attempt might not be a real problem, but a sudden spike suggests something is actively probing it.

    A Threat Response policy scoped to the Prompt Injection threat category can use a threshold instead of triggering on every detection, for example, more than a set number of attempts within an hour.

    Once that threshold is crossed, the affected agent is taken offline automatically, the same way as any other Threat Response policy.


