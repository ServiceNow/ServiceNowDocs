---
title: ACLs, role masking, and user identities in AI Agent Studio
description: Access control lists \(ACLs\) and role masking serve distinct security functions in AI Agent Studio. The difference between these two mechanisms helps you configure agents with the correct permissions and access boundaries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/acls-and-rolemasking.html
release: zurich
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 5
breadcrumb: [Security for AI agents, Configure, Now Assist AI agents, Enable AI experiences]
---

# ACLs, role masking, and user identities in AI Agent Studio

Access control lists \(ACLs\) and role masking serve distinct security functions in AI Agent Studio. The difference between these two mechanisms helps you configure agents with the correct permissions and access boundaries.

## ACLs: controlling access to the agent

ACLs define who can access an AI agent. They determine which users, groups, or roles are permitted to interact with or invoke the agent. ACLs don't govern what the agent is allowed to do once it is running.

ACLs control who can access an AI agent. The user identities and role masking control what the agent can do. Using them together verifies that agents operate within defined security boundaries. An ACL determines which roles a user must have to be allowed to invoke an AI agent. If a user is not permitted by the ACL, they can't reach the agent at all.

User identities and role masking determine what the agent can do once it is invoked \(that is, e once the invoking user has passed the ACL check\). User identities restrict the agent’s permissions to the roles of the user identity with which the agent is executing. Role masking is a configuration for agents set to run as Dynamic Users, which further reduces the scope of roles the agent is permitted to run with by allowing the agent to execute only with the subset of the invoking user’s roles which are also on the permitted roles list of the agent. Together, the user identity and role masking restrict the agent's effective permissions at runtime — limiting which records it can read or write and which operations it can perform. The agent can't exceed the permissions defined by its masked role, even if the invoking user has broader access. Therefore, both user identity and role masking mechanisms are required for complete agent security.

## Role masking: controlling what the agent can do

Role masking defines is a means of further restricting what data and actions an AI agent can access and perform when configured to run as a Dynamic user. Like user identities, role masking controls the agent's permissions at runtime — which records it can read or write, which operations it can execute, and which resources it can access on behalf of a user.

Role masking works by restricting the agent's roles to a subset of the permissions available to the invoking user. Even if the invoking user has broader access, the agent operates only within the permissions defined by its masked role. This is a way to verify that even when invoked by users with high privileges, Dynamic User AI agents run only with the roles that are pertinent to their task and cannot access unrelated data or take high privileged actions.

## Key distinction

A common source of confusion is assuming that ACLs define agent actions. They don't! Use the following summary to distinguish the mechanisms:

|Feature|ACLs|Role masking|User identities|
|-------|----|------------|---------------|
|Controls|Who can access the agent|What the agent can do|Which identity the agent acts as|
|Applied to|Users, groups, and roles that invoke the agent|The agent's runtime execution context|The dynamic user assigned at runtime|
|Security purpose|Restricts agent visibility and invocation|Restricts agent actions and data access|Determines privilege scope during execution|

|Feature|AI user|Dynamic user|
|-------|-------|------------|
|Definition|A predefined identity the agent runs as|A runtime identity assigned to the agent during execution|
|Role masking applies|No|Yes|
|Roles used|Fixed to the AI user's assigned roles|Scoped down by role masking|
|Identity source|Configured statically|Determined dynamically at runtime|

## ACL and role masking evaluation sequence

The following sequence defines how ACLs and role masks are evaluated across the agentic workflow, AI agent, and tool execution contexts:

-   **Step 1: Agentic workflow ACL validation**

    ACLs configured for workflows are evaluated against the invoking user \(automated or conversational\) session roles.

-   **Step 2: Agentic workflow role mask application**

    If the invoking user meets the agentic workflow's ACL criteria \(and the agentic workflow is set to run as a dynamic user with role masking configured\), the agentic workflow role masking is applied to the invoking user's roles \(there by restricting roles from the user session based on the intersection with the configured role masking\).

-   **Step 3: AI agent ACL validation**

    When an agentic workflow invokes an AI agent, the AI agents' ACLs are validated against one AI agent ACLs are validated against one of the roles with which the agentic workflow was approved to execute. Thus:

    -   If the agentic workflow was set to run as an AI user, the AI agent ACL will validate against the AI user session configured at the workflow.
    -   If the agentic workflow was set to run as a dynamic user with role masking, the AI agent ACL will check whether the effective remaining roles after applying the workflow role masking meets the ACL criteria.
-   **Step 4: AI agent role masking application**

    Similar to the agentic workflow above, either the AI user or the AI agent role mask is applied:

    -   If an AI user is selected, all roles of the AI user are enforced \(no masking\).
    -   If role mask is applied, then the roles are limited further based on intersection with the effective roles after applying the workflow role masking.
-   **Step 5: Tool ACL validation**

    If a tool uses ACLs, these are checked against the roles that the AI agent—assigned to the tool—is permitted to use. This means that if role masking is set up, only the roles left after masking are considered during validation.

-   **Step 6: Tool role masking application**

    If the tool is a skill and has role mask configured, then the approved roles will be applied to roles with which the AI agent was approved to run, thereby limiting roles for the tool's execution.


Summary of ACL and role masking evaluation order:

1.  **Agentic workflow ACLs** → validated with invoking \(conversational or automated\) user session's roles.
2.  **Agentic workflow role masking** → applied to the invoking user session.
3.  **AI agent ACLs** → validated with agentic workflow's approved roles \(agentic workflow's AI user OR roles after workflow role masking\).
4.  **AI agent role masking** → applied to agentic workflow's approved roles.
5.  **Tool ACLs** → validated with AI agent's approved roles \(AI agent's AI user or roles after agent role masking\).
6.  **Tool role mask \(Skills only\)** → applied to AI agent's approved roles.

**Note:** When evaluating ACLs and role masks, the admin can identify where and why execution failed due to either ACL or role mask restrictions.

## Why these security mechanisms matter

Using ACLs, role masking, and user identities together provides layered security for AI agents. ACLs prevent unauthorized users from reaching the agent. Role masking verifies that even authorized users can't trigger agent actions that exceed defined boundaries. User identities ensure the agent operates under the correct privilege scope at runtime, preventing escalation beyond what the assigned dynamic user permits. Configuring only one of these mechanisms leaves a gap in the agent's security posture.

