---
title: Arc policies
description: Control which tools, commands, network destinations, files, and connector permissions ServiceNow Arc can use on your users' devices, and which actions wait for a person's approval, from AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-policies.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, arc policies, servicenow arc, arc governance]
breadcrumb: [Explore, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Arc policies

Control which tools, commands, network destinations, files, and connector permissions ServiceNow Arc can use on your users' devices, and which actions wait for a person's approval, from AI Control Tower.

## Key benefits

-   Keep routine work moving while actions that delete data, change external systems, or send messages wait for a person's decision.
-   Limit the tools, hosts, files, and connector permissions Arc can use on your users' devices.
-   Give specific teams different Arc behavior without changing the default for everyone else.

## How Arc policies work

ServiceNow Arc is an autonomous AI agent that runs commands, reads and writes files, and reaches external systems on behalf of users. Because it acts for users, your organization needs control over what it can do.

Arc policies give you that control. You manage them centrally from AI Control Tower, and Arc checks every action against the policies that apply to the user before the action runs. Enforcement is built into Arc itself, so neither the agent nor the user can bypass a policy. For how policies reach the desktop application, see .

Every user starts with the default Arc policy. To change what Arc does for a group, you create a policy for that group and add rules for only the behavior you want to change.

Explicit Block policies can also apply to Arc, but they do a different job. An Explicit Block policy stops a person, or everyone, from using Arc at all. An Arc policy shapes what Arc can do for the people who use it. For details on blocking access, see [Explicit Block policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-explicit-block.md).

For installation, connectors, and everyday use of the desktop application, see .

## Use cases

-   **Opening an internal site for one team**

    Your developers need Arc to reach an internal package registry that the default policy doesn't allow.

    A policy for the developer group with a network rule that allows the registry's host makes it reachable for developers only. Everyone else keeps the default allowlist.

-   **Pausing infrastructure changes for review**

    Your platform engineers use Arc to work on infrastructure code, and applying a change affects live systems.

    An approval pattern with a hard gate makes every apply wait for the engineer's approval. Planning a change and other commands that don't match the pattern aren't affected.

-   **Piloting auto mode with one team**

    Your organization wants to try auto mode with one team before rolling it out more widely.

    A policy for the pilot team turns on the auto approval capability and sets the tools the team uses most to auto approval. The rest of your organization keeps the default prompts.


