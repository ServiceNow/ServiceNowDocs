---
title: Policy management and governance in ServiceNow Arc
description: Policies are governance rules on your ServiceNow instance that control what ServiceNow Arc can do, which actions need approval, and which actions are blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/policy-management-cowork.html
release: australia
topic_type: concept
last_updated: "2026-09-07"
reading_time_minutes: 3
keywords: [policy, ServiceNow Cowork, Cowork, governance, guardrail, tool gate, approval pattern, network rules, sandbox rules]
breadcrumb: [Explore, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Policy management and governance in ServiceNow Arc

Policies are governance rules on your ServiceNow instance that control what ServiceNow Arc can do, which actions need approval, and which actions are blocked.

ServiceNow Arc is an autonomous AI agent that runs commands, reads and writes files, and reaches external systems on behalf of users. Because the agent acts for users, your organization needs control over what the agent can do.

Policies give you that control. You author policies on the ServiceNow instance, and every ServiceNow Arc client enforces them on every action before the action runs. Users work within the boundaries set and approve actions when a policy requires it. Policies are the centrally managed rules and governance components that control what the agent can and can't do, preventing it from taking actions outside the boundaries you define.

The following properties make policy a governance mechanism rather than guidance:

-   **Central authoring**

    Policies live in ServiceNow tables on your instance, not in local configuration that a user can edit.

    You can author policies in Arc tables or in AI Control Tower, on the **Arc policies** tab under **Govern** &gt; **Policies**. For more information, see [Manage Arc agent policies in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/manage-arc-policies-aict.md).

-   **Enforcement in code**

    Neither the agent nor end users can bypass policy rules. Enforcement happens in code, not through the agent's instructions, so it doesn't depend on the agent choosing to conform.

-   **Mandatory policy**

    ServiceNow Arc runs nothing without a policy. Until the client retrieves an active policy from your instance, Arc doesn't perform any action.


## How policy reaches the client

The instance merges every policy that applies to a user and sends the client one effective policy bundle. Clients never see the individual policy records.

When you change a policy, the instance pushes the change to clients in near real time. Clients also check for changes in case they miss a push. Users can see the last policy sync time in their ServiceNow Arc application under **Settings** &gt; **Agent Sandbox**.

A policy bundle doesn't expire. If the instance becomes unreachable, the client keeps enforcing the last policy it retrieved.

## Default Policy

Every instance includes the **Default Policy**. It's active, applies to all users, and includes values for all seven policy components. You can't edit or delete the **Default Policy**, or add rules to it. To change its behavior, create a policy with a lower priority number. For more information, see [Policy stacking and precedence in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-stacking-precedence-cowork.md).

For what each component controls, see [Policy components in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-components-cowork.md).

-   **[Policy components in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-components-cowork.md)**  
A ServiceNow Arc policy has seven components, each controlling a different part of what the agent can do.
-   **[Action approval flow in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/action-approval-flow-cowork.md)**  
Tool gates, approval patterns, and auto approval determine whether each action in Arc runs, requires approval, or is blocked.
-   **[Policy stacking and precedence in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-stacking-precedence-cowork.md)**  
When more than one policy applies to a user, ServiceNow Arc merges them and resolves conflicts by priority in a fixed order, specificity, and restrictiveness.
-   **[How policy affects ServiceNow Arc users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-effect-cowork-users.md)**  
Your administrator's policies decide what ServiceNow Arc can do for you. You see the result as approval prompts and blocked actions, and you can narrow some permissions yourself.

**Parent Topic:**[Exploring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-exploring.md)

