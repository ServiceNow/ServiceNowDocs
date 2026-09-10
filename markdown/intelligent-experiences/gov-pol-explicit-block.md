---
title: Explicit Block policies
description: Stop a specific person, team, or your whole organization from using an AI agent, model, or domain, enforced automatically everywhere that access could happen.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-pol-explicit-block.html
release: zurich
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Policies, Explicit Block, access control]
breadcrumb: [Explore, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Explicit Block policies

Stop a specific person, team, or your whole organization from using an AI agent, model, or domain, enforced automatically everywhere that access could happen.

## Key benefits

-   Stop a specific person, team, or your entire organization from using an AI agent, model, or domain, without writing a script for each platform.
-   Apply one rule consistently whether it covers a handful of contractors or thousands of employees, without reconfiguring it person by person.
-   Keep enforcing at every connected point even if one point is unavailable or doesn't apply, instead of the whole block depending on all of them.

## How Explicit Block policies work

You define who's blocked and what they're blocked from, and publish it. Restricting access this way usually means writing a custom script for each platform involved, or relying on someone to remember to check and revoke access manually; an Explicit Block policy replaces that with one rule, enforced consistently everywhere that access could happen. The policy stands until it's deactivated; there's no pause or in-between state.

Enforcement is attempted independently at each connected point, so if one point is unreachable or doesn't apply, the block still takes effect everywhere else it can.

Because Explicit Block covers users, groups, agents, models, and domains under this same mechanism, the same policy type applies whether the goal is keeping a contractor off internally sensitive tools or keeping an entire department off a model that isn't approved for their work.

## Use cases

-   **Blocking access to an agent**

    Employees use a ServiceNow desktop conversational agent to ask instance-specific questions. The organization might need to block one person from using it, for example while a security review is underway, or prevent anyone from using it at all until that review is complete.

    An Explicit Block policy scoped to a specific person and the conversational agent ends that person's active session and prevents them from starting a new one. Publishing the same policy without naming a person blocks everyone who has used the agent instead.

-   **Blocking access to a specific model**

    Employees often reach AI models directly, outside of any agent or approved workflow, through a browser or a desktop app installed on their own machine. An organization might restrict this to internally hosted models only, or allow certain roles to use specific external models while keeping others off-limits.

    An Explicit Block policy can target a specific model for a specific person: for example, blocking one employee's access to an external model while leaving everyone else's access untouched. Enforcement happens at the device level, so the block applies no matter which application or browser the employee uses to try to reach that model.


