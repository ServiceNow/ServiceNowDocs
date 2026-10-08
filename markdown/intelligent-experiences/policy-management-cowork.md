---
title: Policy management and governance in ServiceNow Cowork
description: Policies are governance rules on your ServiceNow instance that control what ServiceNow Cowork can do, which actions need approval, and which actions are blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/policy-management-cowork.html
release: australia
topic_type: concept
last_updated: "2026-09-07"
reading_time_minutes: 3
keywords: [policy, ServiceNow Cowork, Cowork, governance, guardrail, tool gate, approval pattern, network rules, sandbox rules]
breadcrumb: [Explore Cowork, ServiceNow Cowork, Enable AI experiences]
---

# Policy management and governance in ServiceNow Cowork

Policies are governance rules on your ServiceNow instance that control what ServiceNow Cowork can do, which actions need approval, and which actions are blocked.

ServiceNow Cowork is an autonomous AI agent that runs commands, reads and writes files, and reaches external systems on behalf of users. Because the agent acts for users, your organization needs control over what the agent can do.

Policies give you that control. You author policies on the ServiceNow instance, and every ServiceNow Cowork client enforces them on every action before the action runs. Users work within the boundaries set and approve actions when a policy requires it. Policies are the centrally managed rules and governance components that control what the agent can and can't do, preventing it from taking actions outside the boundaries you define. Every action the agent attempts is evaluated against the active policy before it runs.

The following properties make policy a governance mechanism rather than guidance:

-   **Central authoring**

    Policies live in ServiceNow tables on your instance, not in local configuration that a user can edit.

-   **Enforcement in code**

    ServiceNow Cowork enforces policy on every action, and neither the agent nor end users can bypass policy rules. Enforcement happens in code, not through the agent's instructions, so it doesn't depend on the agent choosing to conform.

-   **Mandatory policy**

    ServiceNow Cowork runs nothing without a policy. Until the client retrieves an active policy from your instance, Cowork doesn't perform any action.


## How policy reaches the client

The instance merges every policy that applies to a user and sends the client one effective policy bundle. Clients never see the individual policy records.

When you change a policy, the instance pushes the change to clients in near real time. Clients also check for changes in case they miss a push. Users can see the last policy sync time in their ServiceNow Cowork application under **Settings** &gt; **Agent Sandbox**.

A policy bundle doesn't expire. If the instance becomes unreachable, the client keeps enforcing the last policy it retrieved.

## Default Policy

Every instance includes the **Default Policy**. It's active, applies to all users, and includes values for all seven policy components. You can't edit the **Default Policy**. To change its behavior, create a policy with a lower priority number. For more information, see [Policy stacking and precedence in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-stacking-precedence-cowork.md).

For what each component controls, see [Policy components in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-components-cowork.md).

-   **[Policy components in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-components-cowork.md)**  
A ServiceNow Cowork policy has seven components, each controlling a different part of what the agent can do.
-   **[Action approval flow in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/action-approval-flow-cowork.md)**  
Tool gates, approval patterns, and auto approval determine whether each action in Cowork runs, requires approval, or is blocked.
-   **[Policy stacking and precedence in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-stacking-precedence-cowork.md)**  
When more than one policy applies to a user, ServiceNow Cowork merges them and resolves conflicts by priority in a fixed order, specificity, and restrictiveness.
-   **[How policy affects ServiceNow Cowork users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-effect-cowork-users.md)**  
Your administrator's policies decide what ServiceNow Cowork can do for you. You see the result as approval prompts and blocked actions, and you can narrow some permissions yourself.

**Parent Topic:**[Exploring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/servicenow-cowork-exploring.md)

