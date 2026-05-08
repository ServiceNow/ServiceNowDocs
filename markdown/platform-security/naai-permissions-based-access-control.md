---
title: Permissions-based access control
description: Use Agent Role Inheritance, identity types, and granular roles to verify your AI agents have only the permissions they need, and can act only within their intended boundaries.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Agentic AI security and governance]
---

# Permissions-based access control

Use Agent Role Inheritance, identity types, and granular roles to verify your AI agents have only the permissions they need, and can act only within their intended boundaries.

ServiceNow uses AI Agents to perform tasks that range from simple automated responses to complex problem solving. AI agents are restricted by their assigner roles, and are subject to the same ACL limitations as standard users.

Now Assist provides several mechanisms to enforce least-privilege access across your

-   Access control lists \(ACLs\) that determine who can invoke an agent, user identities that define what data an agent can access once invoked.
-   Role masking that limits inherited permissions during tool execution

These controls help avoid agentic overreach and verify that AI agents operate within boundaries you define.

## Access controls for AI agents

The following topics describe how to implement, configure, and verify access controls for Now Assist AI agents and agentic workflows.

-   **Implement access control in Now Assist AI agents**

    Understand how ACLs and user identities work together across agentic workflows, AI agents, and tools to control who can invoke an agent and what resources it can access once invoked.

-   **Role masking in Now Assist AI agents**

    Use role masking to define an allow-list of roles that agentic workflows and AI agents can inherit from invoking users, enforcing least-privilege access during tool execution.

-   **Define security controls for an AI agent**

    Step through the AI agent guided setup to configure who can access an agent and what data it can act on, covering both user access and data access settings.

-   **Define security controls for an agentic workflow**

    Step through the agentic workflow guided setup to configure who can access a workflow and what data it can act on, covering both user access and data access settings.

-   **Test user access to an AI agent**

    Run a manual access test to confirm that only the intended users can discover and invoke a given AI agent.

-   **Test user access to an agentic workflow**

    Run a manual access test to confirm that only the intended users can discover and invoke a given agentic workflow.

-   **Configure security controls for a skill**

    Configure access control for custom skills built with the Now Assist Skill Kit to manage who can invoke skill-based functionality.


## Roles and permissions reference

The following reference topics describe the roles installed with Now Assist and what each role permits.

-   **Now Assist Admin roles**

    A reference list of the roles installed with Now Assist Admin, including the permissions required to activate and manage Now Assist features and skills.

-   **Now Assist Admin \[sn\_nowassist\_admin.nsa\_admin\]**

    Details the **sn\_nowassist\_admin.nsa\_admin** role, which allows users to create, edit, and configure Now Assist skills and settings.

-   **Now Assist Admin console user \[sn\_nowassist\_admin.user\]**

    Details the **sn\_nowassist\_admin.user** role, which provides read-only access to the Now Assist Admin console.


**Parent Topic:**[Agentic AI security and governance](now-assist-security.md)

